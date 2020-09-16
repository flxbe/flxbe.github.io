---
layout: page
title: "Testing"
---

This document is the entry point for a series of blog posts about software testing.
After struggling to write good tests myself for a few years, I wanted to share the strategies and ideas
which had the most impact on the quality of my tests.
This series will not be a beginners guide to testing in general.

Since I mainly have experience in developing small (one person) to medium sized projects
(2-4 persons, up to 2 years of development time), I can and will not discuss the effects of
these techniques for large scale projects.
All examples will only contain `javascript` or `rust` code, with which I have the most real
world experience.

## Setting

I always try to structure my tests into the three steps `setup`, `test` and `validate`.
I believe this structure to be generally accepted as a best-practice.

```js
describe("Doing some action", () => {
  test("should have the correct effect", () => {
    // setup
    const data = createTestData();

    // test
    const result = doStuff(data);

    // validate
    assert(isCorrect(result));
  });
});
```

There are many patterns and rules for the structure of the code under test.
Those are obviously very important for the test quality,
since it is a lot easier to write good tests for code which is written to be testable in the first place.
While writing testable code is necessary for good test, it is in my experience not sufficient in real world projects.
Each of the steps `setup`, `test` and `validate` have their own difficulties, even when the software
under test is already nicely structured.
At least for me, there have been many small ideas and approaches, which in the end accumulated to have a huge impact
for the quality and maintenance costs of my tests.
Within this series, I will try to write small posts focused an these ideas.

## General

No posts yet.

## Setup

No posts yet.

## Test

No posts yet.

## Validate

No posts yet.
