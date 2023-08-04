# 100 Days of Python - Log

### Day 34: August 4, 2023

**Today's Progress**
* Completed Day 34 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Quizzler App](https://github.com/StingzLD/quizzler-app)
* [Day 34 - Replit - Type Hints](https://replit.com/@StingzLD/100DaysOfPython-Day-34-Type-Hints)

**Thoughts**
* My, oh my, has it been a while since I worked on this. Technically, yes, this 
  constitutes the breaking of the simple rules of #100DaysOfCode. Unfortunately, life 
  tends to encroach upon the free time required to dedicate ourselves to a long term, 
  daily commit such as this. I am sure if I did just the basics to get by, I could.
  However, I am not the kind of person to just "get by". I always take it upon myself to 
  go above and beyond, to do further research, and really understand the core concepts of 
  what I am doing. After all, the spirit of the challenge is to, well, challenge yourself!
  That means the "code for a minimum one hour a day" really means that I am spending three
  or four hours a day going into rabbit holes, and that is simply not sustainable. 
  
  Because of this, I am now going to be continuing this challenge at a more relaxed 
  pace. In fact, this challenge is no longer going to be "100 Days of Code", but 
  rather "Complete the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/) course". The whole reason for this 
  challenge is to push yourself and learn things you likely would not have otherwise, and 
  that is exactly what the course is doing. My journal entries are likely going to have 
  more days in between them now, or there may just be some small changes that were made 
  because that is all I had time to do that day. And you know what? That is perfectly 
  fine with me. I am still learning, and I am still challenging myself. I am just 
  doing so now without the undue stress that is placed upon you with the daily commitment
  required by the challenge itself.

  Happy coding, everyone!

### Day 33: January 12, 2023

**Today's Progress**
* Completed Day 32 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)
* Completed Day 33 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [IIS Overhead Notifier](https://github.com/StingzLD/iss-overhead-notifier)
* [Automated Birthday Telegram](https://github.com/StingzLD/automated-birthday-telegram)
* [Monday Motivational Quote](https://github.com/StingzLD/monday-motivational-quote)

**Thoughts**
* Having the actual days I have been coding and the day in the course be off has been 
  driving my OCD crazy, so I decided to do an extra lesson today to get it all back on 
  an even kilter. It actually worked out quite well, as Day 33 was very much tied to 
  Day 32 anyway.
* Day 32 was focused on SMTP, which  is definitely a topic I have been wanting to learn 
  about, as that is something I use quite often in my scripts for work. In all of the 
  projects today, it was used in a very simple manner, which is really the best way to 
  learn. I am hoping that it will get more involved by adding in HTML formatting, 
  maybe  even some tables, but if not I will just figure out a way to make it happen 
  like I always do.
* Day 33 was focused on APIs, which is also something I use quite often in my scripts 
  for work, so learning how to use them with Python was great. Combine that with the 
  SMTP work from the previous day, as well as the project being an ISS Overhead 
  Notifier, and you have a very happy man behind this keyboard.

  There was one challenge I had with this project, however it was not due to the APIs. 
  My brain at 10:00 PM (ish) is pretty much mush, and I was having the hardest time 
  trying to create logic to figure out if it is dark or not based on UTC time. 
  Initially, I just went "Okay, if the time is before the sunrise or after the sunset, 
  then it is dark!" Well... Turns out that is not always the case when it comes to UTC 
  because sunset could be 00:00 or later, which means that literally any time after 
  that point would be considered "dark" with the above logic. The solution to this is 
  quite simple, however with my mushy brain, it took me probably 30 minutes to figure 
  it out. The solution? Separate logic for if the sunset is before or after 00:00. If 
  it is after, then the current time must be both before sunrise _and_ after sunset. 
  If sunset is before 00:00, then it can only be one or the other.

### Day 32: January 11, 2023

**Today's Progress**
* Completed Day 31 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [German Flashcards](https://github.com/StingzLD/flashcards-german)

**Thoughts**
* There is a common theme running through this course, and that is the projects actually
  being useful, rather than some random project that has no further benefit after writing 
  it. For today, that project was creating a flashcard program. Specifically, this is to 
  learn a new language, but obviously it can be used for whatever you want to learn. The
  reason this one is so useful for me is I am actually learning German, so I just adapted 
  the program to use German words, and now I am off to the races!
* This flashcard program was an accumulation of the past few days' topics, so it was a 
  good combination of practice while using the concepts in a slightly different way. 
  There are some things that bug me about it that I have yet to resolve, like why I 
  was unable to remove the border around the button images, but I can always update the
  code once I come across an answer. 

### Day 31: January 10, 2023

**Today's Progress**
* Completed Day 30 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Password Manager](https://github.com/StingzLD/password-manager)
* [NATO Alphabet Generator](https://github.com/StingzLD/nato-alphabet-generator)
* [Day 30 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-30)

**Thoughts**
* The day started off by doing some error handling exercises followed by updating the 
  NATO Alphabet Generator to error handle anything input that is not a letter.
* The biggest emphasis of the day is ironic because I decided to stop making 
  changes to the Password Manager and move on with the course, only to find that the 
  course has me go work on the Password Manager some more. Win! One thing I really did 
  not like about it, which I do not think I mentioned before, is the fact that the 
  credentials were just being saved in a custom formatted text file, which is not ideal 
  in any situation. As luck would have it, today that converted to JSON. This not only 
  made the formatting of the passwords file much easier to read, it also allowed for 
  the addition of the Search function, which is pretty critical for a password manager.
* Continuing with the Linux vs Windows element mess, my OCD decided it was best to just 
  have two different versions. The initial design process is done in Linux, and then I 
  run the code in Windows and adjust as needed. This adjustment is saved to a separate 
  file, so no matter which platform you are using, you will have all of the elements 
  in their proper places. The only downside is any changes made to the code now has to 
  be made to two files, so I should probably put in logic that detects the OS and have
  everything handled accordingly, but for now this will do.

### Day 30: January 9, 2023

**Today's Progress**
* Continued developing Password Manager from Day 29 of the  
  [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Password Manager](https://github.com/StingzLD/password-manager)

**Thoughts**
* The more I worked on the Password Manager, the more I wanted to change things. So that
  is what I did! Here is a list of changes that I made:
  - Added blank field check
  - Added successful add notification
  - Added copy button to copy generated password
  - Found a way to open the app centered on the screen
  - Updated UI formatting
  
  Some of these were easy, while others had me searching on how to implement such change.
  The biggest issue I had was with the copy button. Windows will support emojis, which is
  how I was adding a clipboard to the button. When I switched to my laptop (Linux) to
  continue working on this, the clipboard did not appear because it apparently does not
  support emojis. This had me redesign it to use an image which had to be scaled 
  appropriately in order to fit inside the button.
* There were a couple of other items I tried to implement, but they did not go as planned 
  and were ultimately abandoned for the time being. An example of one is creating a text 
  pop that hovers over the copy button to simply say "Copy Password". Technically, I got
  it working. If I hovered over the button, the text displayed. Unfortunately, it brought 
  on an ugly side effect, which was messing up the entire layout for some reason. I 
  vouched to remove it for now, but that is something still on the radar to fix.

### Day 29: January 8, 2023

**Today's Progress**
* Completed Day 29 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Password Manager](https://github.com/StingzLD/password-manager)

**Thoughts**
* Another day, another useful project! Today's project was to create a GUI password 
  manager with an integrated password generator. This is going to be a project that I 
  end up packaging and using basically every day at work, mainly for the easy password 
  generator that I can just slap on my desktop. As such, I was definitely invested in 
  this project.

  I am sure I will be tweaking this the more I use it. One major change I know I will 
  be making is how the passwords are stored, as currently that is as plaintext and 
  easily accessible as you can get. This will need to be beefed up by adding the 
  requirement of a password to open the file and encryption to keep wandering fingers 
  and eyes away.

### Day 28: January 7, 2023

**Today's Progress**
* Completed Day 28 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Pomodoro Timer](https://github.com/StingzLD/pomodoro-timer)

**Thoughts**
* The Pomodoro Timer is a project that is something I can actually use, as it sets a clock
  and runs based on the Pomodoro Technique. The technique, along with screenshots, is 
  shown in the README.md file in the above repo on GitHub. This project is something I am 
  going to take and run with on another project, as pretty much every element in this 
  project can be used for another timer I am wanting to make. Good stuff!

### Day 27: January 6, 2023

**Today's Progress**
* Completed Day 27 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Miles to Kilometers Converter](https://github.com/StingzLD/mi-to-km-converter)
* [Tkinter Widget Demo](https://github.com/StingzLD/tkinter-widget-demo)
* [Day 27 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-27)

**Thoughts**
* It's a... GUI! One of the things that I have really wanted to get into is designing a 
  graphical user interface. I have had a couple of ideas in mind in the past, but I 
  never spent the time to actually learn how to do it. With today's coding, finally got to
  start that journey of learning how to do it. And now that I have the basics down, I can
  create essentially whatever basic application's GUI I want.

### Day 26: January 5, 2023

**Today's Progress**
* Completed Day 26 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [NATO Alphabet Generator](https://github.com/StingzLD/nato-alphabet-generator)
* [Pandas Exercise 7](https://replit.com/@StingzLD/pandas-exercises#exercise-7.py)
* [Day 26 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-26)

**Thoughts**
* Any day you get to learn something new is a great day, and today was a great day. Up to 
  now, I have only dealt with list comprehensions, but never dictionary comprehensions. I 
  did not even know those existed! And to add a cherry on top, I got to work with pandas 
  DataFrames data using the dictionary comprehension. So all-in-all, it was a great day.

### Day 25: January 4, 2023

**Today's Progress**
* Completed Day 25 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Name the States Game](https://github.com/StingzLD/us-states-game)
* [Pandas Exercises](https://replit.com/@StingzLD/pandas-exercises)

**Thoughts**
* The 'Name the States' game was a nice introduction into the pandas module. It
  combined the CSV parsing with the turtle module to create a game that worked well for
  both. As always, I think there is a way to improve upon the game, but the current
  iteration of it definitely works. What I would like to add, though, is a way to click
  on a state and then see if you answer it correctly.

### Day 24: January 3, 2023

**Today's Progress**
* Completed Day 24 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Snake Game](https://github.com/StingzLD/snake-game)
* [Day 24 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-24)

**Thoughts**
* It is ironic that today's work took me back to the snake game because I was thinking 
  about different improvements that could be made. Creating a persistent high score 
  between gaming sessions was not one of them, but it was certainly a good lead into 
  some other ideas I have for different projects. With the reading and writing of files 
  for persistent storage, a lot more options become available, like the small mail 
  merger project in the Replit above for automatically creating personalized invites 
  based on a list of names. 

### Day 23: January 2, 2023

**Today's Progress**
* Completed Day 23 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Turtle Crossing Game](https://github.com/StingzLD/turtle-crossing-game)

**Thoughts**
* The Turtle Crossing Game is the capstone project for all of the turtle module work 
  that has been completed recently. It takes all the bits and pieces from the various 
  games that have been created and put them all into one. Naturally, I had the input 
  lag issue I discussed yesterday, but it was more responsive in this game, so it 
  worked out just fine.
  
  All in all, creating the game was pretty fun. It is always fun 
  to see how quickly it goes from just a bunch of code with a couple of items on the 
  screen to a fully fleshed out game. One class and two lines of code in the main 
  script took it from just a turtle on the screen to a mass transit highway. Good luck!
* If you are looking at the code, you may notice an easter egg in there (or two). If you 
  notice it and understand the reference, let me know!

### Day 22: January 1, 2023

**Today's Progress**
* Completed Day 22 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Pong Game](https://github.com/StingzLD/pong-game)

**Thoughts**
* Happy New Year!
* Ironic that I start the new year by coding the classic Pong game. Overall, I really 
  enjoyed making the game. There are certainly limitations to what the turtle module 
  is capable of, though. The way it all works together means that the movement of the 
  paddles is awkward because it is lagging behind your intended movement, so you end 
  up moving way further than expected. When it does that, you are then locked in until 
  that sequence of key presses finishes, meaning the next player is now behind a few 
  cycles and is unfair.

  I am sure there is a way to circumvent this, but it is one of two issues I am having 
  right now that would not be easily addressable. THe other issue is sometimes the 
  ball gets "stuck" inside the paddle, bounces back and forth inside of it a few times,
  and then it will eventually zoom out because of the dynamic ball speed. I could 
  eventually figure this out, however it is going to take much more time than I currently 
  have available to work on it, especially considering the game is complete otherwise.

  There is one other tiny issue that could be quick to fix, which is the paddles are 
  currently able to move past the walls of the game. This really would not be as big 
  of an issue if the first issue above was resolved, however, because if the paddle moved 
  and stopped when you expected it to, you would never intentionally move it past the 
  walls.

### Day 21: December 31, 2022

**Today's Progress**
* Completed Day 21 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Snake Game](https://github.com/StingzLD/snake-game)

**Thoughts**
* To finish the snake game, there was still a bit of work to be done. In total, I added 
  a food and scoreboard class, updated the snake class to be able to extend the snake 
  by a segment when it eats an ap=le, and ; updated the main script to include all these 
  changes, as well as add the game over conditions. Overall, the game works just as it 
  should. The only thing that bugs me is the placement of the apple is not always 
  centered on the snake, so it is a bit awkward at times, but it still works. This is 
  something that can be improved upon in the future, though. See you all in the new year!

### Day 20: December 30, 2022

**Today's Progress**
* Completed Day 20 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Snake Game](https://github.com/StingzLD/snake-game)

**Thoughts**
* Ah, the infamous Snake Game from my old Nokia past. What nostalgia! Today was 
  focused on getting the basics completed: the screen, creating the snake, making the 
  snake move, user input to change the snake's direction, and doing so using OOP. 
  Using OOP in the various ways that I have during this course has really helped my 
  brain get more used to it because the reason behind using it actually makes a lot of 
  sense in comparison to how I initially learned it which was just the same old "This 
  is a blueprint of a car. Now our car has wheels, a color, etc.". The snake game is 
  really making it click more because it is something I have been thinking about doing 
  anyway. Not the snake game itself, per se, but making a game period.

### Day 19: December 29, 2022

**Today's Progress**
* Completed Day 19 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Etch-A-Sketch](https://github.com/StingzLD/etch-a-sketch)
* [Turtle Race](https://github.com/StingzLD/turtle-race)

**Thoughts**
* Turtles. Turtles everywhere! Continuing with the turtle module, there were two 
  different projects completed today.
* The first project was to create an Etch-A-Sketch, which ended up being much simpler
  than I was anticipating. When you actually think about it, the mechanics are
  ridiculously easy: move forward/backward and rotate your heading.
* This was followed by creating a turtle race, where you have a set of turtles line up at 
  the starting line, you make a bet on who will win, they move forward at random 
  intervals until one of them crosses the finish line, then you get told if you won or 
  lost. Naturally, I took it upon myself to make this more advanced than it really 
  need to be by autoscaling the turtle size, starting y positions, and the finish line 
  based on the sizes chosen for the screen width and height. What can I say? I am a 
  stickler for improving things.

### Day 18: December 28, 2022

**Today's Progress**
* Completed Day 18 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Hirst Painting](https://github.com/StingzLD/hirst-painting)
* [Day 18 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-18)

**Thoughts**
* Today was an interesting day. I got to further my dumbfoundness for contemporary art 
  because it just makes zero sense as to why these pieces sell for so much money. In 
  this case, it is the dot painting by Damien Hirst. It is literally just randomly 
  colored dots organized in a grid. One of them even sold for over 19 MILLION DOLLARS!!
  So incredibly ridiculous...

  At any rate, today's project was to create one of these paintings by extracting 
  colors from an image and then creating the "painting" via the turtle module. Pretty 
  fun little project that had me use a new module I have never touched, as well as use 
  some more of the turtle module that I have never used before.

### Day 17: December 27, 2022

**Today's Progress**
* Completed Day 17 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Trivia Game](https://github.com/StingzLD/trivia-game)

**Thoughts**
* As you can see, I took a nice little break to spend 100% of my time with the family. 
  I think we can all agree that is completely within the rules. Now back to business!

  I enjoy the fact that this course did not just introduce OOP and then move on to the 
  next thing. It actually continued using it with a whole new project, which was nice. 
  Creating the Trivia Game was another good round of practice with writing OOP, and 
  although the game is technically complete per the course requirements, I have more I 
  want to add to it (specifically working with APIs to pull the trivia data). In fact, I 
  even created a "next_step.py" file containing some of the changes I have already 
  started working on, and I updated the README.md file to 
  specify that more work is to be done on it.

### Day 16: December 23, 2022

**Today's Progress**
* Completed Day 16 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Coffee Machine](https://github.com/StingzLD/coffee-machine)

**Thoughts**
* Today was a good day for the course. It has now progressed to OOP, which is honestly 
  one of my weaker points of programming. I understand the concept, and I can write 
  and use the classes no problem, but my brain does not always think in OOP when 
  creating a script. This is admittedly due to not having a lot of practice with it, 
  as the vast majority of the scripts I have written over the years are written in 
  PowerShell and are either single task scripts or scripts that iterate through CSVs to 
  perform various tasks based on the data within them. So even though today's exercise was
  just a conversion of the coffee machine code, it was definitely good practice.

### Day 15: December 22, 2022

**Today's Progress**
* Completed Day 15 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Coffee Machine](https://github.com/StingzLD/coffee-machine/tree/main/old)

**Thoughts**
* Making a coffee machine was a neat little exercise. I had never really thought about 
  making a vending machine style program before, so it was good for my brain to get 
  that experience in.

### Day 14: December 21, 2022

**Today's Progress**
* Completed Day 14 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Day 14 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-14)

**Thoughts**
* This was the last lesson labelled as "beginner", so I am excited to finally move 
  past this section. This project was another higher/lower game, just with a twist. 
  Overall, it was still a very simplistic game, though. In fact, I ended up writing 
  the game in half of the lines of code that as the solution code had, as they had 
  made it far more difficult than it needed to be by adding in functions that would 
  never be used more than once. I mean, I get it. They want to showcase everything 
  that has been learned up to this point, but it was truly unnecessary in my opinion.

### Day 13: December 20, 2022

**Today's Progress**
* Completed Day 12 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)
* Completed Day 13 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Day 12 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-12)
* [Day 13 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-13)

**Thoughts**
* Funny enough, Day 12's project was labelled as the "final project", which was 
  significantly more simplistic than making the Blackjack game. Or maybe it was only more 
  simplistic because I took the Blackjack game too far past what was intended, even 
  though there are still improvements I want to make the game? Either way, Day 12 has 
  been completed.
* Day 13 was all about debugging, which was really no more debugging than has already 
  been performed throughout this course's exercises anyway. Thankfully, since I took 
  so long on the Blackjack game, this allowed me to complete two "days" in one day, so 
  I am now all caught up!

### Day 12: December 19, 2022

**Today's Progress**
* Completed Day 11 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Blackjack](https://github.com/StingzLD/blackjack)

**Thoughts**
* Per usual, I took a bit longer on this than anticipated. This is because I get 
  really into making sure everything is working one hundred percent as intended. With 
  this, I add debugging, see what is actually happening (even if the result is correct,
  is it actually getting that result in the intended way?), move code around, clean 
  code up, etc. 

  There is definitely still work that can be done to make the code much cleaner, and I 
  have already added in extra art to make the user experience that much better in the 
  next version of the game, but for the sake of moving forward with the course I am 
  calling it done for the time being. I may still work on it on the side, but it will 
  definitely be lower priority than anything else until I complete the course.

### Day 11: December 18, 2022

**Today's Progress**
* Started Day 11 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Blackjack](https://github.com/StingzLD/blackjack)

**Thoughts**
* Today was working on the first capstone of the course: Blackjack. I did not get 
  nearly as much completed as I wanted to, so I will have to pick it back up tomorrow 
  and play catch up.


### Day 10: December 17, 2022

**Today's Progress**
* Completed Day 10 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Day 10 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-10)
* [Calculator](https://github.com/StingzLD/calculator)

**Thoughts**
* This was the first time I was tasked with making a calculator. Although it was 
  simplistic, as the arithmetic is built-in to Python already, it is always nice to 
  create something that is actually useful.

### Day 9: December 16, 2022

**Today's Progress**
* Completed Day 9 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Day 9 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-9)

**Thoughts**
* Today's part of the course was definitely only geared towards learning a building 
  block of Python, one that I am definitely familiar with. As such, there was nothing 
  for me to learn today. But of course, it is always good to get some practice in to 
  keep it fresh in your mind.

### Day 8: December 15, 2022

**Today's Progress**
* Completed Day 8 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Day 8 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-8)
* [Caesar Cipher](https://github.com/StingzLD/caesar-cipher)

**Thoughts**
* Sadly, there was nothing new with today's work, as I have already created Caesar 
  Cipher scripts before. However, it was a good refresher on the topic.

### Day 7: December 14, 2022

**Today's Progress**
* Completed Day 7 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Day 7 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-7)
* [Hangman](https://github.com/StingzLD/hangman)

**Thoughts**
* Yet another fun little game, and one that we are all very familiar with: [Hangman.
](https://github.com/StingzLD/hangman) This was a nice exercise to really get my 
  brain back up and running, as it allowed me to think about how to accomplish certain 
  things in ways I have not used in a while. For example, the clearing of the screen 
  to refresh the content, as well as when and how to display certain content in 
  relation to that clear. My kiddos have really been loving Hangman the last few weeks,
  so this will be something nice to show them and play over the upcoming Christmas 
  break.  

### Day 6: December 13, 2022

**Today's Progress**
* Completed Day 6 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Day 6 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-6)

**Thoughts**
* I always love games, so adding [Reeborg's World](https://reeborg.ca/reeborg.html) to 
  the course was fun. I had actually never seen a "jumping hurdles" or "maze" 
  challenge before, so although easy to solve, it was still much more enjoyable than 
  your usual while loop exercises. This is something I will probably end up showing to 
  the kids when they want to move on from blockly and start learning Python.

### Day 5: December 12, 2022

**Today's Progress**
* Completed Day 5 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Day 5 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-5)
* [Password Generator](https://github.com/StingzLD/password-generator)

**Thoughts**
* Today's project was actually a pretty beneficial one, as it is something I use on a 
  regular basis for my job: A Password Generator. The general creation of the tool may 
  not have been very complex, however I did end up searching for and finding a new 
  method I have never used before: Shuffle. I have never had a need to shuffle a list 
  before, so it was pretty nifty to learn something new. I am definitely going to 
  continue to refine this password generator and cater it towards my exact needs.

### Day 4: December 11, 2022

**Today's Progress**
* Completed Day 4 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Day 4 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-4)
* [Rock Paper Scissors Terminal Game](https://github.com/StingzLD/rock-paper-scissors)

**Thoughts**
* Creating the [Rock Paper Scissors](https://github.com/StingzLD/rock-paper-scissors) 
  game was a bit more fun using the actual representation of the hand gesture in the 
  console. I think the logic could use some cleaning up, as I used hard coded 
  evaluations which would not scale well if there were more than three choices, so I 
  may work on that later. The trick to this, though, would be simplifying the logic 
  while also maintaining the detailed results of the game. For now, though, the game 
  is fully functional and a fun way to kill a minute or two.

### Day 3: December 10, 2022

**Today's Progress**
* Completed Day 3 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Day 3 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-3)

**Thoughts**
* The project for today might have been a simplistic one, but it was definitely fun and 
  got the creative juices flowing. It was a *Choose Your Own Adventure* game called 
  **Treasure Island**. If you want to take a peek at it, just head hit the Replit link 
  above and take a look at the treasure-island.py file.

### Day 2: December 9, 2022

**Today's Progress**
* Completed Day 2 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Day 2 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-2)

**Thoughts**
* Although this course is still in the very basics, I have decided to just go through 
  the motions, as there may be a piece of information I did not know or a trick that I 
  might learn. Either way, Day 2 complete!

### Day 1: December 8, 2022

**Today's Progress**
* Completed Day 1 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to work**
* [Day 1 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-1)

**Thoughts**
* Today I made the decision to challenge myself with another 100DaysOfCode challenge! It 
  has been about a year since I last really touched Python, as I have been primarily 
  coding with PowerShell, and I want to ensure I do not get rusty. I want my main focus 
  to be more on topics I do not have much experience in with Python, specifically: APIs, 
  creating applications and websites, scraping, etc. With my currently hectic schedule, 
  I do not want to spend a lot of time researching how to do things. As such, I set out 
  to find pre-designed content that would allow me to push my knowledge and complete my 
  goal.

  Luckily, I found [100 Days of Code: The Complete Python Pro Bootcamp for 2023
  ](https://www.udemy.com/course/100-days-of-code/), which appears to be just what I am 
  looking for. Although I took the assessment and was told to start a third of the way 
  in, I have decided to just go through the entire course as is, since there are projects 
  that I would miss out on. And who knows, I might learn something new about a *"basic"* 
  concept! That has certainly happened to me in the recent past, so maybe I will find 
  some new trick I have never seen before.

  Here's to 100 Days of Python!
