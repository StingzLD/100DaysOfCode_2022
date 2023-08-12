# 100 Days of Python - Log

### August 12, 2023

**Today's Progress**
* Started Day 39 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [Flight Deals](https://github.com/StingzLD/flight-deals)

**External Links**
* [Tequila (flight search API by Kiwi)](https://tequila.kiwi.com/)
* [Sheety](https://sheety.co/)

**Thoughts**
* What a great capstone project, and it is one that I will actually use! The purpose of 
  this app is to pull in data from a Google Sheet using the Sheety API and determine if 
  flights to the cities in the sheet are found via the Tequila API for less than the 
  thresholds defined per ciy in the sheet. Of course, it is a little more involved than 
  that, as you are actually pulling in data from Tequila to update IATA city codes for 
  the cities on the list, then you end up using that data to look for flights to/from 
  all airports in that city code. I have not got to the latter part of the app yet, 
  though, so for now it does everything else.
* This was all written using OOP, which you might think is overkill, and in its 
  current form you are absolutely correct. However, this is all just Part 1 of the 
  capstone project. The next part builds on all of this. How? We shall find out in 
  another day or two! Regardless, writing the code using classes was a good way to 
  knock of the cobwebs and get my brain back in that mindset.

### August 11, 2023

**Today's Progress**
* Completed Day 38 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [Exercise Tracker](https://github.com/StingzLD/exercise-tracker)
* [Replit Version (adds timezone conversion)](
https://replit.com/@StingzLD/100DaysOfPython-Day-38-exercise-tracker)

**External Links**
* [Nutritionix](https://nutritionix.com/)
* [Sheety](https://sheety.co/)

**Thoughts**
* The first part of the project I should have replaced with something I am actually 
  interested in, as counting calories (especially getting artificial values for 
  exercises) is such a waste of time. Sure, calorie intake is important, but getting 
  your macros in order is much more important. You can eat a perfect amount of 
  calories every day in chocolate, but if it is all sugar, how does that really benefit 
  you? At the end of the day, this tracker is less useful than just Pixel. If you are 
  going to track exercises, tracking actual workout information (type, weight, reps, 
  sets, etc.) in order to show how you have progressed over time is going to be more 
  beneficial, in my opinion.
* Not that my little rant is over (sorry!), what I did really enjoy was using Sheety 
  to automatically populate the Google Sheets doc. This is super useful, and I can 
  definitely see using it again in the future. There was one quirk that took me a long 
  while to figure out what was going on, but I got it resolved, and everything is 
  working as intended now. The problem I ran into was a 400 Bad Request when calling 
  the Sheety API. The JSON body was supposed to be "nested in a singular root property 
  named after your sheet." My sheet was called "workouts", as is evident by the endpoint 
  url. Undoubtedly, the root property was not actually supposed to be "workouts", but 
  instead "workout" (without the "s"). I have zero idea why, as that makes zero sense 
  to me, but at the end of the day the why does not really matter, as long as it works.
  All-in-all, I will definitely be using Sheety again.
* The only additional part to this project was throwing it up in Replit to run from 
  wherever, which actually required a code change. Because the timezone of their 
  servers are UTC, I had to add in a new library that would convert the timezone to 
  the proper one. Nothing major, but it was another good library that I have not used 
  before but very likely will need again in the future.

### August 10, 2023

**Today's Progress**
* Completed Pixela Stopwatch Slack App

**Link to Work**
* [Habit Tracker](https://github.com/StingzLD/habit-tracker)

**External Links**
* [Pixela](https://pixe.la/)
* [Slack API](https://api.slack.com/)

**Thoughts**
* Turns out the timer I created yesterday did not work as I thought it would, but that 
  is also partially my fault. I noticed that whenever I used the slash command I 
  created in Slack, it never actually started or stopped a stopwatch. It only ever 
  incremented the quantity by one. After looking into it, I realized that I was just 
  following the basic webhook creation, which used the type of "increment". The 
  stopwatch webhook actually required the type of, you guessed it, "stopwatch".

  Before going through the process of editing and redeploying the app in Slack, I 
  decided it was better to just update my habit tracker code by adding in functions for 
  the stopwatch webhook creation and starting/stopping the stopwatch. I started with 
  the easier piece, which was the latter. You can start and stop the stopwatch without 
  the webhook, if you just use the token, which is what the rest of the code uses. 
  Because fo this, implementing that was a piece of cake, and I was able to start the 
  stopwatch without issue. I even noticed that the return text literally says 
  "Stopwatch start successful", which I have never seen before, so that verifies that 
  this was a much greater success than before!

  The webhook creation function should have been just as easy, but I ran into a JSON 
  serialization error that just made no sense to me because I was doing everything 
  exactly the same as other functions I have created and were working just fine. After 
  fumbling with it for way, way, way too long, I finally realized what the issue was. The 
  value for "graphID" was using curly brackets around the variable (I had just copied 
  and pasted that part of the URL string), which meant the interpreter was thinking 
  the variable was a key in another dictionary, which clearly had no value so was 
  malformed. Once I noticed that, I immediately removed them, and voila! Worked like a 
  charm.

  Now that the code update was finished and I had my new stopwatch webhook hash string,
  I edited and redeployed the Slack app. I tested the slash command, and it stopped 
  the stopwatch and added the appropriate amount of minutes to the quantity for 
  today's pixel. Very nice!

### August 9, 2023

**Today's Progress**
* Started Day 38 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [Exercise Tracker](https://github.com/StingzLD/exercise-tracker)

**External Links**
* [Nutritionix](https://nutritionix.com/)

**Thoughts**
* So far there is nothing crazy about this project, just more API calls. I did not get 
  terribly far into it today, though. That is mainly due to the fact that I ended up 
  creating a webhook in Slack for the Pixela Stopwatch! Now I can see exactly how long I 
  am coding for. No more guessing!

### August 8, 2023

**Today's Progress**
* Completed Day 37 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [Habit Tracker](https://github.com/StingzLD/habit-tracker)

**External Links**
* [Pixela](https://pixe.la/)

**Thoughts**
* I never really thought about the pixel graph on my GitHub page as being a "habit" 
  tracker, but it most definitely is. Now whether they made it first, or Pixela did 
  and GitHub just thought it was a great idea and implemented it, is something I am 
  curious about. Either way, implementing my own version of it is pretty cool. 
  Naturally, though, just doing the minimum amount of work was not enough for me. 
  Having a bunch of commented out code that you then need to uncomment specific 
  sections to use it is just messy and a nightmare to work with. So what did I do? 
  Make it user-friendly, of course! There is more I could add, and I probably will do 
  so, but converting everything into functions, having it prompt the user for actions 
  and inputs, and having it loop until the user is done making changes is really nice. 
* In looking further at the documentation, I see that there is a stopwatch API, as well, 
  which will start the stopwatch on the first request. The second request will stop 
  the stopwatch, as well as update that day's pixel. What is really neat is the fact 
  that when it updates, it actually adds to the existing value for that day. This 
  is really nice and much better than having to manually add the values together and 
  update the pixel accordingly. I will probably work on this functionality tomorrow, 
  so I can keep track of just how much time I am actually spending on these projects. 
  My guess is way more than I really have time for. 

### August 7, 2023

**Today's Progress**
* Completed Day 36 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [Stock News](https://github.com/StingzLD/stock-news)

**External Links**
* [Alpha Vantage (Stock Maret API)](https://www.alphavantage.co/)
* [News API](https://newsapi.org/)
* [Twilio](https://twilio.com/)

**Thoughts**
* Although the stock market does not really interest me, I found the API for acquiring 
  news articles kind of intriguing. I do not necessarily have any use for it at the 
  moment, but the possibilities for querying anything you are interested in are 
  seemingly endless. My dad has been wanting to get into the stock market, though, so 
  this whole app could actually be of use in the near future. I need to look further 
  at the API's documentation, but it would be nice to be able to retrieve stock data 
  for multiple stocks using a single GET call.

### August 6, 2023

**Today's Progress**
* Completed Day 35 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [SMS Rain Alert](https://github.com/StingzLD/sms-rain-alert)

**External Links**
* [OpenWeather API](https://openweathermap.org/api)
* [Latitude and Longitude Finder](https://www.latlong.net/)
* [Ventusky (high resolution live weather map)](https://www.ventusky.com/)
* [Online JSON Viewer](https://jsonviewer.stack.hu/)
* [PythonAnywhere](https://www.pythonanywhere.com/)
* [Twilio](https://twilio.com/)

**Thoughts**
* This is the first time that I have ever sent SMS messages from a script, so this was 
  a lot of fun to finish. I did not realize how cheap it is, either. A mere $0.0079 
  per message for the Pay-as-You-Go plan! I am on a free trial with $15.00 worth of 
  credits, where $1.50 of that goes to the number, leaving $13.50 for messages. If you 
  do the math, that is a LOT of messages, so much so that this particular app could 
  notify me that it is raining every single day for 4.5 years before it runs out of 
  credits. That is insane! I think I might be using SMS for more projects in the 
  future. PythonAnywhere is running the script every day at 6:00 AM, but this is the 
  only task that can run on the free plan, so I will either have pay the $5/month to 
  get up to 20 tasks, or I will just need to host my own server. I have a hosting plan 
  already with one domain still available to use, so perhaps I will use that to run 
  cron jobs and web apps. Either way, this was a lot of fun to learn and play with.

### August 5, 2023

**Today's Progress**
* Started Day 35 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [SMS Rain Alert](https://github.com/StingzLD/sms-rain-alert)

**External Links**
* [OpenWeather API](https://openweathermap.org/api)
* [Latitude and Longitude Finder](https://www.latlong.net/)
* [Ventusky (high resolution live weather map)](https://www.ventusky.com/)
* [Online JSON Viewer](https://jsonviewer.stack.hu/)

**Thoughts**
* Moving at my own pace and not having to be stressed about trying to complete everything
  in one day has been pretty nice. As you will see in the code, there is not a lot of 
  lines of code, however the time I spent playing with it, analyzing the data returned 
  from the API, and determining which way I ultimately wanted to parse through everything 
  took a good chunk of time. Add to that the fact that the API key was not readily 
  available to use (it took some time to propagate), and then once that was working, 
  it took a similar amount of time for the subscription to activate. Needless to say, 
  I spent a good couple of hours working (playing) on this project, and there is still 
  more to be done. The fact that I am not super stressed about having to come back and 
  finish all of this before the end of the day is pretty nice.
* Now for my thoughts on the work done today, which is really what you are interested 
  in. Playing with the OpenWeather API was a lot of fun, especially since I am very 
  interested in all things weather (kind of hard not to be when you live in Texas and 
  are constantly watching the sky during tornado season!). I think once this little 
  app is complete, I will be using this API in different projects. The Ventusky app 
  was so interesting that I actually downloaded it onto my phone, as it is really neat.
  One tool that is going to be really useful for almost every project involving APIs 
  moving forward is going to be the Online JSON Viewer. That is such a slick tool, and 
  I wish that functionality was a plugin I could readily use in PyCharm (or any other 
  IDE for that matter). It made sifting through the massive amount of weather data 
  incredibly easy.

### August 4, 2023

**Today's Progress**
* Completed Day 34 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
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

### January 12, 2023

**Today's Progress**
* Completed Day 32 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)
* Completed Day 33 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
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

### January 11, 2023

**Today's Progress**
* Completed Day 31 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
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

### January 10, 2023

**Today's Progress**
* Completed Day 30 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
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

### January 9, 2023

**Today's Progress**
* Continued developing Password Manager from Day 29 of the  
  [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
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

### January 8, 2023

**Today's Progress**
* Completed Day 29 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
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

### January 7, 2023

**Today's Progress**
* Completed Day 28 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [Pomodoro Timer](https://github.com/StingzLD/pomodoro-timer)

**Thoughts**
* The Pomodoro Timer is a project that is something I can actually use, as it sets a clock
  and runs based on the Pomodoro Technique. The technique, along with screenshots, is 
  shown in the README.md file in the above repo on GitHub. This project is something I am 
  going to take and run with on another project, as pretty much every element in this 
  project can be used for another timer I am wanting to make. Good stuff!

### January 6, 2023

**Today's Progress**
* Completed Day 27 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [Miles to Kilometers Converter](https://github.com/StingzLD/mi-to-km-converter)
* [Tkinter Widget Demo](https://github.com/StingzLD/tkinter-widget-demo)
* [Day 27 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-27)

**Thoughts**
* It's a... GUI! One of the things that I have really wanted to get into is designing a 
  graphical user interface. I have had a couple of ideas in mind in the past, but I 
  never spent the time to actually learn how to do it. With today's coding, finally got to
  start that journey of learning how to do it. And now that I have the basics down, I can
  create essentially whatever basic application's GUI I want.

### January 5, 2023

**Today's Progress**
* Completed Day 26 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [NATO Alphabet Generator](https://github.com/StingzLD/nato-alphabet-generator)
* [Pandas Exercise 7](https://replit.com/@StingzLD/pandas-exercises#exercise-7.py)
* [Day 26 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-26)

**Thoughts**
* Any day you get to learn something new is a great day, and today was a great day. Up to 
  now, I have only dealt with list comprehensions, but never dictionary comprehensions. I 
  did not even know those existed! And to add a cherry on top, I got to work with pandas 
  DataFrames data using the dictionary comprehension. So all-in-all, it was a great day.

### January 4, 2023

**Today's Progress**
* Completed Day 25 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [Name the States Game](https://github.com/StingzLD/us-states-game)
* [Pandas Exercises](https://replit.com/@StingzLD/pandas-exercises)

**Thoughts**
* The 'Name the States' game was a nice introduction into the pandas module. It
  combined the CSV parsing with the turtle module to create a game that worked well for
  both. As always, I think there is a way to improve upon the game, but the current
  iteration of it definitely works. What I would like to add, though, is a way to click
  on a state and then see if you answer it correctly.

### January 3, 2023

**Today's Progress**
* Completed Day 24 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
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

### January 2, 2023

**Today's Progress**
* Completed Day 23 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
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

### January 1, 2023

**Today's Progress**
* Completed Day 22 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
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

### December 31, 2022

**Today's Progress**
* Completed Day 21 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [Snake Game](https://github.com/StingzLD/snake-game)

**Thoughts**
* To finish the snake game, there was still a bit of work to be done. In total, I added 
  a food and scoreboard class, updated the snake class to be able to extend the snake 
  by a segment when it eats an ap=le, and ; updated the main script to include all these 
  changes, as well as add the game over conditions. Overall, the game works just as it 
  should. The only thing that bugs me is the placement of the apple is not always 
  centered on the snake, so it is a bit awkward at times, but it still works. This is 
  something that can be improved upon in the future, though. See you all in the new year!

### December 30, 2022

**Today's Progress**
* Completed Day 20 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
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

### December 29, 2022

**Today's Progress**
* Completed Day 19 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
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

### December 28, 2022

**Today's Progress**
* Completed Day 18 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
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

### December 27, 2022

**Today's Progress**
* Completed Day 17 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
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

### December 23, 2022

**Today's Progress**
* Completed Day 16 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
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

### December 22, 2022

**Today's Progress**
* Completed Day 15 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [Coffee Machine](https://github.com/StingzLD/coffee-machine/tree/main/old)

**Thoughts**
* Making a coffee machine was a neat little exercise. I had never really thought about 
  making a vending machine style program before, so it was good for my brain to get 
  that experience in.

### December 21, 2022

**Today's Progress**
* Completed Day 14 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [Day 14 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-14)

**Thoughts**
* This was the last lesson labelled as "beginner", so I am excited to finally move 
  past this section. This project was another higher/lower game, just with a twist. 
  Overall, it was still a very simplistic game, though. In fact, I ended up writing 
  the game in half of the lines of code that as the solution code had, as they had 
  made it far more difficult than it needed to be by adding in functions that would 
  never be used more than once. I mean, I get it. They want to showcase everything 
  that has been learned up to this point, but it was truly unnecessary in my opinion.

### December 20, 2022

**Today's Progress**
* Completed Day 12 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)
* Completed Day 13 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
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

### December 19, 2022

**Today's Progress**
* Completed Day 11 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
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

### December 18, 2022

**Today's Progress**
* Started Day 11 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [Blackjack](https://github.com/StingzLD/blackjack)

**Thoughts**
* Today was working on the first capstone of the course: Blackjack. I did not get 
  nearly as much completed as I wanted to, so I will have to pick it back up tomorrow 
  and play catch up.


### December 17, 2022

**Today's Progress**
* Completed Day 10 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [Day 10 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-10)
* [Calculator](https://github.com/StingzLD/calculator)

**Thoughts**
* This was the first time I was tasked with making a calculator. Although it was 
  simplistic, as the arithmetic is built-in to Python already, it is always nice to 
  create something that is actually useful.

### December 16, 2022

**Today's Progress**
* Completed Day 9 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [Day 9 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-9)

**Thoughts**
* Today's part of the course was definitely only geared towards learning a building 
  block of Python, one that I am definitely familiar with. As such, there was nothing 
  for me to learn today. But of course, it is always good to get some practice in to 
  keep it fresh in your mind.

### December 15, 2022

**Today's Progress**
* Completed Day 8 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [Day 8 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-8)
* [Caesar Cipher](https://github.com/StingzLD/caesar-cipher)

**Thoughts**
* Sadly, there was nothing new with today's work, as I have already created Caesar 
  Cipher scripts before. However, it was a good refresher on the topic.

### December 14, 2022

**Today's Progress**
* Completed Day 7 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
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

### December 13, 2022

**Today's Progress**
* Completed Day 6 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [Day 6 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-6)

**Thoughts**
* I always love games, so adding [Reeborg's World](https://reeborg.ca/reeborg.html) to 
  the course was fun. I had actually never seen a "jumping hurdles" or "maze" 
  challenge before, so although easy to solve, it was still much more enjoyable than 
  your usual while loop exercises. This is something I will probably end up showing to 
  the kids when they want to move on from blockly and start learning Python.

### December 12, 2022

**Today's Progress**
* Completed Day 5 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [Day 5 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-5)
* [Password Generator](https://github.com/StingzLD/password-generator)

**Thoughts**
* Today's project was actually a pretty beneficial one, as it is something I use on a 
  regular basis for my job: A Password Generator. The general creation of the tool may 
  not have been very complex, however I did end up searching for and finding a new 
  method I have never used before: Shuffle. I have never had a need to shuffle a list 
  before, so it was pretty nifty to learn something new. I am definitely going to 
  continue to refine this password generator and cater it towards my exact needs.

### December 11, 2022

**Today's Progress**
* Completed Day 4 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
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

### December 10, 2022

**Today's Progress**
* Completed Day 3 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [Day 3 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-3)

**Thoughts**
* The project for today might have been a simplistic one, but it was definitely fun and 
  got the creative juices flowing. It was a *Choose Your Own Adventure* game called 
  **Treasure Island**. If you want to take a peek at it, just head hit the Replit link 
  above and take a look at the treasure-island.py file.

### December 9, 2022

**Today's Progress**
* Completed Day 2 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
* [Day 2 - Replit](https://replit.com/@StingzLD/100DaysOfPython-Day-2)

**Thoughts**
* Although this course is still in the very basics, I have decided to just go through 
  the motions, as there may be a piece of information I did not know or a trick that I 
  might learn. Either way, Day 2 complete!

### December 8, 2022

**Today's Progress**
* Completed Day 1 of the [100 Days of Code: The Complete Python Pro Bootcamp for 2023
](https://www.udemy.com/course/100-days-of-code/)

**Link to Work**
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
