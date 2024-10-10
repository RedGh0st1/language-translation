# Language Translation

Convert the code below into JavaScript. Compare the patterns you see to what you know in JavaScript in order to make that translation.

**1. Python**

```python
for i in range(0, 11):
    if i % 2 == 0:
        print(i)

```

<details>
  <summary>Click to see the answer</summary>

```js
for (let i = 0; i < 11; i++) {
  if (i % 2 === 0) console.log(i);
}
```

```ruby
for i in 0..10
  if i.even?
    puts i
  end
end
```

</details>

**2. Java**

```java
int sum = 0;
for (int i = 1; i <= 5; i++) {
    sum += i;
}
System.out.println(sum);
```

<details>
  <summary>Click to see the answer</summary>

```js
let sum = 0;
for (let i = 1; i <= 5; i++) {
  sum += i;
}
console.log(sum);
```
```ruby
sum = 0
(1..5).each do |i|
  sum += i
end
puts sum
```

</details>

**3. Python isPrime**

```python
    if num < 2:
        return False
    for i in range(2, num):
        if num % i == 0:
            return False
    return True

print(is_prime(11))
```

<details>
  <summary>Click to see the answer</summary>

```js
function isPrime(num) {
  if (num < 2) {
    return false;
  }
  for (let i = 2; i < num; i++) {
    if (num % i === 0) {
      return false;
    }
  }
  return true;
}

console.log(isPrime(11));
```
```ruby
def is_prime(num)
  return false if num < 2
  (2...num).each do |i|
    return false if num % i == 0
  end
  true
end

puts is_prime(11)
```

</details>

**4. Java**

```java
int[] numbers = {4, 2, 8, 6, 1};
int max = numbers[0];

for (int i = 1; i < numbers.length; i++) {
    if (numbers[i] > max) {
        max = numbers[i];
    }
}
System.out.println("Largest number is: " + max);
```

<details>
  <summary>Click to see the answer</summary>

```js
let numbers = [4, 2, 8, 6, 1];
let max = numbers[0];

for (let i = 1; i < numbers.length; i++) {
  if (numbers[i] > max) {
    max = numbers[i];
  }
}

console.log("Largest number is: " + max);
```
```ruby
numbers = [4, 2, 8, 6, 1]
max = numbers[0]

numbers[1..-1].each do |num|
  max = num if num > max
end

puts "Largest number is: #{max}"
```

</details>

**5. Go**

```golang
package main

import (
	"fmt"
)

func halvingSum(n int) int {
	sum := n
	num := n
	for num > 0 {
		fmt.Println(num)
		num = num / 2 // Integer division in Go
		sum += num
	}
	return sum
}

func main() {
	res := halvingSum(25)
	fmt.Println(res)
}

```

<details>
  <summary>Click to see the answer</summary>

```js
function halvingSum(n) {
  let sum = n;
  let num = n;
  while (num > 0) {
    console.log(num);
    num = Math.floor(num / 2); // Integer division in JavaScript
    sum += num;
  }
  return sum;
}

const res = halvingSum(25);
console.log(res);
```

```ruby
def halving_sum(n)
  sum = n
  num = n
  while num > 0
    puts num
    num /= 2
    sum += num
  end
  sum
end

puts halving_sum(25)
```

</details>

**6. Java**

```java
// Function to calculate statistics: sum, average, max, min, and median from an array of numbers
import java.util.Arrays;

public static void main(String[] args) {
    int[] numbers = {5, 3, 8, 2, 7, 10};
    calculateStatistics(numbers);
}

public static void calculateStatistics(int[] numbers) {
    if (numbers.length == 0) {
        System.out.println("No numbers provided.");
        return;
    }

    // Calculate sum
    int sum = 0;
    for (int num : numbers) {
        sum += num;
    }

    // Calculate average
    double average = (double) sum / numbers.length;

    // Calculate max and min
    int max = numbers[0];
    int min = numbers[0];
    for (int num : numbers) {
        if (num > max) {
            max = num;
        }
        if (num < min) {
            min = num;
        }
    }

    // Calculate median
    Arrays.sort(numbers);
    double median;
    if (numbers.length % 2 == 0) {
        median = (numbers[numbers.length / 2 - 1] + numbers[numbers.length / 2]) / 2.0;
    } else {
        median = numbers[numbers.length / 2];
    }

    // Print the results
    System.out.println("Sum: " + sum);
    System.out.println("Average: " + average);
    System.out.println("Max: " + max);
    System.out.println("Min: " + min);
    System.out.println("Median: " + median);
}

```

<details>
  <summary>Click to see the answer</summary>

```js
function main() {
  let numbers = [5, 3, 8, 2, 7, 10];
  calculateStatistics(numbers);
}

function calculateStatistics(numbers) {
  if (numbers.length === 0) {
    console.log("No numbers provided.");
    return;
  }

  // Calculate sum
  let sum = 0;
  for (let num of numbers) {
    sum += num;
  }

  // Calculate average
  let average = sum / numbers.length;

  // Calculate max and min
  let max = numbers[0];
  let min = numbers[0];
  for (let num of numbers) {
    if (num > max) {
      max = num;
    }
    if (num < min) {
      min = num;
    }
  }

  // Calculate median
  numbers.sort((a, b) => a - b); // Sort the array
  let median;
  if (numbers.length % 2 === 0) {
    median =
      (numbers[numbers.length / 2 - 1] + numbers[numbers.length / 2]) / 2;
  } else {
    median = numbers[Math.floor(numbers.length / 2)];
  }

  // Print the results
  console.log("Sum: " + sum);
  console.log("Average: " + average);
  console.log("Max: " + max);
  console.log("Min: " + min);
  console.log("Median: " + median);
}

// Run the main function to test
main();
```
```ruby
def calculate_statistics(numbers)
  if numbers.empty?
    puts "No numbers provided."
    return
  end

  sum = numbers.sum
  average = sum.to_f / numbers.length
  max = numbers.max
  min = numbers.min

  sorted_numbers = numbers.sort
  median = if sorted_numbers.length.even?
             (sorted_numbers[sorted_numbers.length / 2 - 1] + sorted_numbers[sorted_numbers.length / 2]) / 2.0
           else
             sorted_numbers[sorted_numbers.length / 2]
           end

  puts "Sum: #{sum}"
  puts "Average: #{average}"
  puts "Max: #{max}"
  puts "Min: #{min}"
  puts "Median: #{median}"
end

numbers = [5, 3, 8, 2, 7, 10]
calculate_statistics(numbers)
```
</details>

**7. Python**

```python
def manage_tasks():
    tasks = []

    def add_task(task):
        tasks.append({"task": task, "done": False})
        print(f'Task "{task}" added.')

    def remove_task(task):
        for t in tasks:
            if t["task"] == task:
                tasks.remove(t)
                print(f'Task "{task}" removed.')
                return
        print(f'Task "{task}" not found.')

    def list_tasks():
        if tasks:
            for i, t in enumerate(tasks, start=1):
                status = "done" if t["done"] else "not done"
                print(f'{i}. {t["task"]} - {status}')
        else:
            print("No tasks in the list.")

    def mark_done(task):
        for t in tasks:
            if t["task"] == task:
                t["done"] = True
                print(f'Task "{task}" marked as done.')
                return
        print(f'Task "{task}" not found.')

    # Simulate some operations
    add_task("Buy groceries")
    add_task("Clean room")
    list_tasks()
    mark_done("Buy groceries")
    list_tasks()
    remove_task("Clean room")
    list_tasks()

# Call the function to simulate task management
manage_tasks()
```

<details>
  <summary>Click to see the answer</summary>

```js
function manageTasks() {
  let tasks = [];

  function addTask(task) {
    tasks.push({ task: task, done: false });
    console.log(`Task "${task}" added.`);
  }

  function removeTask(task) {
    for (let i = 0; i < tasks.length; i++) {
      if (tasks[i].task === task) {
        tasks.splice(i, 1); // Remove the task from the array
        console.log(`Task "${task}" removed.`);
        return;
      }
    }
    console.log(`Task "${task}" not found.`);
  }

  function listTasks() {
    if (tasks.length > 0) {
      tasks.forEach((t, i) => {
        let status = t.done ? "done" : "not done";
        console.log(`${i + 1}. ${t.task} - ${status}`);
      });
    } else {
      console.log("No tasks in the list.");
    }
  }

  function markDone(task) {
    for (let i = 0; i < tasks.length; i++) {
      if (tasks[i].task === task) {
        tasks[i].done = true;
        console.log(`Task "${task}" marked as done.`);
        return;
      }
    }
    console.log(`Task "${task}" not found.`);
  }

  // Simulate some operations
  addTask("Buy groceries");
  addTask("Clean room");
  listTasks();
  markDone("Buy groceries");
  listTasks();
  removeTask("Clean room");
  listTasks();
}

// Call the function to simulate task management
manageTasks();
```

```ruby
def manage_tasks
  tasks = []

  add_task = ->(task) {
    tasks << {task: task, done: false}
    puts "Task \"#{task}\" added."
  }

  remove_task = ->(task) {
    tasks.reject! { |t| t[:task] == task }
    puts "Task \"#{task}\" removed."
  }

  list_tasks = -> {
    if tasks.empty?
      puts "No tasks in the list."
    else
      tasks.each_with_index do |t, i|
        status = t[:done] ? "done" : "not done"
        puts "#{i + 1}. #{t[:task]} - #{status}"
      end
    end
  }

  mark_done = ->(task) {
    task_item = tasks.find { |t| t[:task] == task }
    task_item[:done] = true if task_item
    puts "Task \"#{task}\" marked as done."
  }

  # Simulate some operations
  add_task.call("Buy groceries")
  add_task.call("Clean room")
  list_tasks.call
  mark_done.call("Buy groceries")
  list_tasks.call
  remove_task.call("Clean room")
  list_tasks.call
end

manage_tasks
```

</details>

**8. Java**

```java
class Car {
    String model;
    int year;

    Car(String model, int year) {
        this.model = model;
        this.year = year;
    }

    void displayInfo() {
        System.out.println("Model: " + this.model + ", Year: " + this.year);
    }
}

public class Main {
    public static void main(String[] args) {
        Car car1 = new Car("Toyota", 2020);
        car1.displayInfo();
    }
}
```

<details>
  <summary>Click to see the answer</summary>

```js
class Car {
  constructor(model, year) {
    this.model = model;
    this.year = year;
  }

  displayInfo() {
    console.log(`Model: ${this.model}, Year: ${this.year}`);
  }
}

const main = () => {
  const car1 = new Car("Toyota", 2020);
  car1.displayInfo();
};

// Call the main function
main();
```

```ruby
class Car
  def initialize(model, year)
    @model = model
    @year = year
  end

  def display_info
    puts "Model: #{@model}, Year: #{@year}"
  end
end

car1 = Car.new("Toyota", 2020)
car1.display_info
```
</details>
