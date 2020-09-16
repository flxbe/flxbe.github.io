---
layout: post
title: "The Value Of Tests"
---

- Tests are an executable configuration.
- When test names are done correctly, one can easily grasp the expected component behavior by reading through the test names.
- Improve design, since you need good interfaces for every unit under test.
- As the code grows, refactoring or extensions can be made easily and with confidence, since the tests
  ensure the correct behavior.
- But: For very small programs with a short lifetime, the overhead of setting up and writing tests is often not worth it
  (expect for very easy testing of e.g. functions.)
  - Refactoring most likely never happens.
  - Even if: program is small enough to completely fit in the head, therefore very unlikely to have surprises when refactoring.
  - It is feasible to execute the small set of real use cases for a manual test.
