---
layout: post
title: "Debugger: What's inside for Tester?"
categories: misc
meta: "Debugger & Testers"
permalink: /debugger-for-tester
---
Recently, I saw one of my developer friends using debugger, trying hard to find the root cause why his development code is not working.
After seeing him, I got a doubt, in my 4 years of experience I never use it in my testing code,
Is the debugger not for testers at all?

Already aware of what a debugger is and how to use it, still not using it, quite contradictarian.
I thought to interview someone as well to know if I miss something in understanding,
I approached my lead, and I asked him; he also had the same answer, I didn't use it in my 10-year career.

Let's start with what a debugger is? If our reader is not ware of.

According to wikipedia, "A debugger or debugging tool is a computer program used to test and debug other programs."
Debugger option can be found in all the latest IDEs, beside the run option like below: <br>

<img src="{{ "/assets/images/Debugger/debugger.png" | relative_url }}" title="IntelliJ IDEA Debugger" alt="IntelliJ IDEA Debugger">

Later, I think that why testers are not using debugger which developers overuse now and then.

I was able to find below following reason:
- Tester prefers to relly more on use of logs and rerun over debuggers.

But I personally feel the real reason is there is no such debugger of high quality available in the market that testers can efficiently use.
Think of a debugger where we can run a selenium script, and press some back button that will take me to code one line before, I can move to the last breakpoint step and again start.
How advantageous it will be, it will make selenium testcase debugging very easy.

> What's my learning through this incident?
- As no one is interested in creating this advance debugger nor such an article available on the internet, it doesn't have that value as of now and testes don't need that, least as of now at present.
- If tester does not need that, as of now, then test code should not be this complex that it should require any debugger at all other that of logging.
- It should be a simple concrete statement. 
For more, please refer to my another bolg <br>
(<a title="View Certificate" href="https://manthan-neema.github.io/generalized-testcases-nightmare-for-tester">Concrete Principle</a>)


