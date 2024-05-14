# Test Driven Development Presentation

**Duration:** 30 - 35 minutes

## Slides and Descriptions

### Slide 1 / 2 min

**Start Slide**

- Title of the presentation
- Name of the presenter
- Date
- Company, etc.

### Slides 2 - 4 / 3 min

**What is TDD?**

- Discuss the abbreviation and various interpretations/meanings of TDD:
  - **Test First Development:** Writing tests before writing the code.
  - **Test-Oriented Development:** Emphasis on a large number of tests.
  - **Test Driven Design:** Designing the code with tests in mind, such as writing tests for different modules.
  - **Test Driven Development & Design:** Writing tests first and allowing them to influence the design.

### Slides 5 - 7 / 2 min

**What is a Unit Test?**

- To understand TDD, we first need to know what a unit test is.
- Discuss about the test types (unit, integration, end-to-end, etc.) and focus on unit tests.
- Discuss the concept of a unit test, how many tests should be in a project, and why developers typically have fewer tests than needed.

### Slides 8 - 11 / 3 min

**How can unit tests help developers?**

- Discuss the benefits of unit tests:
  - Assisting in code writing.
  - Aiding in understanding the code – good tests serve as documentation.
  - Facilitating code refactoring – challenges of refactoring with poorly written tests.
  - Helping to find bugs – challenges of identifying bugs with unclear tests.

### Slides 12 - 15 / 5 min

**TDD vs. Simple Unit Testing**

- Discuss the differences between TDD and simple unit testing, noting that writing good unit tests and using TDD are different skills:
  - TDD does not help with test maintainability or readability.
  - TDD helps write trustworthy tests, improve the code's design, and divide the code into manageable pieces.
  - Benefits include incremental development, delivery time, and code quality.

### Slides 16 - 18 / 3 min

**Making test writing easier**

- Discuss the challenges of writing tests and how to simplify the process with a good testing environment, frameworks, and proper workflows.
- Highlight that if test writing only takes about 5 minutes, more tests are likely to be written.

### Slide 19 / 1 min

**Test Naming**

- Discuss the importance of test naming (e.g., `Test_Scenario_ExpectedResult`) and how it aids in understanding tests, finding bugs, and refactoring code.
- Mention that a poor test name might indicate issues with the test or the code.

### Slide 20 / 1 min

**Test Implementation**

- Discuss how to implement tests in a way that is easy to understand and maintain.

### Slide 21 / 3 min

**Real Test Example**

- Show a real test example, explaining the naming and code.

### Slides 22 - 24 / 3 min

**TDD Creation Steps**

- Red - Write the failing test. No code should be written without a failing test.
- Green - Write the code to pass the test, keeping it as simple as possible.
- Refactor - Refactor the code if necessary, ensuring it doesn't introduce new functionality.

### Slide 25 / 5 min

**TDD Test Writing Example**
Use a simple example (e.g., summing two numbers) to demonstrate the TDD steps.

- **What should I test first?** Begin with the simplest test that returns a value. For example, `sum(1,2)` should return `3`. Discuss the function's design: do we really need an actual addition function for two numbers? Perhaps it might be more efficient to consider a design like `sum(1)(2)`? This is a viable option because production code has not been written yet.

- **Run the test - it should fail.** We write a failing test first to validate the test's effectiveness—how else can we ensure the test will fail when the production code is incorrect? Consider this as a test for the test itself. What happens if we don't trust the tests and they all pass? We would end up debugging anyway. And if we don't trust the tests and some fail? Then, we wouldn't be overly concerned.

- **Now I can change the production code to make the test pass as simply as possible:** `sum(a,b) { return 3 }`.

- **Run the test - it should pass.** Now, if necessary, I can refactor the code.

- **What is the simplest failing test that will prove that the function is inadequate?** For instance, `sum(1,1)` should return `2`.

- **Run the test - it should fail.**

- **Now I can change the production code to make the test pass as simply as possible:** `sum(a,b) { return a + b }`. This seems sufficient for now. However, the next step is to consider edge cases—how can I break this function? For example, `sum(1, 'a')` should throw an error. Other edge cases to consider might include `sum(1, Infinity)` and `sum(1, NaN)`.


### Slides 26 - 28 / 5 min (Optional)

**Personal Impressions of TDD**

- Discuss personal experiences and the impact of having more test code than production code in projects. First impressions of TDD (lot of tests wihout any value) and how it has evolved over time (refactoring stage is easy, don't need to debug code).

### Final Slides / 1 min each

**Key Questions Addressed**

- **Why do we write the test before the code?** Consider the design first. Once the code is written, finding time for design considerations becomes much more challenging.

- **Why do we make the test fail first?** To test the test itself and validate its effectiveness. It proves that the test is functioning correctly by failing when expected.

- **Why do we write the simplest code to pass the test?** We don't need more than what the test requires. Writing only the code that is tested helps to maintain focus and forces us to write additional tests, thus increasing coverage.

- **Why do we refactor the code after the test passes?** Refactoring post-testing improves code quality in the safest way possible. We do not refactor untested code, nor do we refactor unless it's necessary, ensuring the integrity and efficiency of the codebase.

- **Why do we write edge cases?** To verify that the function is robust enough and not susceptible to common vulnerabilities. This ensures that the function is reusable and dependable in future scenarios.

- **What we should not cover by the tests?** Basicly, we should not cover the code, which is responsible for the implementation details. We have a unit of the functionality and we expect the correct behavior from it. The inner implementation like a private methods, helper functions should not be covered by the tests for this particular case.

- **Should we write negative cases?** Yes, but selectively. Negative cases should be written only when they are part of the expected functionality or business logic. For instance, if we know the `sum()` function should only operate with numbers, we must write a test for the case `sum(1, 'a')` to ensure proper handling of incorrect inputs. Additionally, cases like `sum(1, Infinity)` and `sum(1, NaN)` should also be tested to manage potential unexpected outcomes effectively. Contrariwise, negative cases should not be written if they do not align with the expected functionality or business logic. For example - third-party functions that can produce the unexpected results, but we can't predict them and should not handle them in this unit.

**Total Duration:** 31 minutes
