# Password-generator-project-

import random
import string


# GENRATE PASSWORD...
def password_generator():
    print("Pasword Generetor")

    #Password length
    length = int(input("Enter the password length: "))

    #The complexity of the password
    print("1. Only letters (lowercase and uppercase)")
    print("2. Letters and digits")
    print("3. Letters, digits, and special characters")

    choice = input("Choose complexity level (1, 2, or 3): ")

    #Show complexity level
    if choice == '1':
        characters = string.ascii_letters
    elif choice == '2':
        characters = string.ascii_letters + string.digits
    elif choice == '3':
        characters = string.ascii_letters + string.digits + string.punctuation
    else:
        print("Invalid choice, please select 1, 2, or 3.")
        return

    # Generete password by randomly selecting characters from the set
    password = ''.join(random.choice(characters) for _ in range(length))

    print(f"\nGenerated Password: {password}")


# Call function
password_generator()
