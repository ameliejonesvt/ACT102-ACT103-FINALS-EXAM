 # ==========================================================
#                  CHRONOBYTE
#              THE LAST CODE STANDING
# ==========================================================

# GAME VARIABLES
player_name = ""
lives = 3
score = 0
correct_answers = 0
wrong_answers = 0
game_running = True
played_lessons = ","

print("====================================================")
print("                  CHRONOBYTE")
print("              THE LAST CODE STANDING")
print("====================================================")
print("A corrupted computer system has taken over the world.")
print("Restore it by answering programming questions!")
print("\nREACH 100 POINTS TO WIN!")
print("LOSE ALL 3 LIVES AND YOU LOSE!")
print("Each lesson can only be played once.")
print("====================================================")

player_name = input("\nEnter your player name: ")

print("\nWelcome to CHRONOBYTE,", player_name, "!")
print("You have 3 lives. Choose your lessons wisely!")

# MAIN GAME
while game_running == True and lives > 0 and score < 100:

    print("\n================ MAIN MENU ================")
    print("PLAYER:", player_name)
    print("SCORE:", score, "/ 100")
    print("LIVES LEFT:", lives)
    print("[1] PRELIMINARY CHAPTERS")
    print("[2] MIDTERM CHAPTERS")
    print("[3] FINALS CHAPTERS")
    print("[0] EXIT GAME")

    chapter = input("\nChoose a chapter: ")

    # PRELIMINARY
    if chapter == "1":

        print("\n========== PRELIMINARY CHAPTERS ==========")
        print("[1] Introduction to Programming")
        print("[2] Python Basic Syntax")
        print("[3] Printing Output")
        print("[4] Variables, Constants, and Data Types")
        print("[5] Basic Data Types in Python")
        print("[6] Arithmetic Operators and Expressions")
        print("[7] Basic Input and Output in Python")
        print("[0] Back to Main Menu")

        lesson = input("\nChoose your lesson: ")

        if lesson == "0":
            continue
        elif lesson == "1":
            lesson_name = "INTRODUCTION TO PROGRAMMING"
        elif lesson == "2":
            lesson_name = "PYTHON BASIC SYNTAX"
        elif lesson == "3":
            lesson_name = "PRINTING OUTPUT"
        elif lesson == "4":
            lesson_name = "VARIABLES, CONSTANTS, AND DATA TYPES"
        elif lesson == "5":
            lesson_name = "BASIC DATA TYPES IN PYTHON"
        elif lesson == "6":
            lesson_name = "ARITHMETIC OPERATORS AND EXPRESSIONS"
        elif lesson == "7":
            lesson_name = "BASIC INPUT AND OUTPUT IN PYTHON"
        else:
            print("Invalid lesson selection!")
            continue

    # MIDTERM
    elif chapter == "2":

        print("\n========== MIDTERM CHAPTERS ==========")
        print("[8] Conditional Statements in Python")
        print("[9] Logical Operators")
        print("[0] Back to Main Menu")

        lesson = input("\nChoose your lesson: ")

        if lesson == "0":
            continue
        elif lesson == "8":
            lesson_name = "CONDITIONAL STATEMENTS IN PYTHON"
        elif lesson == "9":
            lesson_name = "LOGICAL OPERATORS"
        else:
            print("Invalid lesson selection!")
            continue

    # FINALS
    elif chapter == "3":

        print("\n========== FINALS CHAPTERS ==========")
        print("[10] Introduction to Iteration and Loops")
        print("[0] Back to Main Menu")

        lesson = input("\nChoose your lesson: ")

        if lesson == "0":
            continue
        elif lesson == "10":
            lesson_name = "INTRODUCTION TO ITERATION AND LOOPS"
        else:
            print("Invalid lesson selection!")
            continue

    elif chapter == "0":
        print("\nThank you for playing CHRONOBYTE!")
        game_running = False
        break

    else:
        print("\nInvalid chapter selection!")
        continue

    # CHECK COMPLETED LESSONS
    if "," + lesson + "," in played_lessons:
        print("\nYou have already completed this lesson!")
        print("Please choose another topic.")
        continue

    # LESSON CHALLENGE
    print("\n====================================================")
    print("                 LESSON CHALLENGE")
    print("====================================================")
    print("Selected Lesson:", lesson_name)
    print("Player:", player_name)
    print("Lives Available:", lives)
    print("Answer 2 questions to complete this lesson.")

    question_number = 1

    while question_number <= 2 and lives > 0 and score < 100:

        question = ""
        option_a = ""
        option_b = ""
        option_c = ""
        correct_answer = ""
        explanation = ""

        # LESSON 1
        if lesson == "1":

            if question_number == 1:
                question = "What is programming?"
                option_a = "A. Giving instructions to a computer"
                option_b = "B. Playing computer games"
                option_c = "C. Watching videos"
                correct_answer = "A"
                explanation = "Programming means writing instructions that a computer can follow."

            else:
                question = "What is the main purpose of a program?"
                option_a = "A. To decorate a computer"
                option_b = "B. To perform a specific task"
                option_c = "C. To increase screen brightness"
                correct_answer = "B"
                explanation = "A program is created to make a computer perform specific tasks."

        # LESSON 2
        elif lesson == "2":

            if question_number == 1:
                question = "Which character is used for a comment in Python?"
                option_a = "A. //"
                option_b = "B. #"
                option_c = "C. **"
                correct_answer = "B"
                explanation = "The # symbol is used to write a single-line comment in Python."

            else:
                question = "Which is a correct Python statement?"
                option_a = "A. print('Hello')"
                option_b = "B. print 'Hello'"
                option_c = "C. display('Hello')"
                correct_answer = "A"
                explanation = "Python uses print() to display information."

        # LESSON 3
        elif lesson == "3":

            if question_number == 1:
                question = "What is the output of print('Hello World')?"
                option_a = "A. Hello"
                option_b = "B. World"
                option_c = "C. Hello World"
                correct_answer = "C"
                explanation = "The print() statement displays the text inside its parentheses."

            else:
                question = "Which statement displays the number 25?"
                option_a = "A. print(25)"
                option_b = "B. input(25)"
                option_c = "C. number(25)"
                correct_answer = "A"
                explanation = "print(25) displays the number 25 on the screen."

        # LESSON 4
        elif lesson == "4":

            if question_number == 1:
                question = "What is a variable in Python?"
                option_a = "A. A value that can be changed"
                option_b = "B. A computer monitor"
                option_c = "C. A programming error"
                correct_answer = "A"
                explanation = "A variable stores a value that can be changed during a program."

            else:
                question = "What is a constant?"
                option_a = "A. A value that changes every second"
                option_b = "B. A value intended to remain unchanged"
                option_c = "C. A type of loop"
                correct_answer = "B"
                explanation = "A constant represents a value intended to stay the same."

        # LESSON 5
        elif lesson == "5":

            if question_number == 1:
                question = "Which data type is used for whole numbers?"
                option_a = "A. str"
                option_b = "B. int"
                option_c = "C. bool"
                correct_answer = "B"
                explanation = "int is used for whole numbers such as 10, 25, and 100."

            else:
                question = "Which data type stores text?"
                option_a = "A. str"
                option_b = "B. float"
                option_c = "C. int"
                correct_answer = "A"
                explanation = "str means string, which is used to store text."

        # LESSON 6
        elif lesson == "6":

            if question_number == 1:
                question = "What is the result of 10 + 5?"
                option_a = "A. 15"
                option_b = "B. 50"
                option_c = "C. 5"
                correct_answer = "A"
                explanation = "The + operator adds two numbers. 10 + 5 = 15."

            else:
                question = "Which operator is used for multiplication?"
                option_a = "A. /"
                option_b = "B. *"
                option_c = "C. -"
                correct_answer = "B"
                explanation = "The * symbol is the multiplication operator in Python."

        # LESSON 7
        elif lesson == "7":

            if question_number == 1:
                question = "Which function receives information from the user?"
                option_a = "A. print()"
                option_b = "B. input()"
                option_c = "C. output()"
                correct_answer = "B"
                explanation = "input() allows the user to enter information."

            else:
                question = "What is the purpose of print()?"
                option_a = "A. To receive user information"
                option_b = "B. To delete information"
                option_c = "C. To display information"
                correct_answer = "C"
                explanation = "print() displays text, values, and results on the screen."

        # LESSON 8
        elif lesson == "8":

            if question_number == 1:
                question = "Which statement checks whether a condition is true?"
                option_a = "A. if"
                option_b = "B. print"
                option_c = "C. input"
                correct_answer = "A"
                explanation = "An if statement checks a condition before executing code."

            else:
                question = "What is the purpose of else?"
                option_a = "A. To repeat a statement"
                option_b = "B. To run code when the if condition is false"
                option_c = "C. To receive input"
                correct_answer = "B"
                explanation = "The else block runs when the if condition is false."

        # LESSON 9
        elif lesson == "9":

            if question_number == 1:
                question = "Which logical operator requires both conditions to be true?"
                option_a = "A. or"
                option_b = "B. not"
                option_c = "C. and"
                correct_answer = "C"
                explanation = "The and operator returns True only when both conditions are true."

            else:
                question = "Which operator returns True if at least one condition is true?"
                option_a = "A. or"
                option_b = "B. and"
                option_c = "C. not"
                correct_answer = "A"
                explanation = "The or operator returns True when at least one condition is true."

        # LESSON 10
        elif lesson == "10":

            if question_number == 1:
                question = "What is the purpose of a loop?"
                option_a = "A. To stop a computer"
                option_b = "B. To repeat a block of code"
                option_c = "C. To delete a variable"
                correct_answer = "B"
                explanation = "Loops repeat a block of code while following their conditions."

            else:
                question = "Which loop continues while its condition is true?"
                option_a = "A. while loop"
                option_b = "B. print loop"
                option_c = "C. input loop"
                correct_answer = "A"
                explanation = "A while loop repeats its code as long as its condition is true."

        # DISPLAY QUESTION
        print("\n----------------------------------------------------")
        print("QUESTION", question_number, "OF 2")
        print(question)
        print(option_a)
        print(option_b)
        print(option_c)

        answer = input("\nEnter your answer (A/B/C): ").upper()

        # CHECK ANSWER
        if answer == correct_answer:

            print("\nCORRECT ANSWER!")
            print("You earned 10 points!")
            print("Explanation:", explanation)

            score = score + 10
            correct_answers = correct_answers + 1

        else:
            print("\nWRONG ANSWER!")
            print("Correct answer:", correct_answer)
            print("Explanation:", explanation)

            lives = lives - 1
            wrong_answers = wrong_answers + 1

        # PLAYER STATUS
        print("\n========== PLAYER STATUS ==========")
        print("Player:", player_name)
        print("Score:", score)
        print("Lives Remaining:", lives)
        print("Correct Answers:", correct_answers)
        print("Wrong Answers:", wrong_answers)
        print("===================================")

        if score >= 100:
            print("\nYOU REACHED 100 POINTS!")
            print("YOU WIN!")
            break

        elif lives <= 0:
            print("\nYOU HAVE RUN OUT OF LIVES!")
            print("YOU LOSE!")
            break

        question_number = question_number + 1

    # LESSON RESULT
    if lives > 0 and score < 100:

        if question_number > 2:

            played_lessons = played_lessons + lesson + ","

            print("\n========== LESSON COMPLETED! ==========")
            print("Congratulations,", player_name + "!")
            print("You completed:", lesson_name)
            print("This lesson can no longer be selected.")
            print("Your current score:", score)
            print("Your remaining lives:", lives)
            print("You may now choose another lesson.")

# GAME RESULTS
print("\n====================================================")
print("                  GAME SUMMARY")
print("====================================================")
print("PLAYER NAME:", player_name)
print("FINAL SCORE:", score)
print("CORRECT ANSWERS:", correct_answers)
print("WRONG ANSWERS:", wrong_answers)
print("LIVES LEFT:", lives)

if score >= 100:

    print("\n          CONGRATULATIONS!")
    print("          YOU ARE THE WINNER!")
    print("You successfully restored the corrupted system!")
    print("You reached 100 points!")
    print("ENDING: THE HERO OF CHRONOBYTE")

elif lives <= 0:

    print("\n               GAME OVER!")
    print("              YOU LOST!")
    print("NULL has taken over the system.")
    print("You ran out of lives before reaching 100 points.")
    print("ENDING: THE ERA OF NULL")

else:

    print("\n              GAME EXITED")
    print("You decided to leave the game.")

print("\nTHANK YOU FOR PLAYING CHRONOBYTE!")
print("====================================================")
