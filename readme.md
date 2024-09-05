# Language Translation

Convert the code below into JavaScript

1. Python

```python
for i in range(0, 11):
    if i % 2 == 0:
        print(i)

```

2. Java

```java
int sum = 0;
for (int i = 1; i <= 5; i++) {
    sum += i;
}
System.out.println(sum);
```

3. Python isPrime

```python
    if num < 2:
        return False
    for i in range(2, num):
        if num % i == 0:
            return False
    return True

print(is_prime(11))
```

4. Java

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

5. Go

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

6. Java

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

7. Python

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

8. Java

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
