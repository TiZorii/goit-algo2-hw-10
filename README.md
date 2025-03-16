# Homework on "Algorithmic Complexity, Approximate, and Randomized Algorithms"

Hello! 👋🏻 Ready for a new challenge?

This homework consists of two independent tasks.

In the first task, you will learn to implement different variations of the QuickSort algorithm, conduct empirical studies on their efficiency, and visualize the results. Working with large datasets will deepen your understanding of how the choice of pivot element affects sorting performance and the differences between deterministic and randomized approaches.

This hands-on experience will enhance your critical thinking skills and ability to conduct experimental research in algorithms.

By completing the second task, you will learn to implement a greedy algorithm to solve a real optimization problem—creating a class schedule. This task will help you understand how to use a greedy approach to minimize resources (in this case, the number of teachers) while still achieving the desired goals (covering all subjects).

You will also learn how to work with selection criteria by implementing priority logic, preparing you to apply such methods in real-world projects.

This experience will give you a better understanding of how greedy algorithms work and how they can be applied to practical optimization problems.

Let's go! 🚵🏻‍♀️

## Task 1. Comparing Randomized and Deterministic QuickSort

Implement both randomized and deterministic QuickSort algorithms. Conduct a comparative analysis of their efficiency by measuring the average execution time on arrays of different sizes.

### Technical Requirements

1. To implement the randomized QuickSort algorithm, create a function  
   `randomized_quick_sort(arr)`, where the pivot element is chosen randomly.

2. To implement the deterministic QuickSort algorithm, create a function  
   `deterministic_quick_sort(arr)`, where the pivot element is chosen based on a fixed rule: the first, last, or middle element.

3. Generate test arrays of different sizes: `10,000`, `50,000`, `100,000`, and `500,000` elements. Populate the arrays with random integers.

4. Measure the execution time of both algorithms for each array. For a more accurate estimate, repeat the sorting process five times for each array and calculate the average execution time.

### Acceptance Criteria

📌 The acceptance criteria for this homework are mandatory for the mentor's review. If any criteria are not met, the homework will be sent back for revision without evaluation. If you need clarification 😉 or get stuck at any step, reach out to your mentor on Slack.

1. The `randomized_quick_sort` and `deterministic_quick_sort` functions correctly implement the sorting algorithms and successfully sort arrays (20 points).

2. The execution time of the algorithms is measured and presented in a table and graph (10 points).

3. The graphs are constructed with axis labels and a legend (5 points).

4. An analysis of the results is conducted, and conclusions regarding the efficiency of the randomized and deterministic QuickSort are drawn (10 points).

5. The code includes an example of usage and produces expected results (5 points).

### Example Graph Output

![Results](./assets/print_screen_0.png)

### Example Terminal Output

```bash
Розмір масиву: 10000
   Рандомізований QuickSort: 0.0189 секунд
   Детермінований QuickSort: 0.0189 секунд

Розмір масиву: 50000
   Рандомізований QuickSort: 0.1104 секунд
   Детермінований QuickSort: 0.1090 секунд

Розмір масиву: 100000
   Рандомізований QuickSort: 0.2333 секунд
   Детермінований QuickSort: 0.2435 секунд
.
Розмір масиву: 500000
   Рандомізований QuickSort: 1.4166 секунд
   Детермінований QuickSort: 1.4815 секунд

```

# Task 2: Creating a Class Schedule Using a Greedy Algorithm

## Problem Statement

Implement a program to create a university class schedule using a **greedy algorithm** for the **set cover problem**. The goal is to assign teachers to subjects in such a way that the number of teachers is minimized while ensuring all subjects are covered.

---

## Technical Requirements

Given Set of Subjects: {'Математика', 'Фізика', 'Хімія', 'Інформатика', 'Біологія'}
List of teachers:

1. Олександр Іваненко, 45 років, `o.ivanenko@example.com`, предмети:
   {'Математика', 'Фізика'}

2. Марія Петренко, 38 років, `m.petrenko@example.com`, предмети: {'Хімія'}

3. Сергій Коваленко, 50 років, `s.kovalenko@example.com`, предмети:
   {'Інформатика', 'Математика'}

4. Наталія Шевченко, 29 років, `n.shevchenko@example.com`, предмети:
   {'Біологія', 'Хімія'}

5. Дмитро Бондаренко, 35 років, `d.bondarenko@example.com`, предмети: {'Фізика',
   'Інформатика'}

6. Олена Гриценко, 42 роки, `o.grytsenko@example.com`, предмети: {'Біологія'}

## Task Description

### 1. Implement a `Teacher` Class

The `Teacher` class should have the following attributes:

- `first_name` (First name)
- `last_name` (Last name)
- `age` (Age)
- `email` (Email)
- `can_teach_subjects` (Set of subjects the teacher can teach)

### 2. Implement the `create_schedule` Function

The function should use a **greedy algorithm** to assign teachers to subjects. It should return a list of **teachers and the subjects assigned to them**.

#### **Selection Strategy (Greedy Approach):**

- At each step, **select the teacher who can teach the most uncovered subjects**.
- If multiple teachers qualify, **select the youngest**.
