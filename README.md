# e-a-Python-program-to-remove-newline-characters-from-a-file.
def remove_newlines(file_path):
    try:
        with open(file_path, 'r') as file:
            lines = file.readlines()

        modified_lines = [line.rstrip('\n') for line in lines]

        with open(file_path, 'w') as file:
            for line in modified_lines:
                file.write(line)

        print("Newline characters removed successfully.")
    except FileNotFoundError:
        print("File not found.")
    except IOError:
        print("An error occurred while accessing the file.")

# Example usage
file_path = 'path/to/your/file.txt'  # Replace with the actual file path
remove_newlines(file_path)

