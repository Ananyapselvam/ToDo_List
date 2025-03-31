def todo_list():
    tasks = []

    def add_task(task):
        tasks.append({"task": task, "completed": False})
        print(f"Task '{task}' added.")

    def view_tasks():
        if not tasks:
            print("To-do list is empty.")
        else:
            print("To-Do List:")
            for index, task in enumerate(tasks):
                status = "[X]" if task["completed"] else "[ ]"
                print(f"{index + 1}. {status} {task['task']}")

    def complete_task(task_index):
        if 1 <= task_index <= len(tasks):
            tasks[task_index - 1]["completed"] = True
            print(f"Task '{tasks[task_index - 1]['task']}' marked as completed.")
        else:
            print("Invalid task number.")

    def remove_task(task_index):
        if 1 <= task_index <= len(tasks):
            removed_task = tasks.pop(task_index - 1)
            print(f"Task '{removed_task['task']}' removed.")
        else:
            print("Invalid task number.")

    while True:
        print("\nOptions:")
        print("1. Add task")
        print("2. View tasks")
        print("3. Complete task")
        print("4. Remove task")
        print("5. Exit")

        choice = input("Enter your choice: ")

        if choice == "1":
            task = input("Enter task: ")
            add_task(task)
        elif choice == "2":
            view_tasks()
        elif choice == "3":
            try:
                task_index = int(input("Enter task number to complete: "))
                complete_task(task_index)
            except ValueError:
                print("Invalid input. Please enter a number.")
        elif choice == "4":
            try:
                task_index = int(input("Enter task number to remove: "))
                remove_task(task_index)
            except ValueError:
                print("Invalid input. Please enter a number.")
        elif choice == "5":
            print("Exiting...")
            break
        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    todo_list()
