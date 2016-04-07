
This program simulates the FloodMax Leader Election algorithm in an Asynchronized network in Java. 
Threads are used to simulate each process in a Distributed Asynchronous environment. 
The processes communicate with each other using Thread Safe Blocking Queues.
None of the processes know the number of processes in the distributed system and only know their respective IDs and neighbours in the network. 
All the processes execute the same code.


--------------------------------------------------------------------------------------------------------------------------------------------

Steps to Execute

1) The project contains source code, README.txt, sample connectivity text files.
2) While executing the program the connectivity text file should be in the same folder as the java files.

	Run the commands in the following order.
	3) javac Master.java
	4) java Master conn9.txt
	5) Output should be visible on the console. The leader will announce that he is the leader and each process will display that it has found the leader.
	6) All threads will terminate.

--------------------------------------------------------------------------------------------------------------------------------------------------------

Sample Input 

conn9.txt:
9
1 2 3 4 5 6 7 8 9
0 1 1 0 0 0 0 0 0
1 0 1 0 0 1 0 0 0
1 1 0 1 1 0 0 0 0
0 0 1 0 1 1 0 0 0
0 0 1 1 0 0 1 0 0
0 1 0 1 0 0 1 1 0
0 0 0 0 1 1 0 1 1
0 0 0 0 0 1 1 0 1
0 0 0 0 0 0 1 1 0

--------------------------------------------------------------------------------------------------------------------------------------------------------

Sample Output:
2--->1
3--->1
3--->2
4--->3
5--->3
5--->4
6--->2
6--->4
7--->5
7--->6
8--->6
8--->7
9--->7
9--->8
9 I'm leader
8 Leader is: 9
8 Parent:-------------------------------->ID:9
8 Children:------------------------------>[ID:6]
7 Leader is: 9
7 Parent:-------------------------------->ID:9
7 Children:------------------------------>[ID:5]
6 Leader is: 9
6 Parent:-------------------------------->ID:8
6 Children:------------------------------>[ID:4, ID:2]
5 Leader is: 9
5 Parent:-------------------------------->ID:7
5 Children:------------------------------>[ID:3]
4 Leader is: 9
4 Parent:-------------------------------->ID:6
4 Children:------------------------------>[]
2 Leader is: 9
2 Parent:-------------------------------->ID:6
2 Children:------------------------------>[]
3 Leader is: 9
3 Parent:-------------------------------->ID:5
3 Children:------------------------------>[ID:1]
1 Leader is: 9
1 Parent:-------------------------------->ID:3
1 Children:------------------------------>[]
Completed!!

