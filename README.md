import re

def validate_password(password):
#check if the password has at least 8 character
   if len(password) < 8:
    return False
 # check if the password contains at least one uppercase letters
   if not re.search(r'[A-Z]', password):
       return False
 # check if the password contains at least one lowercase letter
   if not re.search(r'[a-z]', password):
         return False
# check if the password contain at least one digit
   if not re.search(r'\d', password):
         return False
# check if the password contain at least one special charachter
   if not re.search(r'[!@#$%^&*()<>,./?{}]', password ):
       return False
# if all the condition are met , the password is valid
   return True

password = input( " Input your password: ")
is_valid = validate_password(password)

if is_valid:
    print(" Valid Password.")
else:
     print("Password does not meet requirements.")
