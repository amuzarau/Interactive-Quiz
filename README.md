# Interactive-Quiz
This is my educational project, based on Joe Marini LinkedIn course

This app is quiz-taking program. The program will run in the terminal and present the user with a menu to control the app. The user can list available quizzes, select the quiz, answer the questions, then see the results and save them to txt-file. The quizzes themselves will be defined using XML – structured data  format, which means we can create and edit quizzes without having to change the code of the app. 

First, to run app, you have to right-click on pyquiz.py file and run application in terminal. When you open the quiz, there is simple start-up  greeting and you are prompted for your name. You put your name in, and then you can see,  that program prints out the menu of options:

(M): Repeat this menu
(L): List quizzes
(T): Take a quiz
(E): Exit program

You can repeat this menu, list the quizzes that are installed, take the quiz or exit the program.
In quizzes, there are two types of questions:  multiple choice – questions and True / False – questions.

After you’ve completed the quiz, you get  your  results, including current date and time, how many questions were in test and how many questions you have answered correctly and total score out of possible one.  After that, you are prompted to save your results in separate txt-file, which you can find  later  in the  program files folder

In this app, following higher-level features are realized: 
1. New quizzes can be added without changing code
2. Quiz results (score, number of correct questions, etc.) are tracked and presented to the user
3. Quiz results can be saved in a file.  

Application architecture is realized with help of classes (Object-Oriented Programming), which will help to keep its code  maintainable and extensible: 

1. The main Quiz App class will be responsible for presenting and controlling the user experience of the app. It will handle the menu selections  and instantiate Quiz Manager class. 

2. The Quiz Manager class will be responsible for managing the installed quizzes in the app. It will coordinate user actions in the main app class and installed quizzes. It will also create QuizParser class, which will handle the process of taking XML-file and building Quiz object from it. Each Quiz object will consist of a series of questions and answers. The Quiz class will also be responsible for presenting its own questions  and checking for correct answers each time. Each Quiz object, created by the parser, will be presented to the user by Quiz Manager 

