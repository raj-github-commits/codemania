# The task is to create a "Health Management System." Suppose you are a fitness trainer and nutritionist. You
# have to deal with three clients, i.e., (Harry, Rohan, Hammad). For each client, you have to design their
# exercise and diet plan.
# Instructions:
# Create a food log file for each client
# Create an exercise log file for each client.
# Ask the user whether they want to log or retrieve client data.
# Write a function that takes the user input of the client's name. After the client's name is entered, A
# message should display "What you want to log. Diet or Exercise"
# Use function
# The purpose of this function is to give time with every record of food or exercise added in the file.
# Write a function to retrieve exercise or food file records for any client.
# You are advised to participate in solving this problem. This task helps you become a good problem solver and
# enables you to accept the challenge and acquire new skills.
# Keep supporting and stay up to date with codewithharry.



# Create 6 files of respective names first

def getdate():
    import datetime
    return datetime.datetime.now()

import datetime
def gettime():
    return datetime.datetime.now()

def take(k):
    if k == 1:
        c = int(input("Enter 1 for exercise and 0 for food: "))
        if (c == 1):
            value = input("type here\n")
            f = open("exercise log for Harry", "a")
            f.write(str([str(gettime())]) + ":" + value +  "\n")
            print("succesfully entered")

        elif (c == 0):
            value = input("type here\n")
            f = open("food_ log_ for_Harry", "a")
            f.write(str([str(gettime())]) + ":" + value + "\n")
            print("succesfully entered")

    elif k == 2:
        c = int(input("Enter 1 for exercise 0 for food: "))
        if (c == 1):
            value = input("type here\n")
            f = open("exercise log for Rohan", "a")
            f.write(str([str(gettime())]) + ":" + value + "\n")
            print("succesfully entered")

        elif (c == 0):
            value = input("type here\n")
            f = open("food log for Rohan", "a")
            f.write(str([str(gettime())]) + ":" + value + "\n")
            print("succesfully entered")

    elif k == 2:
        c = int(input("Enter 1 for exercise 0 for food: "))
        if (c == 1):
            value = input("type here\n")
            f = open("exercise log for Hammad", "a")
            f.write(str([str(gettime())]) + ":" + value + "\n")
            print("succesfully entered")

        elif (c == 0):
            value = input("type here\n")
            f = open("food log for Hammad", "a")
            f.write(str([str(gettime())]) + ":" + value + "\n")
            print("succesfully entered")

def retrieve(k):
    if k == 1:
        c = int(input("Enter 1 for exercise 0 for food: "))
        if (c == 1):
            f = open("exercise log for Harry")
            for i in f:
                print(i, end="")

        elif (c == 0):
            f = open("food_ log_ for_Harry")
            for i in f:
                print(i, end="")

    elif k == 2:
        c = int(input("Enter 1 for exercise 0 for food: "))
        if (c == 1):
            f = open("exercise log for Rohan")
            for i in f:
                print(i, end="")

        elif (c == 0):
            f = open("food log for Rohan")
            for i in f:
                print(i, end="")

    elif k== 3:
        c = int(input("Enter 1 for exercise 0 for food: "))
        if (c == 1):
            f = open("exercise log for Hammad")
            for i in f:
                print(i, end="")

        elif (c == 0):
            f = open("food log for Hammad")
            for i in f:
                print(i, end="")

    else:
        print("Enter a valid input either Harry, Rohan or Hammad")

print("Welcome to the Health Management System !!!\n")

client = int(input("press 1 to log 0 to retrieve: "))

if client == 1:
    b = int(input("Press 1 for Harry 2 for Rohan 3 for Hammad: "))
    take(b)

elif client == 0:
    b = int(input("Press 1 for Harry 2 for Rohan 3 for Hammad: "))
    retrieve(b)
