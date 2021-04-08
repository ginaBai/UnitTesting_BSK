Bowling Scorekeeper
===
The objective is to TEST an application that can calculate the score of a single bowling game.
- There is no graphical user interface.  
- You work ONLY with JUnit test cases in this project.
- You have ONE HOUR to work on this project.
- You are free to consult/use any online resources, including documentations, tutorials, Q&A sites, and any Eclipse built-in tools or plug-ins.
 

**Project Template**  
You are provided with a completed project that contains three classes: `Frame`, `BowlingGame` and `BowlingException`, each contains some fields and methods. DO NOT CHANGE the names and functionalities of the existing fields and methods.

You are expected to create JUnit test cases to verify the behavior of this implementation as thorough as possible based on the following description of a bowling score keeper. Your program should throw `BowlingException` in all error situations. 

**Bowling Score Keeper Task Description**  
The game consists of 10 frames as shown below. In each frame the player has two opportunities to knock down 10 pins. The score for the frame is the total number of pins knocked down, plus bonuses for strikes and spares.

![ExampleImage](https://github.com/ginaBai/UnitTesting_BSK/blob/master/BowlingScoreKeeper/BowlingScoreKeeperExample.png)

A spare is when the player knocks down all 10 pins in two throws. The bonus for that frame is the number of pins knocked down by the next throw. So in frame 3 of the example game below, the score is 10 (the total number knocked down) plus a bonus of 5 (the number of pins knocked down on the next throw).

A strike is when the player knocks down all 10 pins on his first try. The bonus for that frame is the value of the next two throws. 

In the tenth frame, a player who rolls a spare or strike is allowed to have bonus throws to complete the frame. However, no more than three balls can be rolled in tenth frame.

**Examples**  
[Click for Detailed Rules and Examples of Scoring a Game of Bowling](https://slocums.homestead.com/gamescore.html)

[Online Bowling Game Score Calculator](https://bowlinggenius.com)


# Checklists

Use the following checklists to improve the quality of your test suite. 

## Test Case Checklist

### Each test case *should*:
- [ ] be executable (i.e., it has an **@Test** annotation and can be run via “Run as JUnit Test”)
- [ ] have at least one assert statement or assert an exception is thrown. Example assert statements include: **assertTrue**, **assertFalse**, and **assertEquals** ([click for tutorials](https://www.baeldung.com/junit-assertions)). For asserting an exception is thrown, there are different approaches: **try{...; fail();} catch(Exception e){assertThat...;}**, **@Test(expected = exception.class)** in JUnit 4, or **assertThrows** in JUnit 5 ([click for tutorials](https://www.baeldung.com/junit-assert-exception)). 
- [ ]  evaluate/test only one method

### Each test case *could*:
- [ ] be descriptively named and commented
- [ ] If there is redundant setup code in multiple test cases, extract it into a common method (e.g., using **@Before**)
- [ ] If there are too many assert statements in a single test case (e.g., more than 5), you might split it up so each test evaluates one behavior.


## Test Suite Checklist

### The test suite *should*:
- [ ] have at least one test for each requirement
- [ ] appropriately use the setup and teardown code (e.g., **@Before**, which runs before each **@Test**)
- [ ] contain a fault-revealing test for each bug in the code (i.e., a test that fails)
- [ ] For each requirement, contain test cases for:
  - [ ] Valid inputs
  - [ ] Boundary cases
  - [ ] Invalid inputs
  - [ ] Expected exceptions
### To improve the test suite, you *could*:
- [ ] measure code coverage using an appropriate tool, such as EclEmma ([installation](https://www.eclemma.org/installation.html), [tutorial](https://www.eclipse.org/community/eclipse_newsletter/2015/august/article1.php)). Inspect uncovered code and write tests as appropriate.
