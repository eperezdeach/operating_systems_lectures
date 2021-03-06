# C++ Containers

In this practice you are going to study how two common C++ containers work (`std::vector` and `std::list`), in relation with memory access performance.

## Question 1
In this first part you will see how `push_back` works on both containers.
-   Inserting elements in a vector without pre-allocation.
-   Inserting elements in a vector with memory pre-allocation.
-   Inserting elements in a list.
-   Same as first but using pointers this time.

Answer following sub-questions:

1.  How element insertion differs in a vector and a list?
2.  What happens to existing elements in a vector when the container has to grow to store a new element? Are those elements exactly the same after insertion?
3.  What happens when memory is pre-allocated? How does it affect `std::vector<T>::push_back`.
4.  How are elements in a list distributed along memory?
5.  What are the differences between using objects and pointer to objects in a container?

## Question 2
Now, let's study how a sorting operation works on each of the containers

1.  How are elements inside the container affected? Please briefly describe what's happening under-the-hood.
2.  Why syntax is different?

## Question 3
This question will cover speed performance aspects when inserting elements. Please, experiment with different number of elements before making any conclusion.

1.  How is the performance between a vector and a list? Which one should be used?
2.  Plot the insertion speed for different total number of elements (100, 1000, 5000, 10000, 20000, 100000...)
3.  What are the differences between `C` and `D` classes? How does it affect insertion performance?
4.  Repeat the previous plot but using `D` elements.
5.  Something interesting happened when first executing tests for `D`. What was it? Why? Try commenting out the `profile_push_backs<std::vector<D>>(n)` line. Try also reducing the number of elements. Does it work now?

## Question 4
This last part inspects speed performance when accessing elements.

1.  How is the performance between a vector and a list? Which one should be used?
2.  Plot the access speed for different total number of elements (100, 1000, 5000, 10000, 20000, 100000...)

## Delivery and Grading
A PDF containing the answers to questions must be sent to Professor's email before November 17th, 2019, 23:59:59. Only the last email within the valid period will be corrected, but all deliveries after deadline will just be ignored.

This practice aims for 5% of the course (maximum score is then 0.5). All questions has the same weight.

## Side notes
### C class
The only purpose of `C` class is to define traceable constructors and destructors, so you can keep track of the life-cycle of the object.

### TicToc class
This helper class will allow you to automatically measure the execution time between the point where the `TicToc` object is created and where it is destroyed.
