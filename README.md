# File-Handling-and-Exception-Handling-Assignment
##File Read & Write Challenge

def modify_file(input_filename, output_filename):
    try:
        with open(input_filename, 'r') as infile:
            lines = infile.readlines()

        # Modify the content (example: make all text uppercase)
        modified_lines = [line.upper() for line in lines]

        with open(output_filename, 'w') as outfile:
            outfile.writelines(modified_lines)

        print(f"File has been modified and saved to {output_filename}")
    except FileNotFoundError:
        print("Input file not found.")
    except Exception as e:
        print(f"An error occurred: {e}")

      ##  Error Handling Lab 

        def read_user_file():
    filename = input("Enter the filename to read: ")

    try:
        with open(filename, 'r') as file:
            print("File content:")
            print(file.read())
    except FileNotFoundError:
        print("Error: File not found.")
    except IOError:
        print("Error: File could not be read.")
    except Exception as e:
        print(f"An unexpected error occurred: {e}")
