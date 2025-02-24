Download link :https://programming.engineering/product/data-structures-homework-3-minimum-spanning-tree/


# Data-Structures-Homework-3-Minimum-Spanning-Tree
Data Structures Homework 3: Minimum Spanning Tree
1. Introduction

In this project, you should implement Kruskal’s algorithm, which calculates a minimum spanning tree of a given graph. You should write a program that reads a file which contains information of the graph and outputs the minimum spanning tree in the given format.

There can be many different implementation, but your implementation should have a time complexity of O(e log n), where e is the number of edges and n is the number of vertices in the given graph.

As described in the lecture slides, you can achieve O(e log n) by using min heap and disjoint set trees.

2. Requirements (Read Carefully!)

You should write a single C program, named hw3.

The program takes one command-line argument, which is the input file name. For example, the user will run the program like this:

./hw3 input.txt

The first argument is the name of the input file.

If the number of command-line arguments is not 1 (zero or more than 1), then you should print a usage string on the display and exit the program. The usage string looks like this:

usage: ./hw3 input_filename

If the input file does not exist, your program should display an error message on the screen and terminate. The error message should be:

The input file does not exist.

The input file format is like the following. Here we assume the graph is an undirected graph.

The first line contains the number of vertices in the graph. We assume that the vertex number starts from 0. Thus, if there are 7 vertices in the graph, the vertex numbers are 0 to 6.

The second line contains the number of edges in the graph.


From the third line, each line contains three numbers, each separated by a space. The first two numbers are end points of an edge, and the third number is the weight of the edge.

An example input file looks like this.

7

9

0128

0510

1216

1614

2312

3422

3618

4525

4624

The corresponding graph for this input will be:



Your program should generate an output file named “hw3_result.txt“. The format of the output file is as follows.

From the first line, each line should print the edge that is included in the minimum spanning tree. Specifically, the line should contain three numbers: source vertex, destination vertex, and the weight. The edges should be printed in the ascending order of their weights.

After you print all the edges included in the MST, then you should print two more lines. The next to last line should print the total cost of the minimum spanning tree. That is simply the sum of weights of all the edges included in the MST.

The final line should say either “CONNECTED” or “DISCONNECTED“. If the minimum spanning tree connects all vertices, then the line should print “CONNECTED”. If the minimum spanning tree does not connect all vertices, then the line should print “DISCONNECTED”.


An example output file for the input file described above is here. Note that the edges are printed in the ascending order of weights.

0510

2312

1614

1216

3422

4525

99

CONNECTED

(7) At the end of the program, you should print the following lines on the screen.

output written to hw3_result.txt.

running time: 0.073622 seconds

The actual running time printed will be different on each run. In order to print out the running time, use the function clock().

Once you implement the program, compare the execution time of your program with the given binary file (hw3_example) using the input file “input_large.txt”. (This file can be created by compiling and running the code “probgen.c”.) For this input file, your program should take less time compared to five times the time taken by the example binary file.

Similar to other homework, you should write a Makefile. The TA will build your code by running “make”. It should create a binary file, “hw3”.

Test-run the given binary code and write your program so that it produces the same result as the given binary code.

Your implementation should support up to 10,000 vertices and 50,000,000 edges.

3. Submission

You should submit your source codes and the Makefile. (You do not need to submit compiled binary files.) Combine your files into a zip file named cse3080_hw3_20200001.zip. The red numbers should be changed to your student ID. Submit your files on the cyber campus.

4. Evaluation Criteria

Your program should compile without problem and produce the binary file.

If the user does not give correct number of arguments, your program should print the usage message on the display and terminate.


If the input file does not exist, your program should correctly print an error message on the display and terminate.

When the user correctly executes the program with a command-line argument, your program should produce the result file “hw3_result.txt”.

The output must be correct.

The running time on the “input_large.txt” input file should be similar (on the cspro machine) to the given binary file “hw3_example”. Points will be deducted if the running time of your program is much larger (more than five times) than the time taken by “hw3_example”.

5. Notes

You must write your own code. You may discuss ideas with other students but must not copy their work. Similarly, you can find ideas on the Internet, but must not copy the code from the sources obtained from the Internet.

Our department uses a software that detects duplicate codes. Since the software uses an assembly code level detection, just changing the variable names will not bypass the software. Make sure you write your own code from the scratch. Then, you will have no problem.

Explained earlier, but your program should compile and run on the cspro machine. Make sure you check before you submit your work. The TA will download your code, run “make” and execute your binary files to check if they produce correct outputs.

6. Late Policy

10% of the score is deducted for each day, up to three days. Submissions are accepted up to three days after the deadline.
