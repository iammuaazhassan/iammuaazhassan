# Task Manager Project

## Overview
This project implements a task management system with functionality for adding, removing, updating, and finding tasks. The system also includes a priority queue for managing tasks based on their priority.

## Files
- `Task.h`: Header file for the `Task` class, which represents a single task with attributes such as task name, due date, and priority.
- `Task.cpp`: Implementation file for the `Task` class.
- `TaskManager.h`: Header file for the `TaskManager` class, which manages a collection of tasks, allowing for adding, removing, updating, and finding tasks.
- `TaskManager.cpp`: Implementation file for the `TaskManager` class.
- `TaskPriorityQueue.h`: Header file for the `TaskPriorityQueue` class, which manages tasks in a priority queue.
- `TaskPriorityQueue.cpp`: Implementation file for the `TaskPriorityQueue` class.
- `main.cpp`: Main program file, providing a menu-driven interface for interacting with the task management system.

## Classes

### Task
- **Attributes**:
  - `taskname`: Name of the task.
  - `date`: Due date of the task.
  - `priority`: Priority of the task.
- **Methods**:
  - `get_taskname()`
  - `set_taskname(string)`
  - `get_date()`
  - `set_date(string)`
  - `get_priority()`
  - `set_priority(int)`
  - `display_task_name()`
  - `display()`

### TaskManager
- **Attributes**:
  - `task`: An instance of `Task`.
  - `prev_task`: Pointer to the previous task in the list.
  - `next_task`: Pointer to the next task in the list.
  - `HEAD`: Pointer to the head of the task list.
- **Methods**:
  - `add_task()`
  - `remove_task(const string&)`
  - `update_task_priority(const string&, int)`
  - `update_task_name(const string&, const string&)`
  - `update_task_date(const string&, const string&)`
  - `find_task_by_name(const string&)`
  - `find_task_by_priority(int)`
  - `isPriorityAvailable(int)`
  - `display_task_names()`
  - `display_task_details()`

### TaskPriorityQueue
- **Attributes**:
  - `front`: Pointer to the front of the priority queue.
- **Methods**:
  - `enqueue(TaskManager* taskManager)`
  - `dequeue()`
  - `isEmpty()`
  - `displayPriorityQueue()`

## How to Use
1. **Compile the project**:
   ```sh
   g++ -o TaskManager main.cpp Task.cpp TaskManager.cpp TaskPriorityQueue.cpp
   ```

2. **Run the executable**:
   ```sh
   ./TaskManager
   ```

3. **Menu Options**:
   - Choose `1` to add a task.
   - Choose `2` to remove a task.
   - Choose `3` to update a task (task name or priority).
   - Choose `4` to find a task (by name or priority).
   - Choose `5` to display the task list (task names or details).
   - Choose `6` to display the priority queue.
   - Choose `7` to enqueue a task into the priority queue.
   - Choose `8` to dequeue a task from the priority queue.
   - Choose `0` to exit the menu.

## Example Usage
```sh
 ======================================================
|                    ----------                       |
|                       MENU                          |
|                    ----------                       |
|     CHOOSE 1 TO ADD TASK                            |
|     CHOOSE 2 TO REMOVE TASK                         |
|     CHOOSE 3 TO UPDATE TASK                         |
|     CHOOSE 4 TO FIND TASK                           |
|     CHOOSE 5 TO DISPLAY TASK LIST                   |
|     CHOOSE 6 TO DISPLAY PRIORITY QUEUE              |
|     CHOOSE 7 TO ENQUEUE TASK INTO PRIORITY QUEUE    |
|     CHOOSE 8 TO DEQUEUE TASK FROM PRIORITY QUEUE    |
|                                                     |
|     CHOOSE 0 TO EXIT MENU                           |
|                                                     |
 ======================================================

 ENTER YOUR CHOICE : 1
```

## License
This project is licensed under the MIT License. Feel free to use, modify, and distribute this code as you see fit.

## Author
[MUAAZ HASSAN ANSARI]
