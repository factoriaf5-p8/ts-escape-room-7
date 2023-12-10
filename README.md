# Typescript Labs

## Lab 7: Working with Arrays

file: `/src/07-arrays.problem.ts`



Let's start looking at a bit more complex type declarations.

We've got a `User` type that is similar to what we've had before. We also have a new `Post` interface:

```ts
interface User {
  id: number;
  firstName: string;
  lastName: string;
  role: "admin" | "user" | "super-admin";
  posts: Post;
}

interface Post {
  id: number;
  title: string;
}
```
I've created a `defaultUser` that has a couple of posts added, but there's an error:

```ts
export const defaultUser: User = {
  id: 1,
  firstName: "Matt",
  lastName: "Pocock",
  role: "admin",
  posts: [
    {
      id: 1,
      title: "How I eat so much cheese",
    },
    {
      id: 2,
      title: "Why I don't eat more vegetables",
    },
  ],
};
```
The problem is that in the `User` interface it's expecting a single `Post` instead of the array that `defaultUser` has.

Challenge
Your challenge is to fix this type error by determining how to represent arrays.