# Context
Based on: 
 - https://stephenleewalker.wordpress.com/2015/09/09/tdd/#more-54
 - https://stephenleewalker.wordpress.com/2015/10/12/parallels-between-refactoring-and-tdd/#more-63

# Designing Software with TDD and Refactoring
At the start of my apprenticeship, whenever I got a new coding project I sat down with my notebook and designed the structure of the application. I attempted to determine all the implementation details of the application. However, many times I would run into some of the problems common of upfront design: there were problems I did not foresee, I implemented things that were never used, and I changed my design several times. It was clear that this approach, especially with problems I was unfamiliar with, was not effective. It was only after several mistakes and the guidance of my mentors that I realized I had the tools to produce quality software, but I was not using them correctly. These tools are Test Driven Development and refactoring. 

Test Driven Development (TDD) is the foundation of designing quality software.  Looking back at the start of my apprenticeship, my code suffered because I confused unit testing with TDD. In other words, just because I had tests did not mean I was applying TDD. Initially I was letting my understanding of an application's design drive my tests, rather than the other way around. 
> I need to translate a vector of integers into a map of values that I can use in my view to present a Tic-Tac-Toe board. To present the board in my view, I need an index for each table cell, I need to know what text goes in each cell, is the cell clickable, etc.

My desire was to fully understand the end product so that I could ensure I get there. But the beauty of TDD is that, "algorithms tend to write themselves" (Martin, Clean Coders Episode 19). 
  > Aside: A great example of this is the [Primes Factors Kata](http://butunclebob.com/ArticleS.UncleBob.ThePrimeFactorsKata).

It does this by enforcing the 'divide-and-conquer' technique to break down a problem. Applied appropriately, one starts with the base cases and works their way up. As a result, "as tests get more specific, code gets more generic", (Martin, [The Cycles Of TDD](http://blog.cleancoder.com/uncle-bob/2014/12/17/TheCyclesOfTDD.html)). It is not so much a conscience decision as it is a requirement to keep the lights green. 
> (testing "it can present an empty board space" ...)

> (testing "it can present an occupied board space" ...)

> (testing "it can present a board row" ...)

> (testing "it can present a board" ...)

I do not need to fully determine the implementation details at a project's start because I am confident that a design will emerge through TDD (This realization is why some refer to TDD as 'Test Driven Design'). That design is further defined and improved through refactoring.

Refactoring complements TDD to produce robust designs.  I used to think of refactoring as any change to your code that improves its design without changing its behavior. While this is true, I missed one important factor: refactoring is done in small steps. Like TDD, refactorings should be done incrementally, ensuring that all your tests still pass. The point of refactoring is to keep your application running while improving its design. In conjunction with TDD, a cycle develops: 
 - Write the least amount of code to create a failing unit test
 - Write the least amount of production code that is sufficient to pass the failing test
 - Refactor
 - Repeat 
 
As the solutions to problems emerge through TDD, that solution is constantly being improved through refactorings. This is why Martin Fowler states that, "refactoring can be an alternative to upfront design" (Refactoring, 67) - the idea is that through refactoring, you will better understand the system and make incremental improvements to the design. 

Throughout my apprenticeship I was reminded time and again that coming up with perfect solutions upfront is impossible. I still take out my notebook and plan out projects, but only minimal requirements. Rather than relying on fully understanding all the implementation details of a project, I am confident that a robust design will emerge through the application of TDD and refactoring.
