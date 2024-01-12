# Random-Password-Gen
Creating a random password generator using python. 
#Random Password Generator
import random


numbers = ['1','2','3','4','5','6','7','8','9','0']
letters = ['a','b','c','d','e','f','g','h','i','j','k','l','m','o','p','q','r','s','t','u','v','w','x','y','z']
symbols = ['!','@','#','$','%','(',')']

print("Welcome To The Totally Safe And Cool Password Generator")

nr_letters = int(input('how many letters would you like in your password?\n'))
nr_symbols = int(input(f'How many symbols?\n'))
nr_numbers = int(input(f'How many numbers?\n'))

password_list = []
for char in range(1, nr_letters + 1):
    password_list.append(random.choice(letters))

for char in range(1, nr_symbols + 1):
    password_list.append(random.choice(symbols))

for char in range(1, nr_numbers + 1):
    password_list.append(random.choice(numbers))

random.shuffle(password_list)

password = ""
for char in password_list:
    password += char
print("char", char)

pwd = ''.join(password_list)
print(f"Your random password to use is: {pwd}")
