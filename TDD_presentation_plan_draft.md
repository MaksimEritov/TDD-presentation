Test Driven Development presentation

Time: 30 - 35 min

Slides in presentation with the description:

-------------------

1 slide / 2 Min : start slide. Title of the presentation, name of the presenter, date, company, etc.

-------------------

2 - 4 slides / 3 min :  What is TDD? Talk about the abbreviation and different understandings/meenings of TDD.

* Test First Development - Write tests first and then write the code,
* Test `Oriented` development - lot of tests
* Test Driven Design - designing the code with tests for example - write tests for the different modules
* Test Driven Development & Design - writing the tests first and let them change the design

-------------------

5 - 7 slides / 2 min : What the Unit Test is? - to understand the TDD we need to understand what the unit test is. Talk about the unit test, what is the unit test. How many tests should be in the project. Why usually developers they are much lower than they should be?

-------------------

8 - 11 slides / 3 min: How Unit test can help develper? - Talk about the benefits of the unit tests.

* How they can help the developer to write the code.
* How they can help to understand the code - good tests are the documentation.
* How they can help to refactor the code. - Difficulties of the refactoring with wrong written tests.
* How they can help to find the bugs - Difficulties of the finding bug with not undersatndable tests.

-------------------

12 - 15 slides / 5 min: TDD vs simple Unit Testing. - Talk about the difference between TDD and simple unit testing. Writing good unit tests and use TDD are a different skils.  

* TDD can't help with tests maitainability.
* TDD can't help with test readability.
* TDD help to wite trust-worthy tests. - Bad test example when someone set that this test supose to be failed.
* TDD help to improve the design of the code.
* TDD help to divide the code into small pieces. - divide and rule
* TDD help to increase the code coverage.

Profits:

* Increment development.
* Delivery time
* Code quality

-------------------

16 - 18 slides / 3 min: How to make test writing easier? - Talk about the difficulties of the test writing. How to make it easier - good testing environment setup. Good framework which can do test execution easy and fast. Good mocking framework. Good test data setup. Proper workflows. If someone would know that test writing will take only 5 min, he will write more tests.

-------------------

19 slide / 1 min: Test nameing - Talk about the importance of the test naming (Classic one - `Test_Scenario_ExpectedResult`. Cascade testing design in JS). How the test name can help to understand the test. How the test name can help to find the bug. How the test name can help to refactor the code. The test assertion mesage is useles if the test name is not good. If you can't find good name for test, it means that something wrong with the test or code.

-------------------

20 slide / 1 min: Test implementation. - Talk about the test implementation. How to write the test. How to write the test in the way that it will be easy to understand and maintain.

-------------------

21 slide / 3 min: Real test example. - Show the real test example with the naming and code explanation.

-------------------

22 - 24 slides / 3 min: TDD creation steps

* Red - Write the failing test. No code without failing test
* Green - Write the code to pass the test. As simple as possible. Without the unnecessary code.
* Refactor - If the code is not good, it's better to refactor it before writing the next test. Now when we have a tests, we can refactor the code without the fear to break something. But without adding new functionality.

-------------------

25 slide / 5 min: TDD test writing on a simple example (sum two numbers) - Show the TDD creation steps on a simple example.

* What should I test first? - simplest one which gave a value for the test. Example - `sum(1,2)` should return `3`. Disscuss about the function design - may be we dont need actuall add fucntion for 2 numbers? May be better to write something like `sum(1)(2)`? It's easy - the production code not exist yet. Production code is any code which is not a test code.
* Run the test - it should fail. We write the failing test first to prove the value of the test - how can we know that the test is good and it will fail when the production code is broken? Kinda test for the test. What if We don't belive in the tests and they all passed? We will debug anyway. What if We don't belive in the tests and some of them failed? We will not worry about it.
* Now I can change the production code to make the test pass as simple as possible. - `sum(a,b) { return 3 }`
* Run the test - it should pass. Now I can refactor the code if it's necessary.
* What the simplest failing test that will prove that the function is not good enough? - `sum(1,1)` should return `2`.
* Run the test - it should fail.
* Now I can change the production code to make the test pass as simple as possible. - `sum(a,b) { return a + b }`. Looks like it's good enough. But the next step is to think about the edge cases - how can I crush this function? For example - `sum(1, 'a')` should throw an error. Other edge cases - `sum(1, Infinity)`, `sum(1, NaN)`.

We work incrementally. We don't write the code which is not needed. We don't write the code which is not tested. We don't write the code which is not refactored.

-------------------

26 - 28 slide / 5 min / Optional: My impression about the TDD. Tests can be written without the permission. Developer don't need to ask. My own experience - project with the more tests code then the production one.

-------------------

- Why do we write the test before the code? - Think about design. You will never have a time after.
- Why do make test fail first? - Test the test. Prove the value of the test.
- Why do we write the simplest code to pass the test? - We don't need more. We don't need to write the code which is not tested. Force us to write more tests. Increase coverage
- Why do we refactor the code after the test pass? - We improve the code quality in a most secure way. We don't refactor the code which is not tested. We don't need to refactor the code which is not needed.
- Why do we write the edge cases? - To prove that the function is good enough. To prove that the function is not vulnerable and reuseable in the future.
- Should we write negative cases? - Yes, but not always. My consept is that we should write the negative cases only if we know that the the negative case is a part of predicted functionality or business logic. For instance - we know that `sum()` function should work only with numbers - we should write the test for the `sum(1, 'a')` case. Or we should consider that the `Infinity` or `NaN` are also a numbers, but can bring to the unexpected results. So we should write the test for the `sum(1, Infinity)` and `sum(1, NaN)` cases.

-------------------

Total minutes: 31 min
