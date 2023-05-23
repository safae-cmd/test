<div align="center">
  <img src="hsh-logo.png" alt="hsh - Simple Linux Shell">
</div>

# hsh - Simple Linux Shell

> Your command line companion

hsh is a simple yet powerful Linux shell written in C. It aims to replicate the behavior and error messages of the `/bin/sh` shell, providing a familiar and seamless experience for users.

## Features

- **Interactive Mode**: Execute commands directly within the shell and receive immediate feedback.
- **Non-Interactive Mode**: Run commands from files, allowing for automation and batch processing.
- **Error Handling**: Display clear and concise error messages, mirroring the `/bin/sh` shell for consistency.
- **Command History**: Access previously executed commands using the up and down arrow keys.
- **Customizable**: Extend the shell's functionality by adding your own commands or modifying the existing ones.

## Getting Started

### Prerequisites

- Linux environment
- GCC compiler

### Installation

1. Clone the repository: git clone https://github.com/your-username/hsh.git
2. Compile the shell: gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh 
3. Run the shell in interactive mode: ./hsh
4. Run the shell in non-interactive mode with a command file: ./hsh < commands.txt

## Usage Examples

### Interactive Mode

```shell
$ ./hsh
$ /bin/ls
$ main.c shell.c
$
$ exit
$

### Non-Interactive Mode

$ echo "/bin/ls" | ./hsh
hsh main.c shell.c
$
$ cat commands.txt
/bin/ls
/bin/pwd
$ ./hsh < commands.txt
hsh main.c shell.c
/home/user/project-directory

### Error messages
$ echo "qwerty" | ./hsh
./hsh: 1: qwerty: not found
$ echo "qwerty" | ./././hsh
./././hsh: 1: qwerty: not found

### Contact
For any questions or feedback, please contact [Your Name] at your-email@example.com.
