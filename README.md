# Student Management Console

A command-line application for managing student records with features for adding, editing, deleting, and searching student information. The application uses JSON files for data storage in a structured directory format.

## Features

- Add new students with unique 7-digit IDs
- Edit existing student records
- Delete student records
- Search for students using various criteria
- JSON-based data storage with organized directory structure

## Project Structure

```
project_dir/
├── students/
│   ├── 12/
│   │   ├── 1234567.json    # Student record
├── run.php                  # Main application entry point
```

## Requirements

- PHP 7.4 or higher
- CLI environment (Command Prompt, Terminal, etc.)

## Usage

### Basic Command Structure

```sh
php run.php --action=<action> [--id=<student_id>]
```

### Adding a New Student

```sh
php run.php --action=add
```

The system will prompt for:
- Student ID (7-digit unique identifier)
- Name
- Surname
- Age
- Curriculum

Example stored file (`students/12/1234567.json`):
```json
{
  "id": "1234567",
  "name": "John",
  "surname": "Doe",
  "age": 22,
  "curriculum": "Computer Science"
}
```

### Editing a Student

```sh
php run.php --action=edit --id=1234567
```

You can update any field while leaving others unchanged:
```
Enter new name [John]: Jack
Enter new surname [Doe]:
Enter new age [22]: 23
Enter new curriculum [Computer Science]:
```

### Deleting a Student

```sh
php run.php --action=delete --id=1234567
```

### Searching for Students

```sh
php run.php --action=search
```

Search results are displayed in a table format:
```
ID       | Name | Surname | Age | Curriculum
----------------------------------------------
1234567  | Jack | Doe     | 23  | Computer Science
```

## Technical Details

### Data Storage
- Student records are stored as individual JSON files
- Files are organized in directories named after the first two digits of the student ID
- Each record contains: id, name, surname, age, and curriculum

### Implementation
- Built using modern PHP standards and OOP principles
- Utilizes command-line interface for interaction
- Implements file handling for data persistence
- Ensures data integrity through structured storage

## Future Improvements

- Graphical user interface (GUI)
- Database integration (MySQL, SQLite)
- Advanced search functionality
- User authentication and role management

## Author

**Tebogo Phiri**
- GitHub: [TebogoP](https://github.com/TebogoP/)
- LinkedIn: [Tebogo Phiri](https://www.linkedin.com/in/tebogo-phiri-b5a96796/)

## License

This project is licensed under the MIT License.
