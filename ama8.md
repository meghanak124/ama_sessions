# Computer Science & AI Concepts

## 1. Which Uses Separate Memory: Process or Thread?

- **Process** uses separate memory.
- Each process has its own memory space, resources, and execution environment.
- Threads inside the same process share the same memory.

### Example

- Opening multiple applications on your computer = multiple processes.
- Multiple tabs/tasks inside one application may use threads.

---

## 2. What is a Module?

A **module** is a file or collection of code that contains functions, classes, or variables which can be reused in other programs.

### Purpose of Modules

- Organize code
- Reuse functionality
- Improve maintainability

### Example in Python

```python
import math

print(math.sqrt(25))
```

Here, `math` is a module.

---

## 3. Difference Between Multithreading and Multiprocessing

| Feature        | Multithreading                      | Multiprocessing                                 |
| -------------- | ----------------------------------- | ----------------------------------------------- |
| Memory         | Shared memory                       | Separate memory                                 |
| Speed          | Faster communication                | Slower communication                            |
| Best For       | I/O-bound tasks                     | CPU-bound tasks                                 |
| Crash Impact   | One thread crash may affect process | One process crash usually doesn't affect others |
| Resource Usage | Lightweight                         | More resource-intensive                         |

### Examples

- **Multithreading:** Chat applications, web servers
- **Multiprocessing:** Video rendering, machine learning training

---

## 4. What is MCP?

MCP stands for **Model Context Protocol**.

It is a protocol that helps AI models communicate with external tools, applications, databases, and services in a standardized way.

### Purpose of MCP

- Connect AI with external systems
- Enable tool usage
- Share structured context between applications and AI models

### Example

An AI assistant using MCP can:

- Read files
- Query databases
- Access APIs
- Use external tools safely

---

## 5. Difference Between DOM and Virtual DOM

| Feature       | DOM                               | Virtual DOM                  |
| ------------- | --------------------------------- | ---------------------------- |
| Definition    | Real webpage structure            | Lightweight copy of DOM      |
| Speed         | Slower updates                    | Faster updates               |
| Update Method | Updates entire structure directly | Updates only changed parts   |
| Performance   | Less optimized                    | Highly optimized             |
| Used In       | Traditional JavaScript            | React and similar frameworks |

### DOM

DOM (Document Object Model) represents webpage elements as objects.

### Virtual DOM

Virtual DOM is a virtual representation of the real DOM used to improve performance.

---

## 6. Difference Between AI and ML

| Feature    | AI (Artificial Intelligence)  | ML (Machine Learning)                 |
| ---------- | ----------------------------- | ------------------------------------- |
| Definition | Simulating human intelligence | Subset of AI that learns from data    |
| Goal       | Make machines intelligent     | Enable systems to learn automatically |
| Scope      | Broad field                   | Specific approach within AI           |
| Examples   | Chatbots, robotics            | Recommendation systems, spam filters  |

### Relationship

- AI is the bigger concept.
- ML is one technique used to achieve AI.

### Example

- AI = Self-driving car system
- ML = Algorithm learning driving patterns from data
