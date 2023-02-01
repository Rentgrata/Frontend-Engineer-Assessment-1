# Filtering 


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
```

3. Requirements:

Build a class that filters a list of users based on specified criteria (name, date of birth, email).
The filtering mechanism should be dynamic and update the displayed list in real-time as the user changes the filter criteria.
The solution should be optimized for performance and user experience.

Examples:

- An example of using the class to filter a list of users:

```
const users: User[] = [
  { id: 1, name: "John Doe", dateOfBirth: "01/01/1990", email: "johndoe@example.com" },
  { id: 2, name: "Jane Doe", dateOfBirth: "02/01/1991", email: "janedoe@example.com" },
  { id: 3, name: "Bob Smith", dateOfBirth: "03/01/1992", email: "bobsmith@example.com" }
];

const filter = new UserFilter(users);
const filteredUsers = filter.filterBy({ name: "John Doe" });

console.log(filteredUsers);
// Output: [{ id: 1, name: "John Doe", dateOfBirth: "01/01/1990", email: "johndoe@example.com" }]
```

- An example of updating the filter criteria dynamically:

```
const filter = new UserFilter(users);

let filteredUsers = filter.filterBy({ name: "John Doe" });
console.log(filteredUsers);
// Output: [{ id: 1, name: "John Doe", dateOfBirth: "01/01/1990", email: "johndoe@example.com" }]

filter.updateFilterCriteria({ name: "Jane Doe" });
filteredUsers = filter.getFilteredUsers();
console.log(filteredUsers);
// Output: [{ id: 2, name: "Jane Doe", dateOfBirth: "02/01/1991", email: "janedoe@example.com" }]
```
