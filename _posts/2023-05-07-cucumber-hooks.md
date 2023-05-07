---
layout: post
title: "Cucumber Hooks: When To Use What?"
categories: misc
meta: "Cucumber Hooks"
permalink: /cucumber-hooks-When-to-use-what
---
Hooks are used to execute a block of code at some point of cucumber Scenario Execution. They are one of the most important functionality of cucumber. 
But when to use which one, this can be used as initial guide to start with [>>>>]({{ "/cucumber-hooks-When-to-use-what" | absolute_url }})


> Global Hooks

Hook | Description | General Use Case |
--- | --- | --- | --- |
`@BeforeAll` | do executes before cucumber scenario execution starts | DataBase initialization, loading project property, if defined any |
`@AfterAll` | do executes after cucumber scenario execution completed | DataBase Disconnection |

> Scenario Hooks

Hook | Description | General Use Case |
--- | --- | --- | --- |
`@Before` | do executes before each and every scenario.| for initializing webdriver, <br> Its use should be avoided if what is being executed is important to display in Living Documentation, use Background instead. |
`@After` | do execute after each and every scenario | closing browser <br> Its use *should NOT* be done to clear test data in general, so that test case failure analysis can be done |

> Step Hooks

Hook | Description | General Use Case |
--- | --- | --- | --- |
`@BeforeStep` | do executes before each and every step, util some failed/skipped | Context dependent |
`@AfterStep`  | do executes after each and every step, util @BeforeStep is executed  | for taking screenshot, if required decision must be taken carefully it can affect performance |

> Conditional Hooks (Same can be applied at step level)

Hook | Description | General Use Case |
--- | --- | --- | --- |
`@After("@Manthan1")` | executes if tag applicable to scenario | for doing something for particular scenario |
`@After("@Manthan1 and @Manthan2")` | executes if All the tag applicable to scenario | It should be avoided as far as possible, at most it creates confusion when debuging |
`@After("@Manthan1 or @Manthan2")` | executes if any of the tag applicable to scenario | to execute same code, and avoid redundancy |
`@After("not @Manthan2")`  | executes if none of the tag applicable to scenario | It should also be avoided as fas as possible |
