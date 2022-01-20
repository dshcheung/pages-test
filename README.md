# Lab - Lab 10 Seconds Math <!-- omit in toc -->
- [Additional Resources](#additional-resources)
- [Starter code](#starter-code)
- [Introduction](#introduction)
- [Requirements](#requirements)
- [Bonus](#bonus)
  - [Before Game Starts](#before-game-starts)
  - [In Game](#in-game)
  - [When Game Finishes](#when-game-finishes)

# Additional Resources
- [W3School Events](https://www.w3schools.com/tags/ref_eventattributes.asp)
- [jQuery](https://api.jquery.com/)
- [jQuery Cheatsheet](https://oscarotero.com/jquery/)

# Starter code
- Click `Code` and copy the `ssh link`
- In your terminal navigate to your `unit-1` folder
- Use the command `$ git clone [ssh link]`
- Create a new branch `[your initials]-solution`
- Use Live Server

# Introduction
This game will help you get better at math by quickly solving small math problems. You have a visible timer that displays the time you have left to answer questions. When the counter reaches zero you are **game over**.

Everytime you get an answer right, you'll receive an additional **10 seconds** to keep playing. If you are fast enough, you can keep accumulating seconds to play. The game ends when you run out of time.

When the game ends, it will display your score and allow you to play again.

[Original Idea](http://www.mathster.com/10secondsmaths)

# Requirements
- Display:
  - `count-down clock`. Initial value is **10 seconds**
  - `random math problem` to solve. Initial operation is **addition** only

- When the user inputs any character in the `solution input`:
  - Timer will start counting down
  - Check the user's answer against the solution:
    - If the **answer is empty/wrong**:
      - Display a red border in the `solution input`
    - If the **answer is correct**:
      - Clear the `solution input`
      - Add 10 extra seconds to the `count-down clock`
      - Replaces question with a `new math problem`

- When the timer hits `zero`:
  - It will hide the `answer screen`
  - It will display:
    - `Game over screen`
    - Number of points accumulated by the user (5 per correct answer)

Visit [MDN Interval](https://developer.mozilla.org/en-US/docs/Web/API/WindowOrWorkerGlobalScope/setInterval) to see how to make JS invoke a function every x ms.

# Bonus
## Before Game Starts
- Add a slider to increase number generation difficulty: `10` (min) - `100` (max) in increments of 10
- Add checkboxes to select what operators to quiz: `addition`, `substraction`, and `multiplication`, and randomly generate problems for all kind of operations

## In Game
When the user guesses an answer right
- Add encouraging messages. Make them `show` for 5 seconds and then `fadeout`

## When Game Finishes
Calculate a better score based on:
  - Number of questions answered correctly
  - Selected difficulty (more difficulty == more points per answer)
  - Number of operators enabled (`{ add: 1, sub: 2, mult: 5 }`)
