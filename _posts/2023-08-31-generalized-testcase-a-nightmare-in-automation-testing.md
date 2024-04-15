---
layout: post
title: "Generalised Testcases: A Nightmare In A Testers' Life"
categories: misc
meta: "concrete principle"
permalink: /generalized-testcases-nightmare-for-tester
---
Recently, one of my colleague was writing cucumber testcases for automating in a generalized manner. 
I feel it can be better, if it can be concrete instead of generalized one.
Why?? Generalized testcase have a lot of disadvantage in long term, top most is generalized testcase's meaning changed every time a tester read the testcase.
So I introduced with a rule named concrete principle. [>>>>]({{ "/generalized-testcases-nightmare-for-tester" | absolute_url }})

> What is Concrete Principle??  <br>
> Never start automating a testcase until you can have a concrete input and a concrete output beforehand.

The top advantage is whoever read it anytime, every one will have always one and only one understanding for the testcase.<br>
My colleague was creating a testcase for wikipedia like the below one:

> Given I want to search on wikipedia <br>
> When I Search for a word  <br>
> Then I should be able to see the word in the heading of the search result page  <br>

It seems to be correct functionality, correct? But, will it really work in the real life?? <br>
What is the <i> word </i> you want to search for? What is the <i> word </i> you want to verify in the heading on result page? <br>
It seems to have ambiguity in the testcase, if anytime testcase failed in the future. It would be nightmare to refactor the same. Trust me!!! <br>
And after-refactoring not sure if it will have the same intention as same as, when it was created initially because ambiguity is present from the starting point.

The same can be updated to follow concrete principle, like below one:

> When I search for word "Neema" on wikipedia <br>
> Then I should be able to see the word in the heading of the result page

It seems to be easier in understanding now, but still we will require to use data injection or some other method for matching the word in the <i> then step-definition </i>, if both the <i> given & when step-definitions </i> are in different classes,
which is a very normal case in an automation framework.

So to solve the problem, simply make the output also as concrete as the below one:

> When I search for word "Neema" on wikipedia <br>
> Then I should be able to see word "Neema" in the heading of the result page

Simply pass the input though <i> given step </i> and verify the output in <i> then step </i>.
Input/Output can be change in respective steps, but notice they are always <i> concrete </i>.

Tester should have intention to make things easy but NOT complex, generalization is for developer they need to have their code work for everything in generalized manner.
For an automation testers their code should run by passing concrete things in the testcases only.
