import random
import string

def generate_password(length):
    if length < 8:
        print("Password length must be at least 8.")
        return None
    
    uppercase_letters = string.ascii_uppercase
    lowercase_letters = string.ascii_lowercase
    digits = string.digits
    special_characters = string.punctuation

    password = [
        random.choice(uppercase_letters),
        random.choice(lowercase_letters),
        random.choice(digits),
        random.choice(special_characters)
    ]

    remaining_length = length - 4
    all_characters = uppercase_letters + lowercase_letters + digits + special_characters
    password.extend(random.choice(all_characters) for _ in range(remaining_length))

    random.shuffle(password)

    generated_password = ''.join(password)

    return generated_password

if __name__ == "__main__":
    try:
        while True:
            length = int(input("Enter the desired password length: "))
            password = generate_password(length)
            if password:
                print("Generated Password:", password)

                while True:
                    confirm_password = input("Is the password okay? (yes/no): ")
                    if confirm_password.lower() == 'yes':
                        print("Your password is:", password)
                        exit()
                    elif confirm_password.lower() == 'no':
                        break
                    else:
                        print("Please enter 'yes' or 'no'.")
    except ValueError:
        print("Please enter a valid number for password length.")
