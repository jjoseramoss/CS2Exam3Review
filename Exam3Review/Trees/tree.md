# Trees

1. Trees - What is the difference between a linked list and a tree-based 
data structure? How are they similar? <br>
    
    Differences:
        A linked list is linear, the nodes are connected sequentially, while a tree is hierarchical, nodes branch out from a root.
        Linked Lists are traversed sequentially, while trees can be traversed in multiple ways.
        Linked Lists have at most one next node per node, but trees can have multiple children

    Similarities:
        Both are collections of nodes linked via pointers, both dynamically allocate memory and grow as needed, both use recursive algorithms for operations

2. Trees – Review the tree based data structures that we introduced in 
class (there were only two so far) <br>

    Binary Tree: 
        Each Node has at most two children (left and right)

    Binary Search Tree: 
        A binary tree where the left child contains smaller values and the right children contains larger values.

3. Binary Search Tree (code) – See the list of values below. Be 
prepared to complete any of the following with both plain language 
explanations and code:<br>

    {14 8 -10 -20 3 -5 -12 6 -7 -16} <br>

    *Draw the resulting Binary Search Tree, and identify things such as the 
    number of leaf nodes, the level of any given node (for example, the level of -
    5) and the height and size of the tree.

                                    14
                                   /  
                                  8                 Level of -5: 4
                                 /                  # of leaf nodes: 3
                            -10                     Height: 5
                      -----/   \                    Size: 10
                    -20        3
                       \      / \
                      -12    -5  6
                       /      /
                      -16      -7
    * Given a search value (for example, zero) be prepared to explain in specific 
    steps how to determine whether or not the value is present in the tree 
    (remember that we start with a root node, which can only see its children!)
    *If the value is not present, explain the steps needed to insert the node
    *You can assume that any code task you are given for your binary search 
    tree will contain Nodes with a format like the one shown below:

    1. Start at the root node
    2. Compare target val with the current node's value, in this case 0
        - If Smaller then go left
        - If larger go right
    3. Stop if the value is found or if you reach a nullptr - these are your base cases
    4. Insert - If not found, Place a new node at the first nullptr in the appropriate position



# Class Notes

Every Binary tree is made of nodes

Every node can point to up to 2 child nodes
    anything a node points directly to is a child
    The parent node is the node that points to this node
instead of a "head" node, we call the top the "root"
every node has a "level"
    how many transitions from the root do we need to 
    reach the node
    Level 0 is the root of the tree
the height of a tree is the maximum level of any node
A "leaf node" is a node that has no children

the rules for BINARY TREE
    every binary tree has 1 root
    every node has up to 2 children


the rules for a BINARY SEARCH TREE
    is a binary tree, ....
    every node to the left of a parent node 
        must be LESS THAN parent
    every node to the right of parent node
        // must be GREATER THAN parent