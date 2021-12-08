# Backtrack-2.0
The same problem as in Backtrack is solved using Graph implementation. BFS and DFS algorithms are used to find the path efficiently.<br><br>
A particular ‘RPA’ firm is in the process of developing a restaurant which has bot waiters. Bot needs to deliver the food from the specified exit door, of the kitchen with multiple exit doors to the specified table.
The restaurant has blocked areas where Bot cannot move and the passages where it can move. The layout of restaurant can be rectangular or square.
Layout map can be considered as a matrix of cells where cell with ‘0’ represents the passage and cell with ‘1’, the blocked area. Bot has memorised this map in a particular format for faster processing. Given a particular table location bot needs to find the path from the kitchen, starting from the specified exit door to the table to serve the customer. Bot has a constraint it can move only in either right or down direction one step at a time (i.e. only to the adjacent cell in right or down direction provided it is not blocked) without preference to any particular direction.
Layout matrix is stored in the file input.txt
You need to provide the code that helps the bot with the path form specific exit door of the kitchen to the mentioned table if there exists the one. If multiple paths exists your code should find any one.
<br>
Implementation
Your code should provide the following functionalities 1. Readmap
Layout matrix consists for ‘0’ (allowed for moving) and ‘1’ (Blocked area)
You need to interpret layout matrix as a directed graph .Each vertex in this graph has max degree 2. For each vertex, vertex id and location (rowno, columnno) of the layout matrix should be maintained. Vertex id numbering should be row wise.<br>
0111<br>0010<br>0011<br>1000<br>
Your code should read the layout matrix from the file input.txt (file reading) and store it as a graph using adjacency list representation. List should be created using “insert at front option” only.<br>
2. Findpath
Help bot to find path from the start point to the end point if one exists.
You should access data from the created adjacency list representation and using graph traversal techniques (BFS and DFS) determine the path from start point to end point if it exists. Give your comments on the path generated by BFS and DFS Traversal techniques.
BFS: Breadth First Search
DFS: Depth First Search<br>
3. Storepath
Your program should generate output files outbfs.txt and outdfs.txt<br>
If path exits, program should store coordinates of the path given by BFS traversal in outbfs.txt and DFS traversal in outdfs.txt (each coordinate on new line same as done for Assignment I). If no path exists ‘-1’ should be stored in output file.
<br>
Input file description
First line indicates the start point for the Bot, second line termination point, 3rd line onwards represent the layout matrix.<br>
Sample Input file: 00<br>
33<br>
0111<br>
0010<br>
0011<br>
1000<br>
