# ft_pipex

![alt tag](https://github.com/ftTower/ft_pipex/blob/main/errorcmd.png)


## Description

This project implements a program called `pipex` that simulates the behavior of the shell command `< file1 cmd1 | cmd2 > file2`. It takes four arguments: `file1`, `cmd1`, `cmd2`, and `file2`, where `file1` and `file2` are file names, and `cmd1` and `cmd2` are shell commands with their respective parameters.

The program must be executed as follows:
```
./pipex file1 cmd1 cmd2 file2
```

## Examples

### Example 1
```
$> ./pipex infile "ls -l" "wc -l" outfile
```
Should be identical to `< infile ls -l | wc -l > outfile`.

### Example 2
```
$> ./pipex infile "grep a1" "wc -w" outfile
```
Should be identical to `< infile grep a1 | wc -w > outfile`.

![alt tag](https://github.com/ftTower/ft_pipex/blob/main/basic.png)

## Features

- Input/output handling with files and pipes.
- Execution of specified shell commands with their parameters.
- Sensible error handling to avoid unexpected interruptions.
- No memory leaks.
- Multiple pipe handling for bonus points.

## Main Functions

### `pipex`

The main function that directs the program flow by checking for errors, determining whether to execute the rescue command, and calling the appropriate functions.

### `choose_proccess`

Chooses the child or parent process to execute based on the PID returned by the `fork` function.

### `forker`

Creates a new child process to execute a command.

### `bonus`

Implements the bonus functionality for handling multiple pipes.

## Bonus

- Multiple pipe handling.
- Project validated at 115%.

## Compilation

The project is compiled using a Makefile that compiles the source files without relinking.

The project can be compiled using the following Makefile rules:

### Compilation Rules

- `make` or `make all`: Compiles the main project.
- `make bonus`: Compiles the project with bonus features.
- `make clean`: Removes object files and compilation folders.
- `make fclean`: Removes object files, compilation folders, and the executable.
- `make re`: Performs a complete reset of the project by removing all generated files and recompiling everything from scratch.

## Requirements

- Error handling without unexpected interruptions.
- No memory leaks.

## Notes

The program was successfully validated at 115%. ✅

---




