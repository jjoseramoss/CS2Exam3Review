# Recursion
1. Recursion – Be prepared to explain any of the following in simple 
 terms: <br>
     a. What are the parts that make up a recursive algorithm? 

        1. Base Case: This is the simplest version of the problem that can be solved
            directly without recursion. It stops the recursion from continuing
            endlessly. Think of it as the "exit point" for the recursion

        2. Recursive Case: This part breaks the problem into smaller versions of 
            itself abd calls the same algorithm to solve those smaller problems. The 
            recursive case continues to call itself with simpler inputs until it 
            reaches the base case.

    What role does each of these play in solving a large complex problem?

        The recursive case helps divide a complex problem into smaller, more manageable problems. The algorithm keeps working on simple versions of the problem, gradually reducing its complexity. Once it hits the base case, the problem-solving process stops and the results from the smaller problems are combined to solve the original large problem.
        
    
     b. What is the difference between an iterative and a recursive 
         solution?

         An iterative solution solves a problem by repeating a set of steps in a loop, like a for or while loop. It keeps running the same instructions until the problem is solved. In contrast, a recursive solution solves the problem by calling the same function repeatedly within different arguments. Each call solves a smaller version of the problem until the base case is reached

2. Recursion (code) – Be able to identify the following for a recursive 
function, such as the one shown below: <br>
    a. How many recursive calls are made to the function counter() in 
        the example below?
        
       There are 9 recursive calls since 45/5 = 9 and the recursive function calls the function while subtracting 5 to num until it reaches 0

    b. What is the output?
        
        45 40 35 30 25 20 15 10 5 0

    c. Look at each statement in the function definition and note what 
        each statement’s significance is in recursion (you can disregard 
        the “cout” statements, but everything else is needed here.)

        The first line shows the function name and the parameter num which is reduced every time the function is called

        the second line shows the base case as this will end the recursion allowing the function to go back through each call and end

        the third important line, recursively calls the function and reduces num by 5 in order to get closer to the base case

    d. (Hint: your answers from #1 should connect to your answers in 
        part c of this problem

    ```
        #include <iostream>
        using namespace std;

        void counter(int num) {
        if (num == 0)
            cout << num << " ";
        else {
        cout << num << " ";
            counter(num - 5);
        }             
        }
        int main() {   
        counter(45);                
        return 0;                     
        }

    ```