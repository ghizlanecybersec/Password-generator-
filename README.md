import random
import string

print("welcome to the password generator ")

length=input("enter the total number characters in the password :\n")
length_password1=int(length)
letters=int(input("enter the number of letters in the password :\n"))
numbers=int(input("enter the number of numbers in the password:\n"))
symbols=int(input("enter the number of symbols in the password:\n"))

random_1=random.choices(string.ascii_letters,k=letters)
random_2=random.choices(string.digits,k=numbers)
random_3=random.choices(string.punctuation,k=symbols)

passwords=random_1+random_2+random_3

length_password2=len(passwords)

if length_password1==length_password2:
    random.shuffle(passwords)
    password_generator="".join(passwords)
    print("password generator:",password_generator)
else:
    print("invalid input the sum of letters , numbers ,and symbols doesn't match the password")


    
