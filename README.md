import os
def modify_file(input_filename, output_filename):
"""
Reads a file, modifies each line by adding a line number,
and writes the modified content to a new file. Handles
potential file_related errors.'""
try:
with open(input_filename, 'r')as infile,open(output_filename, 'w') as outfile:
for i, line in enumerate(infile):
modified_line=f"{i+1}: {line}"
outfile.write(modified_line)
print(f"successfully modified '{input_filename}' and wrote to '{output_filename}'")
except FileNotFoundError:
print(f"Error: The file '{input_filename}' was not found.")
except Exception as e:
print(f"An unexpectederror occured:{e}")


def main():
"""
prompts the user for an input filename,output filename,
and calls the modify_file function to process the files.

"""
input_filename=input("Enter the input filename: ")
output_filename=input("Enter the output filename:  ")
modify_file(input_filename, output_filename)
if_name_=="'_main_":

main()
