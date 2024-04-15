---
layout: post
title: "What is Truth Problem: A faster Solution To The Testers' Problems"
categories: misc
meta: "what is truth problem"
permalink: /what-is-truth-problem
---
Recently, We got into one problem, where every one in the team has their own views in the output of a existing testcase. Every one has their different expectation for the output.
So we introduced with a problem statement named, <i> What is TRUTH??? </i>. [>>>>]({{ "/what-is-truth-problem" | absolute_url }})

What is this exactly? This basically helps in deciding what is true, what is correct output of an existing testcase.

While testing one of the existing feature on the code changes by developer, we got different output from different team members:

- Me: Output should be A,B,C
- Developer: Output is correct, i.e. A,B,P
- Business Analyst: Output should be A,B,C,P
After many round of discussion, and finding the flow of the code, we got to know our BA was correct as always that output should be A,B,C,P only.

But do we really needed to make this much discussion and trying to get the flow in backend and application documentation.

So we introduced a principle called, What is truth? 
We have a code working in production from very long, it would have any issue in very rare case.
And if their that defect would be not a critical because if its critical it should be on priority on fix side.

So we can just do operation by deploying the production code in test server and check the expected output, so easy? correct.

> What is Truth?? <br>
> Production Code is the TRUTH.

In fact, we have two servers to the test environment, on one we have the code on which change done by developer is there, and on one we have production code.
Simply compare the output any time if it gets into the confusion.

For a new member in the team, domain knowledge is the most important thing that is missing which get to know with time only.
What is truth problem is very useful for individual working on the application.
