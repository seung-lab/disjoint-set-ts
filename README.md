Disjoint Set Implementation
===========================

The first task is to implement the disjoint set (also known as union-find) data structure in Typescript. In our work with labeled 3d images, we sometimes use disjoint sets to represent agglomerations of smaller labels as larger more meaningful objects such as neurons. A disjoint set allows us to efficiently represent sets of objects that have no overlap between them. That is, if label A and label C belong to different sets, label B may be joined to either label A or label B but not both. If label B is joined to label A and then joined to label C, the sets will merge into a single ABC set with the original isolated A and C sets ceasing to exist.

You can read more about disjoint sets on [Wikipedia](https://en.wikipedia.org/wiki/Disjoint-set_data_structure). 

To complete the assignment, you’ll fill in the missing code for a single Typescript file, disjointset.ts, that contains the class definition for a DisjointSet and its operations makeset, union, and find. We will compile the file into a javascript file using the tsc command as and run the program like so:

```bash
tsc --lib es2021 disjointset.ts
node disjointset.ts input.txt
```

Which should output the number of sets, their set representatives (which should be the minimum member of each set), and the size of each set. Running `find` on a non-member element should return null.

In the text input, the format is two signed integers on each line separated by a space that represent a union pair.

Your code must compile and produce correct output. We will run some tests on our side to make sure edge cases are covered.

Provide written answers between a sentence to a paragraph for the following questions:

* What are some notable differences that this disjoint set data structure has compared to a typical set implementation?
* Is it possible to add a `delete` operation to the disjoint set? If so, what is the time complexity?
* If we restricted the size of the inputs to 16-bit unsigned integers, how might you improve the run time of the implementation?
* Under what circumstances would you choose half-path vs full-path compression?
