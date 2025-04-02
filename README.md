# Function to read, modify, and write file content
def modify_file(input_file, output_file):
    try:
        # Open and read the input file
        with open(input_file, 'r') as file:
            content = file.read()
        
        # Modify the content (convert to uppercase in this example)
        modified_content = content.upper()
        
        # Write the modified content to the output file
        with open(output_file, 'w') as file:
            file.write(modified_content)
        
        print(f"Content has been successfully written to {output_file}")
    except FileNotFoundError:
        print(f"Error: The file {input_file} was not found.")
    except Exception as e:
        print(f"An error occurred: {e}")

# Specify the input and output file paths
input_file_path = 'input.txt'  
output_file_path = 'output.txt'  

# Call the function
modify_file(input_file_path, output_file_path)
