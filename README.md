# Interview Preperation Day 3

## Q1. What are promises and why do we need them?
- Promise are use to handle async operation in JS. easy to handle callback hell, also use to handle the error. In promise there are Three stages, mainly
    1. Pending
    2. Resolve - (then method)
    3. reject - (catch method)
- initial stage of any promise is always pending.
##
    Example:
    function Sum(a,b){
    return new Promise((res,rej) =>{
        res(a+b)
        console.log("Promise Resolved!!!"); //Promise Resolved!!!
    })
    }
    Sum(2,3).then((data) =>console.log(data)) //5


## Q2. What is promise chaining?
- Promise chaining is a technique in JavaScript to execute multiple asynchronous operations in a specific order by chaining promises together using the .then method.
- Multiple .then method can be used in promise chaining.
##
    Example:
    function display(Num, timeout){
        return new Promise((res, rej) => {
            setTimeout(() => {
                console.log(Num);
                res('Promise Resolved...')
            }, timeout);
        })
    }
    display(1, 1000)
    .then(() => display(2, 2000))
    .then(() => display(3, 3000))
    .then(() => display(4, 4000))
    .then(() => display(5, 5000))
    .then(() => display(6, 6000))
    .then((data) => console.log('Promise Completed....'))
  
## Q3. What is the DOM?
- Document Object Model is basically a javascript mechanism by which we can change the document structure, style, and content.
- DOM helps with data representation of the objects that comprise the structure and content of a document on the web.
- Different methods in DOM are
    - Id - getElementById - return unique value
    - querySelector -       return unique value    
    - Class - getElementsByClassName 
    - tag Name - getElementsByTagName
    - querySelectorAll 
    - addEventListener - (event, callback function)

## Q4. What are closures? Give an example of closure
- A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment).
- Closure is the combination of minimum two functions.
- Inner function is able to excess the outer function variable but vise-varsa not possible.
- Outer function and inner function is going to create a Lexical environment.
##
    Example: 
    function outer(a){
        function inner(){
            return "Hello"
        }
        console.log(a);
        return inner;
    }

    let res = outer(10);
    console.log(res());

    Output:
    10
    Hello

## Q5. How many operators do we have in JS ?
We have 7 types of Operators in JavaScript -
1. Arithemic operators
    - Addition (+) 
    - Substraction (-)
    - Multiplication (*)
    - Division (/)
    - Modulous (%)
    - Expontial (**)
    - Increment (++)
    - Decrement (--)
2. Assignment Operator
    - Assign (=)
    - Addition Assign (+=)
    - Substraction Assign (-=)
    - Multiplication Assign (*=)
    - Division Assign (/=)
    - Modulous Assign (%=)
3. Bitwise Operator
    - Bitwise OR (|)
    - Bitwise AND (&)
    - Bitwise NOT (~)
    - Left shift (<<)
    - Right shift (>>)
4. Comparision Operator
    - Equal to (==)
    - Strict Equal to (===)
    - Not Equal to (!=)
    - Strict Not equal to (!==)
    - Greater than (>)
    - Less than (<)
    - Greate than equal(>=)
    - Less than equal(<=)
5. Logical Operator
    - AND (&&)
    - OR (||)
    - Not (!)
6. Ternary Operator
    - (Condition) ? "Execute True Condition" : "Execute False Condition"
7. typeof Operator
    - return datatype

## Q6. What are objects in javascript?
Objects is a Non-premitive data type in which data is stored in the form of Key-Value pair seperated by colon. Key is also called as Properties.

    Example:
    const student ={
        name: "Sahil",
        age: 23,
    }
    console.log(student);

    Output:
    { name: 'Sahil', age: 23 }

