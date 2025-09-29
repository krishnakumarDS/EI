# Virtual Classroom Manager

A terminal-based Virtual Classroom Manager application for EdTech platforms, built with TypeScript following SOLID principles and design patterns.

## Features

- **Classroom Management**: Add, list, and remove virtual classrooms
- **Student Management**: Enroll students into classrooms and list students in each classroom
- **Assignment Management**: Schedule assignments for classrooms and allow students to submit them
- **Robust Error Handling**: Comprehensive error handling with logging and retry mechanisms
- **Clean Architecture**: Follows SOLID principles and design patterns for maintainability

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd virtual-classroom-manager
```

2. Install dependencies:
```bash
npm install
```

3. Build the TypeScript code:
```bash
npm run build
```

## Usage

Run the application:
```bash
npm start
```

Or for development:
```bash
npm run dev
```

## Commands

### Classroom Management
- `add_classroom [name]` - Create a new classroom
  ```
  > add_classroom Math 101
  Classroom Math 101 has been created.
  ```

- `list_classrooms` - List all classrooms
  ```
  > list_classrooms
  Available Classrooms:
  - Math 101 (Students: 1, Assignments: 1)
  ```

### Student Management
- `add_student [id] [class name]` - Enroll a student in a classroom
  ```
  > add_student S12345 Math 101
  Student S12345 has been enrolled in Math 101.
  ```

- `list_students` - List all students
  ```
  > list_students
  Available Students:
  - S12345 (Enrolled in: Math 101)
  ```

- `list_students_in_classroom [name]` - List students in a specific classroom
  ```
  > list_students_in_classroom Math 101
  Students in Classroom Math 101:
  - S12345
  ```

### Assignment Management
- `schedule_assignment [class] [details]` - Schedule an assignment for a class
  ```
  > schedule_assignment Math 101 Complete exercises 1-10 from page 25
  Assignment for Math 101 has been scheduled.
  ```

- `submit_assignment [id] [class] [details]` - Submit an assignment
  ```
  > submit_assignment S12345 Math 101 Complete exercises 1-10 from page 25
  Assignment submitted by Student S12345 in Math 101.
  ```

- `list_assignments` - List all assignments
  ```
  > list_assignments
  Available Assignments:
  - assignment_1: Complete exercises 1-10 from page 25 (Class: Math 101, Submissions: 1)
  ```

- `list_assignments_for_classroom [name]` - List assignments for a specific classroom
  ```
  > list_assignments_for_classroom Math 101
  Assignments for Classroom Math 101:
  - assignment_1: Complete exercises 1-10 from page 25 (Submissions: 1)
  ```

### Other Commands
- `help` - Show available commands
- `exit` - Exit the application

## Architecture

The application follows a clean architecture with separation of concerns:

### Folder Structure
```
virtual-classroom-manager/
├── src/
│   ├── controllers/         # Handle user input/output
│   ├── models/             # Domain entities
│   ├── services/           # Business logic
│   ├── repositories/       # Data access layer
│   ├── interfaces/         # Type definitions
│   ├── utils/              # Utility functions
│   ├── main.ts             # Application entry point
│   └── VirtualClassroomManager.ts  # Main application class
├── package.json
├── tsconfig.json
└── README.md
```

### Design Patterns Used

1. **MVC (Model-View-Controller) Pattern**
   - Models: `Classroom`, `Student`, `Assignment`, `Submission`
   - Controllers: `ClassroomController`, `StudentController`, `AssignmentController`
   - View: Terminal output handled in `VirtualClassroomManager`

2. **Repository Pattern**
   - `ClassroomRepository`, `StudentRepository`, `AssignmentRepository`
   - Abstracts data access and implements `IRepository<T>` interface

3. **Singleton Pattern**
   - `Logger`, `ErrorHandler`, and all repositories
   - Ensures single instance throughout the application

4. **Service Layer Pattern**
   - `ClassroomService`, `StudentService`, `AssignmentService`
   - Encapsulates business logic and implement corresponding interfaces

### SOLID Principles

1. **Single Responsibility Principle (SRP)**
   - Each class has a single responsibility (e.g., `Logger` only handles logging)

2. **Open/Closed Principle (OCP)**
   - Interfaces allow for extension without modification

3. **Liskov Substitution Principle (LSP)**
   - All implementations can be substituted for their interfaces

4. **Interface Segregation Principle (ISP)**
   - Specific interfaces for each service type

5. **Dependency Inversion Principle (DIP)**
   - High-level modules depend on abstractions (interfaces)

## Error Handling

The application includes robust error handling:

- **Centralized Error Handling**: `ErrorHandler` class provides consistent error handling
- **Logging**: `Logger` class provides centralized logging with timestamps
- **Retry Mechanism**: Transient errors are automatically retried
- **Type-Safe Error Handling**: Proper handling of TypeScript's `unknown` error type

## Development

### Adding New Features

1. Create models in the `src/models/` directory
2. Define interfaces in `src/interfaces/`
3. Implement repositories in `src/repositories/`
4. Add business logic in `src/services/`
5. Create controllers in `src/controllers/`
6. Update `VirtualClassroomManager.ts` to handle new commands

### Running Tests

```bash
npm test
```

### Building for Production

```bash
npm run build
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

