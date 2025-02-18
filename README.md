import random
import string

# Function to generate a random password
def generate_password(length):
    # Define the character sets for password generation
    all_characters = string.ascii_letters + string.digits + string.punctuation
    
    # Ensure the password length is at least 1
    if length < 1:
        print("Password length must be at least 1.")
        return
    
    # Generate the password using random.choices() to select characters
    password = ''.join(random.choices(all_characters, k=length))
    
    return password

# Main program
def main():
    # Prompt the user to enter the desired password length
    length = int(input("Enter the desired password length: "))
    
    # Generate the password
    password = generate_password(length)
    
    # Display the generated password
    print(f"Generated Password: {password}")

if __name__ == "__main__":
    main()
