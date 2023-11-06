# DemoQuizApp

## Problem Statement:

The App follows a minimalistic design that is task oriented. The purpose of the app is to quiz students on their basic WEB development knowledge in a timed-manner.


## Functional features of the application

* Upon landing, reader is provided with a button to start a quiz
* Upon starting the quiz:
  * A timer is started for the question for 15 seconds
  * User is provided with 4 checkboxes as multiple choice (unique)
  * A button is provided to submit and move to the next question once a selection is made
* Once the user moves onto the next question:
  * Timer will be reset to 15
  * The user will be asked the next question and another submission
* Once the quiz is over, the user will be provided to try again or exit.
## Directory Structure and Setup of the App, and how different files are linked together

#### Directory Structure

The Directory structure is fairly straight forward, in the root directory, we have our index.html (our main content page), and 2 folders; css (where we store our styling for our website) and js (where we store our scripts for the website)

![alt text](https://i.imgur.com/QgY4l3V.png "Image of the File Structure")

#### How files work together

index.html serves as the main point of the application which connects to the css and javascript using reference links
stylecss contains the styling of the html elements for the quiz app
questions.js stores an array of quiz questions with options and the correct answer
quizApp.js provides all the logic the website uses to provide useful interactions for the user as they are navigating the quiz.


## Codebase explanation
* The index.html uses divs that are cycled through based on the button click.
  * Additionally, the div " Quiz box is dynamically altered based on the question the user is on
  * CSS, JS linkes are referenced within the header tag
* style.css is responsible for the overall styling of each HTML elements and animations such as:
  * Button highlights
  * Positioning of each element
  * Timer bar
* questions.js is only responsible of storing the "questions" array which holds:
  * Question number
  * question
  * answer
  * and options
* QuizApp.js provides the main functionality of the entire quiz application
  * At the top of the file, the code selects various HTML elements used in the app such as buttons, timers and question elements
  * Variables to control quiz operations
  * Event Listeners for the buttons mentioned above, which provide their own respective task (Start, Exit, Que e.t.c)
    * One major aspect of the event listener is, depending on the button selected, the application removes and adds classes from html elements. The reason for this is to help css determine when it's applied to a specific tag.
    * ShowQuestions functions dynamically generates the question based on the index(question user is on) of the array
    * OptionSelected works throug ha simple if/else statement that determines whether the users choice matches the correct choice.
    * Show results uses the variables to generate a score for users to view
    * Timer Control manages the timer for each questions, displaying a progress bar and handles time expiratiion (startTimer, and startTimerLine functions)
    * Que Counter updates the footer div in the HTML document to provide the user with which question they're on.
