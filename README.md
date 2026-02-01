# Ved-S.-Patel-Assignment-4
Files, Exceptions, and Errors in Python
# Task 1
try:
    with open('sample.txt', 'r') as file:
        for line in file:
            print(line, end='')
except FileNotFoundError:
    print("Error: The file 'sample.txt' was not found.")
except IOError:
    print("Error: An error occurred while reading the file.")

# Task 2
try:
    user_input = input("Enter data to write to output.txt: ")
    with open('output.txt', 'w') as file:
        file.write(user_input + '\n')
    print("Data written successfully.")

    append_input = input("Enter data to append to output.txt: ")
    with open('output.txt', 'a') as file:
        file.write(append_input + '\n')
    print("Data appended successfully.")

    with open('output.txt', 'r') as file:
        print("\nFinal content of output.txt:")
        print(file.read())
        
except IOError:
    print("Error: An error occurred while handling the file.")
