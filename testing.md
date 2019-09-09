---
layout: page
title: "Testing"
---

This document is the entry point for a series of blog posts about software testing.
After struggling to write good tests myself for a few years, I wanted to share the strategies and ideas
which had the most impact on test quality.
This series will not be a beginners guide to testing in general.

## Setting

I always try to structure my tests into the three steps `setup`, `test` and `validate`.
I believe this structure to be generally accepted as a best-practice.

```js
describe("Doing some action", () => {
  test("should have the correct effect", () => {
    // setup: create test data
    const data = createTestData();

    // test: do some action
    const result = doStuff(data);

    // validate: check results
    assert(isCorrect(result));
  });
});
```

There are many patterns and rules for the structure of the code under test.
Those are obviously very important for the test quality,
since it is a lot easier to write good tests for code which is written to be testable in the first place.
While writing testable code is necessary for good test, it is in my experience not sufficient in real world projects.
Each of the steps `setup`, `test` and `validate` has its own difficulties, even when the software
under test is nicely structured.
At least for me, there have been many small ideas and approaches, which in the end accumulated to have a huge impact
for the quality and maintenance costs of my tests.
This series will therefore consist of focused posts about such ideas.

## Posts

### General

No posts yet.

### Setup

No posts yet.

### Test

No posts yet.

### Validate

No posts yet.
