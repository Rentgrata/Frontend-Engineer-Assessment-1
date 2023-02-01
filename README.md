# Filter Problem


1. Problem statement:

You are asked to build a class in TypeScript that filters a list of users received from a backend API. The filter should allow users to search for specific users based on specified criteria such as name, date of birth, and email. The solution should be optimized for performance and user experience.


2. Data:

The data received from the backend API will consist of an array of user objects, each with the following properties:


```
interface User {
  id: number;
  name: string;
  dateOfBirth: string;
  email: string;
}

const users: User[] = [
  { id: 1, name: "John Doe", dateOfBirth: "01/01/1990", email: "johndoe@example.com" },
  { id: 2, name: "Jane Doe", dateOfBirth: "02/01/1991", email: "janedoe@example.com" },
  { id: 3, name: "Bob Smith", dateOfBirth: "03/01/1992", email: "bobsmith@example.com" }
];
```


3. Requirements:

Build a class that filters a list of users based on specified criteria (name, date of birth, email).
The filtering mechanism should be dynamic and update the displayed list in real-time as the user changes the filter criteria.
The solution should be optimized for performance and user experience.

- Note: The filter should check whether the input contains or exactly matches the input string.


