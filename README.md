class ToDoList:
    def __init__(self):
        self.tasks = []

    def add_task(self, task):
        self.tasks.append(task)
        print(f"Task '{task}' added to the to-do list.")

    def remove_task(self, task):
        if task in self.tasks:
            self.tasks.remove(task)
            print(f"Task '{task}' removed from the to-do list.")
        else:
            print(f"Task '{task}' not found in the to-do list.")

    def display_tasks(self):
        if self.tasks:
            print("Tasks in the to-do list:")
            for task in self.tasks:
                print(f"- {task}")
        else:
            print("No tasks in the to-do list.")

# Usage 
todo = ToDoList()
todo.add_task("Complete project")
todo.add_task("Buy groceries")
todo.display_tasks()
todo.remove_task("Buy groceries")
todo.display_tasks()
