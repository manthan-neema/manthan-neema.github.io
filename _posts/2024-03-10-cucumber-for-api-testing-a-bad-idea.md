---
layout: post
title: "Testing API in BDD Style: Is it really a good Idea?"
categories: misc
meta: "API with cucumber"
permalink: /api-testing-using-cucumber
---
Recently I saw one of my colleagues using cucumber for API testing.
I thought was it a good idea to use BDD for API testing? [>>>>]({{ "/api-testing-using-cucumber" | absolute_url }})

Let's start with understanding the purpose of API testing and where it fits in the testing pyramid.
APIs are used to make low-level testing easy. It's an interface to connect to the code.
BDD is used to have a common understanding of what the whole functionality is supposed to be.

Using BDD for API testing, which is low-level testing is not a good idea at all in almost of the cases.

Firstly, using cucumber at a low-level design is wrong and didn't serve the purpose of BDD, which is collaboration.
Using cucumber like below should be avoided.

> Given I want to search on Wikipedia <br>
> When I send "Wikipedia" in the body of the search API <br>
> Then I should get the response status code as 200 <br>
> And I should get "Wikipedia" in the response body. <br>

The first thing, it is challenging for the end user to understand the above scenario it requires additional focus.
The second business team is not at all interested in this low-level design of API they are more for the technical team members.

Suppose you are writing a test case with cucumber like this, which is correct for collaboration within the team.

> Given I want to search on Wikipedia <br>
> When I Search for "Wikipedia" <br>
> Then I should get "Wikipedia" in response. <br>

In the above scenario, how will assert the different things in one test case you need to assert the status response code, response body, and headers as well if required, api authorization check authentication check etc.

That's why cucumber should be used for collaboration where end user directly envoled like UI where they directly interact with.
