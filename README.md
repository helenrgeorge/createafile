# createafile
# Creates a file or writes to an existing file

import os #import the OS library

# prompt user for file name and directory

filePath = input('Where do you want to save your file?: ') 
fileName = input('What do you want to name your file?: ')


completePath = filePath+fileName

# check if file already exist

if os.path.exists(completePath): 
    print("File already exist")
else:
    print("Creating new file")

# take input from user

name = input('What is your name? ')
address = input('What is your address? ')
phonen = input('What is your phone number? ')

# write input to file

with open(completePath, "w") as file_object:
    file_object.write(name)
    file_object.write(", ")
    file_object.write(address)
    file_object.write(", ")
    file_object.write(phonen)
   
# read file

with open(completePath, "r") as file_object:
    newfile = file_object.read()
    
# print file

print("Please confirm that the following information is correct: ")
print(newfile)
