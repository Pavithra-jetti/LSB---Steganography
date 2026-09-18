Image Steganography in C
Overview

This project is a command-line Image Steganography tool developed in C. It allows users to hide (encode) a secret file inside a BMP image and later retrieve (decode) it, using LSB (Least Significant Bit) encoding.

The project demonstrates the practical use of structures, file handling, bitwise operations, pointers, and enums in C, along with modular, header-based program design.

Features
Encode a secret file into a BMP image
Decode and extract the hidden secret file from a stego image
Verifies BMP image capacity before encoding
Uses a magic string to confirm a valid stego image during decoding
Preserves secret file extension during encode/decode
Color-coded console output for success/failure messages
Command-line argument–driven operation (-e for encode, -d for decode)
Technologies Used
Programming Language: C
Compiler: GCC
Platform: Linux / Windows
Concepts: Structures, Enums, Pointers, File Handling, Bitwise (LSB) Operations, Modular Programming
Libraries: stdio.h, string.h
Project Structure
text
Image-Steganography-in-C/
│
├── main.c
├── encode.c
├── encode.h
├── decode.c
├── decode.h
├── common.h
├── types.h
├── colors.h
├── beautiful.bmp
├── secret.txt
├── README.md
└── .gitignore
File Description
File	Description
main.c	Program entry point; parses arguments and triggers encode/decode
encode.c	Core encoding logic — hides secret file data inside the BMP image
encode.h	EncodeInfo structure definition and encoding function declarations
decode.c	Core decoding logic — extracts hidden data from the stego image
decode.h	DecodeInfo structure definition and decoding function declarations
common.h	Shared definitions, including the magic string used to validate images
types.h	User-defined types (Status, OperationType, uint)
colors.h	Terminal color codes for formatted console output
beautiful.bmp	Sample source BMP image used for encoding
secret.txt	Sample secret file to be hidden inside the image
README.md	Project documentation
.gitignore	Specifies generated files that should not be uploaded to GitHub
How to Run
1. Clone the Repository

Open Command Prompt / Terminal and run:

bash
git clone <your-github-repository-link>
2. Open the Project Directory
bash
cd Image-Steganography-in-C
3. Compile the Program
bash
gcc main.c encode.c decode.c -o a.out
4. Run the Program

To encode a secret file into an image:

bash
./a.out -e beautiful.bmp secret.txt

To decode a secret file from an image:

bash
./a.out -d beautiful.bmp
Run

After compiling, the program is operated entirely through command-line arguments:

text
Encoding: ./a.out -e <source.bmp> <secret_file> [output.bmp]
Decoding: ./a.out -d <stego.bmp> [output_file]

The tool encodes a magic string, the secret file's extension, its size, and its data (bit by bit) into the BMP's LSBs, and reverses this process to decode.

Learning Outcomes
Gained practical knowledge of file-format–level programming (BMP headers)
Learned how bitwise LSB manipulation can be used for data hiding
Practiced structuring a multi-file C project with separate .c/.h modules
Improved understanding of pointers, structures, and enums in C
Learned command-line argument parsing and validation
Practiced error handling across multi-stage operations (encode/decode pipelines)
Improved debugging and problem-solving skills
Author

Pavithra Jetti
