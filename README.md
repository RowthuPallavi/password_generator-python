# password_generator-python
Random Password Generator using Python
import random
import string

def generate_random_password(length=8):
    # Define characters to use in the password
    characters = string.ascii_letters + string.digits + string.punctuation

    # Filter out characters that might be confusing in a password (optional)
    filtered_characters = ''.join(c for c in characters if c not in '"\'`|\\')

    # Generate the password randomly
    password = ''.join(random.choice(filtered_characters) for _ in range(length))
    return password

if __name__ == "__main__":
    # Set the desired length for the password
    password_length = 8

    # Generate and print the random password
    password = generate_random_password(password_length)
    print("Random Password:", password)
