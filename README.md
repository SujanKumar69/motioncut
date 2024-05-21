print("Welcome to my quiz game")
question_bank=[
    {"text":"How many months are there in a year.","answer":"A"},
    {"text":"For how many years leap year occurs.","answer":"B"},
    {"text":"How many days are there in a week.","answer":"D"}
]

options=[["A. Twelve","B. Ten","C. Eleven","D. Thirteen"],
         ["A. Five","B. Four","C. Three","D. Six"],
         ["A. Five","B. Four","C. Six","D. Seven"]]

score=0

def check_answer(user_guess,correct_answer):
    if user_guess==correct_answer:
        return True
    else:
        return False
    

for question_num in range(len(question_bank)):
    print(question_bank[question_num]["text"])
    for i in options[question_num]:
        print(i)
    
    guess=input("Enter your answer(A/B/C/D): ").upper()
    is_correct = check_answer(guess,question_bank[question_num]["answer"])
    if is_correct:
        print("Correct answer")
        score+=1
    else:
        print("Incorrect answer")
        print(f"The correct answer is {question_bank[question_num]['answer']}")
    
print(f"Your final score is {score}")
print(f"Your percentage is {(score/len(question_bank))*100}%")
