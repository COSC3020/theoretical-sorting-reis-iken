[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/9YUeXH71)
# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.

**MY ANSWER:**

Obviously, the algorithms mergesort, quicksort, insertion sort, and heapsort are comparison-based - but we have not found such an algorithm with $O(n)$ time.

We must set straight the fact that we cannot assume anything - the comparisons we make are all we know about the data set.

So someone claiming such a thing as this $O(n)$ algorithm would be revolutionary...

I'm not sold it's possible. How could it be? The decision tree model shows - there is no way that we could successfully sort the data set in faster than $O(nlogn)$ time without making additional assumptions.

But let's talk about how we might go about verifying this claim anyways (more like disprove it).

Obviously, we would need to test the algorithm using diverse data sets - data sets with varying levels of size and varying levels of already-sortedness, including totally sorted, reverse-sorted, random, etc.

We would definitely want to see how the algorithm performs with exceedingly large data sets.

In these tests, we would expect to see faster runtimes than the other algorithms for every input. But not only that, we would also expect to see the runtime linearly increase with the input size, since that is what's being claimed here.

We would also want to see whether the algorithm is consistent throughout multiple runs of the same input. And would want to observe the space complexity of the algorithm as well, if we can.

Ultimately, however, the decision tree has proved for us that it is impossible for us to sort solely using comparison faster than $O(nlogn)$ time. It is worth noting, however, that $O(nlogn)$ is our theoretical lower bound for the worst-case time complexity. So in theory, to find a better algorithm, we would need to prove that the worst case runtime is better than $O(nlogn)$ . Once again, however, our decision tree is blatant proof that this is impossible. There's not a whole lot to it - unless some metaphorically 4th-dimensional idea comes into play, we cannot acheive better runtime.
