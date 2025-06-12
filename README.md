# Comp-251-Assignment-1-solution

Download Here: [Comp 251: Assignment 1 solution](https://jarviscodinghub.com/assignment/comp-251-assignment-1-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

Questions
Exercise 1 (80 points) We want to compare the performance of hash tables implemented using chaining
and open addressing. In this assignment, we will consider hash tables implemented using the multiplication and linear probing methods. We will (respectively) call the hash functions h and g and describe
them below. Note that we are using the hash function h to define g.
Collisions solved by chaining (multiplication method): h(k) = ((A · k) mod 2w) >> (w − r)
Open addressing (linear probing): g(k, i) = (h(k) + i) mod 2r
In the formula above, r and w are two integers such that w > r, and A is a random number such that
2
w−1 < A < 2
w. In addition, let n be the number of keys inserted, and m the number of slots in the hash
tables. Here, we set m = 2r
and r = dw/2e. The load factor α is equal to n
m
.
We want to estimate the number of collisions in random sequences of insertions and deletions of keys
with respect to the choice of values for w and α.
We provide you a set of three template files within COMP251HW1.zip that you will complete. This
file contains three classes, a main class and one for each hash function. Those contain several helper
functions, namely generateRandom that enables you to generate a random number within a specified
range. Details on which functions are included, how to use them, and where to add in your code can be
found as comments in the java files. Please read them with attention. In addition, we provide you a jar
file to visualize your results named JavaPlotBuilder.jar.
Your first task is to complete the two java methods Open_Addressing.probe and Chaining.chain.
These methods must implement the hash functions for (respectively) the linear probing and multiplication methods. They take as input a key k, as well as an integer 0 ≤ i < m for the linear probing method,
and return a hash value in [0, m[. Note that the value of A must be updated when you change w.
Next, you will implement the method insertKey in both classes, which inserts a key k into the
hash table and returns the number of collisions encountered before insertion. Note that for this exercise
2
as well as for the rest of the homework, we define the number of collisions as the number of keys encountered, or “jumped over” before inserting or removing a key. You can assume the key is not negative.
You will also implement a method removeKey, this one only in Open_Addressing. This
method should take as input a key k, and remove it from the hash table while visiting the minimum
number of slots possible. Like insertKey, it should output the number of collisions. If the key is not
in the hash table, the method should simply not change the hash table, and output the number of slots
visited. You will notice from the code and comments that empty slots are given a value of −1. If applicable, you are allowed to use a different notation of your choice for slots containing a deleted element.
Finally, you will complete the method main.main, which calls the previous functions from the
main class. There are three tasks to complete within this main method.
Task 1
First, you will test the effect of increasing the number of keys on the average number of collisions for
each hash function. You will be given an array of keys to insert, keysToInsert, and a list of values
of n to test, nList inside the main method. Random seeds can be used in java in order to make random results reproducible (and eventually evaluate assignments). You will find the hash tables already
initialized with such seed. For each value of n, insert the n first elements of keysToInsert into each
hash table, and store the α value, as well as the average number of collisions for that value of α into the
appropriate provided list. The program is already set up to output a CSV file for you to visualize.
Task 2
Your second task is to test the removeKey method on the Open_Addressing table from task 1
with n=16. Initialize a new Open_Addressing hash table with the same seed as in Task 1, and insert the first 16 elements of keysToInsert. You will be given an array of keys to remove named
keysToRemove. Call removeKey with each of these keys. Store the number of collisions associated
with each removal operation in the arraylist removeCollisions, as well as the index of the key you just
attempted to remove in removeIndex. Finally, use the provided method to output a CSV file.
Task 3
Your third task is to evaluate the effect of varying w on the number of collisions for each method. For
this exercise, the keys you insert will be generated randomly with generateRandom. Each key can
be inserted only once (i.e. The random sequence of keys must have no duplicates). For this exercise,
you will not be using a specific seed, which you can do by calling functions that require a seed argument
with a seed of −1. Because your experiments will now have some variance, you will need to execute 10
simulations for each value of w to obtain representative averages. You will choose appropriate values of
w, use the provided function to output a CSV file, and visualize your results. You will submit a pdf file,
called Conclusions.pdf, including plots of your results, as well as a short explanation of what you
observe, and an explanation for it.
To plot your results, you can use JavaPlotBuilder.jar to generate a plot with α on the x-axis
and the average number of collision on the y-axis. JavaPlotBuilder.jar is run from command
line as follows:
java -jar JavaPlotBuilder.jar filename.csv
3
where filename.csv is the name of the file that is generated by the main method.
For this assignment, you will need to submit a zip file containing the completed version of the three
provided java files, n_comparison.csv, remove_collisions.csv, and w_comparison.csv
(the three CSV files generated by the main method), as well as Conclusions.pdf, the PDF file with
your observations and explanations.
Once you have submitted your files, you can proceed to the second part of the assignment.
Exercise 2 (20 points) This section is answerable through MyCourses. Note that you MUST use your
own results to answer those questions. Answers to this quiz that would not match the results presented
in your pdf file will be considered plagiarism (refer to course outline).

