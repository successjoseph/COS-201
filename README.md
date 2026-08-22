# COS-201 — Student Record System

![C](https://img.shields.io/badge/Language-C-blue)

## Table of Contents
- [About](#about)
- [Project Contents](#project-contents)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Testing](#testing)
- [Contributing](#contributing)
- [Authors and License](#authors-and-license)

## About

This repository contains a university coursework project for a course called "COS 201": a command-line Student Record System written in C (`main.c`). It manages an in-memory, dynamically-allocated array of `Student` records (name, roll number, marks) with a menu-driven interface supporting add, remove, modify, display all, search by roll number, calculate average marks, sort by marks (ascending/descending via `qsort`), and save/load to a flat CSV-style text file. Code comments (e.g. `// 5. Memory Management: Allocate space for one more student`) map directly to specific assignment requirements, confirming this is coursework built to satisfy a graded rubric rather than a general-purpose tool. The repo also includes `COS 201 LABS ASSESSMENT.pdf` (the assignment brief), a `.vscode/tasks.json` GCC build task, a compiled `main.exe`, a sample data file (`COS_102_Student_Records.txt`), and six screenshots of the program running in `screenshots/`.

## Project Contents

```
COS-201/
├── main.c                              # Student Record System source
├── main.exe                            # Compiled Windows binary
├── COS 201 LABS ASSESSMENT.pdf          # Assignment brief
├── COS_102_Student_Records.txt          # Saved student records (CSV-style)
├── .vscode/tasks.json                  # VS Code GCC build task
└── screenshots/                        # Screenshots of the program running
```

## Prerequisites

- A C compiler. The included VS Code task (`.vscode/tasks.json`) invokes `C:\msys64\ucrt64\bin\gcc.exe` (MSYS2 UCRT64 GCC), but any standard C compiler (GCC, Clang, MSVC) will work.

## Installation

```bash
git clone https://github.com/successjoseph/COS-201.git
cd COS-201
gcc main.c -o main
```

## Configuration

None. The program reads/writes its data file using a hardcoded filename constant (`FILENAME = "COS_102_Student_Records.txt"`) in the same directory as the executable — there are no environment variables or external config files.

## Usage

```bash
./main
```

On startup it prompts for your name, then auto-loads any existing records from `COS_102_Student_Records.txt`. The main menu offers:
```
1. Add Student
2. Remove Student
3. Modify Student Record
4. Display All Students
5. Search for Student (by Roll No)
6. Calculate Average Marks
7. Sort Students by Marks
8. Save Records to File
0. Exit
```
Records are auto-saved to the CSV-style text file on exit (option 0), and a student is considered "Passed" if marks > 40.

## Testing

No automated tests are currently included.

## Contributing

This is a personal university coursework submission, not intended for outside contributions.

## Authors and License

- **Author:** successjoseph ([github.com/successjoseph](https://github.com/successjoseph))
- **License:** No license file included in this repository — all rights reserved by default.
