# Introduction
In this section, we'll begin with the basic of programming; the what, when and how's. I'll start by addressing some of the fundamentals such as functions, variables, data types, logical operations including if, else, for, switch, etc. I'll then move into definitions such as what `IDE` and `compiler` means. I'll cover each topic more in depth in subsequent sections, but for now, let's just get to know what all of this stuff means!

--- 

## Outline
* [1. Functions](#Functions)
* [2. Variables](#Variables)
* [3. Data Types](#Data&nbsp;Types)
* [4. Logical Operations](#Functions)
* [5. Definitions](#Definitions)

---

## Functions
According to Wikipedia, functions (or subroutines) are defined as 

> A sequence of program instructions that performs a specific task, packaged as a unit. This unit can then be used in programs wherever that particular task should be performed".

Functions may also be referred to as a procedure, routine, subroutine or method. To avoid confusion however, we'll stick with function, although "methods" will be discussed later as they have a slightly different meaning in object-oriented programming.

---

## Variables 
Wikipedia says a variable is a:

> Storage address (identified by a memory address) paired with an associated symbolic name, which contains some known or unknown quantity of information referred to as a value. 

Brain hurting yet? Let me give a more friendly definition of my own phrasing: 

> A thing that represents data of different types.

Ok I'm probably making every computer scientist and mathematician a personal enemy with this definition, but in practive, using variables is no where near as scary as what the formal definition would have you think. Let's take a quick peak shall we?

```go
var a = 10 
var name = "John" 
var no = false
var yes = true 
```

See, easy, right? We'll still want to understand what's going on under the hood in order to write more efficient programs, but the majority of your day to day programming will involve writing variables like in the example :) 

--- 

## Data Types 
Data types are to variables as an actor is to movies; variables can be many different things but only one thing at a time. The 6 most common data types are:

| Type        | Examples                                        | Common keyword    |
|-------------|:------------------------------------------------|:------------------|
| `Byte`      | 'a', 'b', 'c', '!', '$', '?', '1', '9'          | `byte`            |
| `String`    | "hello world", "John", "I love programming!"    | `string`          |
| `Integer`   | 1, 2, 25452, -23, 0x100, 0xA, 0xFFFFFF          | `int`             |   
| `Boolean`   | true, false                                     | `bool`            |
| `Float`     | 3.14, -59.15698                                 | `float`           |
| `Array`     | [10,11,12], ["hello","world"]                   | `Array`, `[]`     |


> **Note** the values `0x100, 0xA, 0xFFFFFF` are [Hexadecimal](https://simple.wikipedia.org/wiki/Hexadecimal) values. These are often used over numeric values as each hex character represents more data that decimal. In fact, just two hex characters `FF` can represent numbers as large as `255`! As you continue your journey, you'll see hex everywhere, but practically speaking, you're typically fine using decimals for your daily programming tasks.

--- 

## Logical Operations 
Logical operations are the guts of programming. They allow us to repeat tasks and to make decisions in code. All logical operations can be reduced down to a boolean (true or false) value. This is what gives us the 0's and 1's in binary.

Logical operations typically consist of a programming `construct`, logical `operators` and `variables`. `Constructs` may include (but not limited to):

* `if`
* `else`
* `then`
* `for`
* `switch`
* `case` 

While `operators` include (but not limited to):

| Definition                | Operator  |
|---------------------------|:----------|
| `not`                     | `!`       |
| `equals`                  | `==`      |
| `not equals`              | `!=`      |
| `greater than`            | `>`       |
| `less than`               | `<`       |
| `and`                     | `&&`      |
| `greater than or equal to`| `>=`      |
| `less than or equal to`   | `<=`      |

---

# Definitions
The world of programming is vast. After 20 years of doing it I've came to realize there are no boundaries as you will never know all there is to know. However, there are many keywords you're going to see over and over again throughout your programming career. Here are some of them.

### `Terminal`
Also referred to as a `command line`, terminals allow us to interact with a computer without the use of graphical user interfaces or [GUI](#GUI)s. We interact with terminals by telling it what we want to do via typing as opposed to clicking on buttons or menus. Some [cli](#cli) applications however, do allow for mouse interactions. 

Example:
```bash
> cd my-projects
> pwd 
> /users/john/my-projects
> ls 
> notes.md essay.md outline.md cat-picture.jpg
```

- `cd` means "change directory" and allows us to navigate folders in the terminal.
- `pwd` means "print working directory" which allows us to see exactly what folder we are in and where it's located.
- `ls` means "list" and is used to show what files and folders we have available to us within a folder.

### `CLI`
Stands for `command line interface`. CLI applications are ones that run within the [terminal](#terminal).

Example:

```bash
> cat helloword.txt 
> Hello world! This is the contents of the helloworld.txt file that the cat cli app will write to the terminal!
```

### `GUI`
A GUI or `graphical user interface` is the most typical software you are use to using. Games, web browsers, email applications, messaging apps and even web sites are all examples of GUIs.

### `IDE` 
Or `integrated development environment` is a piece of software that allows us to write, build and [debug](#debugging) our code without needing to use any other software. All modern IDEs can show us when we've made a mistake in our code and can even help us figure out what we need to do next. While most IDEs are [GUI](#GUI) applications, there are [terminal](#terminal) based applications as well including:

* `vim`
* `emacs`
* `micro`

The terminal based development tools can be extremely useful for many scenarios. For example, when remotely connected to a `linux` machine which often have `vim` installed by default, we can run it to edit files.

### `Compiler`
A compiler is a specialized piece of software that takes our `source code` and converts it into an application that the computer can run. Compilers do all of the heavy lifting of analyzing your code, optimizing it and changing it into machine code.

### Debugging 
Debugging is a process in which you step through your programs code as it's running in order to inspect what's going on at each step. Debugging works by stopping the execution of the program whenever a `breakpoint` that you set ahead of time in your code, is found. Modern debuggers will let you see exactly what values all variables are currently set to as well what parts of the code or getting executed based on the logic you've implemented.

Example: Your application is outputting 10 when you expect 15. You find the function that takes the variables and adds them together. You check the current values of the variables and both look correct. You step ahead where the math operation is happening. You hover over the line with your mouse and see that the calculated value is 10...And then you see the bug!

```go
// Add takes a and b and returns the sum.
func Add(a, b int) {
    return a + a // Our bug! a + a should be a + b !!
}

Add(5, 10)
```

### `Loosely Typed Language`
A strongly types language is the opposite of a [strongly types language](#`strongly&nbsp;typed&nbpsp;language`) in that variables don't need to be declared with a type assigned to them and functions don't need to be declared with `return types`. For example, in `javascript` you can declare a variable with any value without needing to tell it what [data type](#data&nbsp;types) it is ahead of time. It does the work for you. Great huh? Well there's a downside to this. It makes the code slow, really, really slow. 

However, in programming when we talk about slow, we typically are talking in the realm of milliseconds (fractions of a second) differences in processing time. The issue is when we are performing the same operations thousands of times a minute or even a second. Google for example gets thousands of searches a second and is able to find millions of entries in a second or less. The reason it's able to do this is in part because of how fast the underlying programming languages can execute.

The other issue this creates is programmer error. Because error wont occur until after the code is running, it's extremely easy to mix the wrong types of data together. For example:

```javascript 
function add(a, b) {
    return a + b
}

var a = 10
var b = "hello"

add(a, b)
```

Now because `javascript` will analyze this automatically, instead of getting add returning the sum of a and b, it will return the string value `"10hello"` which is obviously not what we want.

Variables in loosely typed languages can also switch types whenevever. For example:

```javascript
var x = 10 
x = "hello"
x = 3.14 
x = false
x = []
```

This can lead to all sorts of bugs in your application!

### `Strongly Typed Language`
A strongly types language is the opposite of a [loosely typed language](#`loosely&nbsp;typed&nbsp;language`) in that data types are either required to be declared by the programmer or can sometimes be `inferred` while `compiling` the code. For example, in the `Go` programming language, both styles are perfectly valid:

```go
x := 10 

var y int 
y = 10
```

When compiling this code, the `Go compiler` will see that you are declaring `x` as a new variable and assigning the value of `10` to it. Because 10 is an integer type, the compiler will automatically declare x as being of type `int`.

The important thing to note is that in strongly typed languages, variables can not change from their original data type, not typically anyway. There are some exceptions to the rule, but in general, if you declare x as an integer, it will remain an integer and can not be changed into any other data type while the app is running.

Strongly typing means coding can be slower and the `syntax` may be a little more verbose, however, it often leads to far superior performance, less bug prone and easier for future programmers (even yourself) to reason about. It removes the guesswork which is of vital importance to programmers.

### `Go` 
Is a strongly typed programming language created by Google.

### `Javascript`
Is a loosely typed programming language that was originally intended to be ran for simple things in websites but has since became a major language in both complex websites such as Facebook as well as `backend` and `cli` applications.

### `Backend`
See [Server](#server)

### `Server`
A server is an application (or part of an application) that processes requests from a [client](#client). For example, a website is a `client` which talks to a `server` in order to do things such as like a Facebook page, get the latest tweets, process a form submission, complete a transaction, etc.

Any time you have a relationship where one application depends on another to obtain a piece of data or to do something, you have a `client-server` relationship.

### `Client` 
A client is an application or a part of an application in which talks to a [server][#server]. Any time you have a relationship where one application depends on another to obtain a piece of data or to do something, you have a `client-server` relationship.

