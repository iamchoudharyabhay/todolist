#include <iostream>
#include <vector>
#include <string>

using namespace std;

class TodoList {
private:
    vector<string> tasks;

public:
    void addTask(const string& task) {
        tasks.push_back(task);
    }

    void displayTasks() const {
        cout << "Tasks:\n";
        for (const string& task : tasks) {
            cout << "- " << task << endl;
        }
    }
};

int main() {
    TodoList todoList;

    // Adding tasks
    todoList.addTask("Complete homework");
    todoList.addTask("Buy groceries");
    todoList.addTask("Exercise");

    // Displaying tasks
    todoList.displayTasks();

    return 0;
}
