---
layout: post
title: "Top-Down Design"
---

- Start writing software at the outside of the system with a high level of abstraction
  - Extremely near at the user level
- Work down the stack, only implement more detailed and technical components as necessary
  - The correct structure of the domain is not always clear.
- Really nice for UI iterations
- But: How to write tests for components, to which the underlying software does not yet exist?
  - Easy for a test style heavily favoring mock objects
  - But: I do not like this style, because reasons
- There is no perfect solution: One has to provide some solution for lower level components for the tests to succeed.
- In Practice: Creating the necessary implementations can often lead to changes in multiple layers of the software
  and therefore writing more tests for these components during this step.
  - However: While not perfect, I dit not have an example, where this was unmanageable. Often, one can first provide some stub implementation, to first make the test pass. Later, properly test and implement the underlying code.
  - Even if you forget to fix a stub implementation, this will be caught during code review.
- This will scale badly as the software becomes increasingly "deep".
  - For very large projects, this may be a major drawback that needs to be addressed.
  - However: I did not have experience for those cases. I could always mitigate this by favoring shallow designs
    where possible (which are less complex anyway).
- Assuming all components are written, I however strongly favor the use of as much real world parts during the tests
  as possible.
  - While the struggle is arguably higher when not using mocks to create this state, once reached, I think it is worth it.
