# Traversal
Data structure can be vary such as Binary Trees and Graphs. Once established, these objects work like a database, their content can be explored through a process called traversal. In this repo, we will examine popular traversal techniques which is BFS (Breadth First Search) and DFS (Depth First Search)

## Depth First Search
#### Pseudocode
- Graph
    
    ```swift
    DFS(G,n) {
    	n.visited = true
    	print(n)
    	if G.hasNeighbours {
    		for c in G.neighbours(n) do {
    			if !c.visited {
    				DFS(G,c)
    			}
    		}
    	}
    }
    ```
- Tree
    ```swift
    T -> Key : Node
    	 left : T
    	 right : T
    
    DFS(T) {
    	if T.key == nil {
    		return
    	} 
    
    	key.visited = true
    	print(key)
    
    	if (T.left !=nil) {
    		DFS(T.left)
    	}
    
    
    	if (T.right != nil) {
    		DFS(T.right)
    	}
    }
    ```
## Breadth First Search
#### Pseudocode
- Graph
    ```swift
        BFS(G,startingNode) {
    	 Queue queue = Queue()
    	 queue.enqueue(startingNode)
    
    	 startingNode.visited = true
    	 print(startingNode)
    
    	 while(!queue.isEmpty) {
    	 	node = queue.dequeue
    
    	 	for n in node.neighbors {
    	 		if !n.visited {
    	 			queue.enqueue(n)
    	 			n.visited = true
    	 			print(n)
    	 		}
    	 	}
    	 }
    }
    ```
- Tree
    ```swift
    BFS(G,startingNode) {
    	 Queue queue = Queue()
    	 queue.enqueue(startingNode)
    
    	 startingNode.visited = true
    	 print(startingNode)
    
    	 while(!queue.isEmpty) {
    	 	node = queue.dequeue
    
    	 	for n in node.childrens {
    	 		if !n.visited {
    	 			queue.enqueue(n)
    	 			n.visited = true
    	 			print(n)
    	 		}
    	 	}
    	 }
    }
    ```
