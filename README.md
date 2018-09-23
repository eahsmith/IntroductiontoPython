# IntroductiontoPython
Big Data and Social Analytics Module 1: Exercise 1: Printing strings Exercise 2: Rolling dice Exercise 3: Coin flip distribution
{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<div align=\"right\">Python 3.6 Jupyter Notebook</div>"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Introduction to Python"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Your completion of the notebook exercises will be graded based on your ability to do the following:\n",
    "\n",
    "> **Understand**: Do your pseudo-code and comments show evidence that you recall and understand technical concepts?\n",
    "\n",
    "> **Apply**: Are you able to execute code (using the supplied examples) that performs the required functionality on supplied or generated data sets?"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "#### Notebook objectives\n",
    "By the end of this notebook you will be expected to:\n",
    "> \n",
    "  - Identify **basic concepts of programming**;\n",
    "  - Understand **Python syntax**;\n",
    "  - Distinguish between the different **native data types** used in Python;\n",
    "  - Use **flow control structures** to implement **conditional and repetitive logic**;\n",
    "  - Understand **functions** as a block of organized, reusable code that is used to perform a single, related action, as being necessary for improving the modularity of an application, as well as allowing for code reuse within and across applications; and\n",
    "  - Understand a Python **package** as a file consisting of Python code that defines functions, classes, variables, and may also include runnable code. You should be able to **import** a Python package or specific functions from a package.\n",
    " \n",
    "####  List of exercises\n",
    ">   - Exercise 1: Printing strings.\n",
    "  - Exercise 2: Rolling dice.\n",
    "  - Exercise 3: Coin flip distribution."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Notebook introduction\n",
    "\n",
    "In the Orientation Module, you were given a number of links that provided additional Python documentation and tutorials. This section will serve as a summarized version of useful commands that are needed to get non-technical users started, and equip them with the basics required to complete this course.\n",
    "\n",
    "This course is not intended to be a Python training course, but rather to showcase how Python can be utilized in analysis projects and, more specifically, in analyzing social data. You will be provided with links that you can explore in your own time in order to further your expertise. You are welcome to offer additional suggestions to your peers in the online forums.\n",
    "\n",
    "You should execute the cells with sample code and write your own code in the indicated cells in this notebook. When complete, ensure that you save and checkpoint the notebook, download a copy to your local workstation, and submit a copy to the Online Campus.\n",
    "\n",
    "You can also visit theÂ [Python Language Reference](https://docs.python.org/3/reference/index.html)Â for a more complete reference manual that describes the syntax and \"core semantics\" of the language.\n",
    "\n",
    "> **Note to new Python users**: \n",
    "\n",
    "> This notebook will introduce a significant amount of new content. You do not need to be able to master all of the components, but you are urged to work through the examples below, and to attempt following the logic. In this notebook, you will be introduced to Python syntax. The second notebook in this module will start to introduce various components of data analysis basics, and the third will guide you through a basic example from beginning to end. The focus will shift from programming to subject-related examples in subsequent modules."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<div class=\"alert alert-warning\">\n",
    "<b>Note</b>:<br>\n",
    "It is strongly recommended that you save and checkpoint after applying significant changes or completing exercises. This allows you to return the notebook to a previous state should you wish to do so. On the Jupyter menu, select \"File\", then \"Save and Checkpoint\" from the dropdown menu that appears.\n",
    "</div>"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# 1. Introduction to Python programming"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Python is generally [defined](https://docs.python.org/3/faq/general.html#what-is-python) as a *high-level, general-purpose, interpreted, dynamic computer programming language*. \n",
    "\n",
    "Letâ€™s try to break this statement down, for those new to computer programming. High-level means that we can express instructions that computers are able to execute in a language that is closer to a human language, and not the machine language that a computer requires to run the instructions. The interpreter is a program that converts the high-level programming instructions into low-level programming instructions that a computer understands. Dynamic means that they do not enforce or check type-safety at â€œcompile-timeâ€, in favor of deferring such checks until â€œrun-timeâ€. This has many advantages, including lower development costs, rapid prototyping, and flexibility required by specific domains, such as data processing and analysis. This makes Python a perfect language for this course, as it is easy to understand (the expressions used are very similar to day-to-day conversations), it has a simple syntax, and provides objects that are appropriate for data processing and analysis.\n",
    "\n",
    "Because itâ€™s a programming language, there are some basic computer science concepts that are important to understand before you start coding.\n",
    "\n",
    "## 1.1 Basic concepts\n",
    "\n",
    "### 1.1.1 Variables\n",
    "Variables are the backbone of any program and, therefore, the backbone of any programming language. A variable is used to store information to be referenced and manipulated in a set of instructions commonly referred to as a computer program. Variables also provide a way of labeling data with a descriptive name, in order for programs to be understood more clearly by the reader and ourselves (recall high-level from above). It is helpful to think of variables as containers that hold information. Their sole purpose is to label and store data in the computer's memory. This data can then be used throughout a program.\n",
    "\n",
    "Variables can store various pieces of information such as the name of a person, that person's age or weight, or their date of birth. Each of these pieces of information contain different types of information. The data type of the variable containing the name of a person would be a string, while the age is stored as an integer, and the date of birth as a datetime object. Fortunately, in Python, unlike in Java or C, you do not need to tell the computer what type a variable is before you assign an object to it. This means that you can begin your program by referring to your name, say, as â€œXâ€.\n",
    "\n",
    "    >>> X = 'Mary'\n",
    "    \n",
    "In the middle of your program, you might change your mind, and reassign your â€œXâ€ variable to your age.\n",
    "\n",
    "    >>> X = 21\n",
    "\n",
    "This provides you with flexibility that you can exploit to quickly test ideas without worrying that your code will break when executed. As with anything, \"with great flexibility, comes great responsibility!\" It is best practice to use names that are intuitive for the data that the variable stores. The only exception is using names which are reserved by the programming language, called **keywords**. Keywords define the language's rules and structure, and they cannot be used as variable names. Inside Jupyter, a Python reserved name is highlighted differently to other names, as will shortly become clear.\n",
    "\n",
    "A variableâ€™s type also defines what you can do, and the behaviors you can expect, when you perform certain operations on it. This is illustrated later in this notebook.\n",
    "\n",
    "### 1.1.2 Control structures\n",
    "When we put together a set of instructions for the computer to execute, the computer reads the instructions sequentially. This is known as the \"flow of the code\". However, it is often the case that an instruction in the code requires a decision to be made. For example, say you have written a program to accept interns into your organization. To comply with the labor regulations governing your organization, you ask each candidate to enter their age amongst other details. Before accepting them as an intern, your program checks if the person's age is within the prescribed limits. If not, the application of a potential intern is rejected. Such decision points that affect the flow of the code occur frequently in computer programming and are known as **flow control structures**. [Specifically](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-096-introduction-to-c-january-iap-2011/lecture-notes/MIT6_096IAP11_lec02.pdf):\n",
    "\n",
    "> A control structure is a block of programming that analyzes variables and chooses a direction in which to go based on given parameters. The term flow control details the direction the program takes (which way program control â€œflowsâ€). Hence it is the basic decision-making process in computing; flow control determines how a computer will respond when given certain conditions and parameters.\n",
    "\n",
    "Control structures make the programs function properly and, without control structures, your programâ€™s code would only flow linearly from top to bottom. Changing what action a program takes, based on a variable's value, is what makes programming useful. Below, you will be introduced to the different control structures available in Python.\n",
    "\n",
    "### 1.1.3 Data structures\n",
    "A data structure is a particular way of storing and organizing data in a computer so that it can be used efficiently. Previously, you were introduced to the concept of variables using a person's name, age, and date of birth as examples. Imagine doing that for everyone who is enrolled in the MIT Big Data and Social Analytics certificate course. That would be a lot of variables that you would struggle to keep track of. A data structure is a way to get around having to create millions of variables. Python implements many data structures that you will be using, such as lists, dicts, tuples, and sequences. Moreover, other data structures can be built on top of these for efficiently working with data. In Python, the NumPy and Pandas modules provide data structures that are intuitive and expressive enough for many of our needs in data analysis.\n",
    "\n",
    "### 1.1.4 Syntax\n",
    "Each programming language is designed and implemented differently, and using it requires adherence to its syntax, which is the set of rules that define the combinations of symbols that are considered to be correctly-structured programs in that language. When these rules are followed, the programming language can understand your instructions and, therefore, you are able to create software that can be run. If you do not adhere to the rules of programming languagesâ€™ syntax, you will unfortunately run into errors and your programs will not be executed. As it turns out, the syntax of any programming language tends to be the biggest obstacle many people face when being introduced to programming for the first time, or when learning a new programming language. (Note that syntax errors are only one type of error among many that are possible.) Fortunately, Python will correctly identify syntax errors as it encounters them. This will be useful when trying to find errors in your code. Some key things to remember when using Python are highlighted below.\n",
    "\n",
    "**Case sensitivity**\n",
    "> All variables are case-sensitive. Python treats â€œnumberâ€ and â€œNumberâ€ as separate, unrelated entities.\n",
    "\n",
    " \n",
    "**Comments**\n",
    "> Commented lines start with the hashtag symbol <font color='#008080'><b> # </b></font> and are ignored when interpreting the code at run-time.\n",
    "\n",
    "**Indentation**\n",
    "> Code blocks are demarcated by their indentation. In particular, **control structures** end with a colon <font color='brown'><b> : </b></font> at the decision point. Code blocks indicating action that must be taken when the decision evaluates to \"True\" are demarcated by indentation. \n",
    "\n",
    ">> Note:  **Spaces and tabs do not mix**<br>\n",
    "> Because whitespace is significant, remember that spaces and tabs don't mix, so use only one or the other when indenting your programs. A common error is to conflate them. While they may look the same during editing, the interpreter will read them differently, and it will result in either an error or unexpected behavior. Most decent text editors can be configured to let the tab key emit spaces instead."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "In summary, this section described what a variable is, how you can store information in it, and then retrieve that information at a later stage. The variable can have a name, and this name is usually informed by the kind of content youâ€™ll be storing in the variable. So, if youâ€™re storing your name in the variable, you would name the variable â€œyourNameâ€. You would not **have** to give it that name, you could name the variable â€œWowImProgrammingâ€, but that wouldnâ€™t make much sense considering you are trying to store a personâ€™s name. Finally, variables have types, and these types are used to help us organize what can and cannot be stored in the variable. \n",
    "\n",
    "> **Hint**: Having a type will help to open up what kinds of things we can do with the information inside the variable. \n",
    "\n",
    "\n",
    "> **Example**: If you have two integers (letâ€™s say 50 and 32), you would be able to subtract one variable from the other (i.e., 50 â€“ 32 = 18). But, if you had two variables that stored names (e.g., â€œTrevorâ€ and â€œGeoffâ€) it wouldnâ€™t make sense to subtract one from the other (i.e., â€œTrevorâ€ â€“ â€œGeoffâ€), because that does not mean anything. \n",
    "\n",
    "Therefore, types are a powerful thing, and they help you make sense of what you **can** and cannot do with your variables."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# 2. Programming with Python\n",
    "\n",
    "Now that the basic concepts have been introduced, letâ€™s make these concrete using illustrative examples. This notebook uses Jupyter's code cells (in light gray background) to demonstrate these ideas. As you learned in the Orientation Module, you can execute instructions in a code cell and the output will be displayed below the cell, where applicable.\n",
    "\n",
    "In most cases, a comment is included in the very first line of the cell to help in following the material. A comment is any line in the set of instructions that is preceded by a hashtag symbol. Inside Jupyter, once you have used the comment indicator, the line is highlighted in a different color and the font italicized, which is a very helpful visual aid for both readers and developers. See the example below:\n",
    "\n",
    "> **Note**:\n",
    "\n",
    "> The code cell below will not produce any output when executed."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 1,
   "metadata": {},
   "outputs": [],
   "source": [
    "# I am a comment and I'm ignored by the interpreter."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 2.1 Strings"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Python works with \"values\" that can take different forms depending on the data type. For example, both a person's first name and age constitute different, valid values inside Python.  "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "'Bob'"
      ]
     },
     "execution_count": 2,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# A valid value of type string that can be manipulated.\n",
    "\"Bob\""
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "'Bob'"
      ]
     },
     "execution_count": 3,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Alternatively, you can also use single quotes to specify the value.\n",
    "'Bob'"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "You can use the function â€œtype()â€ and include the name of the value in between the parentheses to find out what type the value is. (Functions in Python are explained in more detail later in this notebook.)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "str"
      ]
     },
     "execution_count": 4,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Find the type of a valid value that can be manipulated.\n",
    "type('Bob')"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 68,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "float"
      ]
     },
     "execution_count": 68,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a=3.75\n",
    "type(a)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "From the above, you can see that our value ```'Bob'``` has type ```str```. The value of a string data type is a sequence of characters. Strings are typically used for text processing.\n",
    "You can perform concatenation and a number of other functions on strings."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "'He is Bob'"
      ]
     },
     "execution_count": 5,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# String concatenation using the '+' operator.\n",
    "'He' + ' ' + 'is' + ' ' + 'Bob'"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "3"
      ]
     },
     "execution_count": 6,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# How long is the string 'Bob'.\n",
    "len('Bob')"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 7,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "'BobBobBob'"
      ]
     },
     "execution_count": 7,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Print 'Bob' 3 times with no space.\n",
    "'Bob'*3"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "'B'"
      ]
     },
     "execution_count": 8,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Get the 1st element of the string 'Bob'.\n",
    "'Bob'[0]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 9,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "'o'"
      ]
     },
     "execution_count": 9,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Get the second element of the string 'Bob'.\n",
    "'Bob'[1]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "'b'"
      ]
     },
     "execution_count": 10,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Get the third element of the string 'Bob'.\n",
    "'Bob'[2]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 11,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "'b'"
      ]
     },
     "execution_count": 11,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Get the last element of the string 'Bob'.\n",
    "'Bob'[-1]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 12,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "'o'"
      ]
     },
     "execution_count": 12,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Get the second last element of the string 'Bob'.\n",
    "'Bob'[-2]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 13,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "'BobBobBo'"
      ]
     },
     "execution_count": 13,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Slicing: Remove the last element of the string 'BobBobBob' and return the remainder of the string. \n",
    "('Bob'*3)[0:-1]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 2.2 Integers"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Another example of a value is Bobâ€™s age. Assuming Bob is 40 years old, the value can be specified as follows:"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 14,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "40"
      ]
     },
     "execution_count": 14,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# A valid value of type integer. \n",
    "40"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 15,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "int"
      ]
     },
     "execution_count": 15,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Type of a valid value for Bob's age.\n",
    "type(40)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Note the difference in how the two values are specified: for string values the name is included between single or double quotes, whereas this is not needed for the age value. Had quotes been used in the latter, it would have expressed a different value of a different type."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 16,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "'40'"
      ]
     },
     "execution_count": 16,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# A valid value but not of type integer.\n",
    "'40'"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 2.3 Boolean"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Let's introduce three new ideas with this example: how to compare two values, another valid data type in Python, and the concept of casting. First, letâ€™s compare the two values (40 and '40') to see if they are of the same type."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 17,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "False"
      ]
     },
     "execution_count": 17,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "type(40) == type('40')"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "What is happening here? We have used an operator (```==```) that accepts one value on either side, and compares these values to see if they are the same. The values being compared in this case are not ```40``` and ```'40'```, but their corresponding value types (i.e., integer, string, etc.). (If our intention is to compare the original values we would have used ```40 == '40'```)\n",
    "\n",
    "What type is the resulting False value?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 18,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "bool"
      ]
     },
     "execution_count": 18,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Type of value from a comparison.\n",
    "type(type(40) == type('40'))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "The \"False\" value is of the â€œBooleanâ€ type, which is another fundamental data type in programming. Boolean values can only take two values: \"True\" or \"False\".\n",
    "\n",
    "It is often the case that, instead of working with the native data type, such as the Boolean data type that you have just seen, you want to use a different but equivalent data type. For example, if you accept that a \"False\" value represents the lack of something in a given context, you may want to represent that as an integer with the value 0. This is achieved using the concept of **casting**, which allows certain data types to be cast as a different type. In Python, you cast a value by calling the type that you want to cast it to, and including the value as an argument to that call. Thus, in this case, you achieve the following."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 19,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "0"
      ]
     },
     "execution_count": 19,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Casting a bool to an int.\n",
    "int(type(40) == type('40'))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 2.4 Floating point numbers"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Floating point numbers are numbers that contain floating decimal points."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 20,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "2.6"
      ]
     },
     "execution_count": 20,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Example of a floating number.\n",
    "2.6"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 21,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "float"
      ]
     },
     "execution_count": 21,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Find the type of a floating number.\n",
    "type(2.6)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Remember that data types define what operations are allowed between values of the same type. However, certain data types, such as integers and floating numbers, can be used together in expressions. In this case, casting occurs without the need for the user to do it manually. The resulting value takes the type of the more encompassing data type of the involved values, as can be seen in the example below: "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 22,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "42.6"
      ]
     },
     "execution_count": 22,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Adding an integer to a float results in a value of type float.\n",
    "40 + 2.6"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 23,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "float"
      ]
     },
     "execution_count": 23,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "type(40 + 2.6)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "What happens when dividing two integer values? "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 24,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "0.275"
      ]
     },
     "execution_count": 24,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Divide two integers.\n",
    "11 / 40"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 25,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "float"
      ]
     },
     "execution_count": 25,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Type of resulting value from dividing two integers.\n",
    "type(11 / 40)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<div class=\"alert alert-warning\">\n",
    "<b>Note for Python 2.7 users</b>:<br>\n",
    "It turns out that, in Python 2.7 and earlier versions, operations involving two integers will result in an integer value, even if the correct result is a float. Thus, one needs to be very careful when dealing with integer operations. Ideally, you always want to ensure that you cast one of the values (it does not matter which one) to a float, so that the resulting value is correctly represented as a float. This is not required for Python 3 and later.\n",
    "</div>"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 26,
   "metadata": {},
   "outputs": [],
   "source": [
    "# Example of casting integer prior to performing math operations required for Python 2.7 and earlier.\n",
    "# 11/float(40)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 2.5 Complex numbers"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Complex numbers are important in many scientific and engineering disciplines. Python can also represent and perform calculations with  [complex numbers](https://docs.python.org/3/library/cmath.html)."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 27,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(1.5+2j)"
      ]
     },
     "execution_count": 27,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Complex numbers are represented by a real + imaginary part. The imaginary part is indicated by adding a suffix j.\n",
    "1.5 + 2j"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 28,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "complex"
      ]
     },
     "execution_count": 28,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "type((1.5 + 2j))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 2.6 The assignment operator and variables"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Our expressions, for example \"```type(40) == type('40')```\", can quickly become unwieldy and a source of errors that are difficult to debug. To help in manipulating values elegantly (and programmatically), it is common to use variables to store the value of interest. The variable is then used to reference the value of interest. To assign a value to a variable, we use the assignment operator \"```=```\" as in the following example:"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 29,
   "metadata": {},
   "outputs": [],
   "source": [
    "a_boolean_value = (type(40) == type('40'))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Here, the value on the right-hand side of the assignment operator â€œ```=```â€ has been assigned to the variable that has been cleverly named â€œ```a_boolean_value```â€. You can now use the variable in other parts of your code.\n",
    "\n",
    "Letâ€™s introduce another function, called â€œprintâ€ (another **keyword**), which prints the value associated with your variable."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 30,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "False\n"
     ]
    }
   ],
   "source": [
    "print(a_boolean_value)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "You can also use print for other expressions you have met before:"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 31,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "0.275\n"
     ]
    }
   ],
   "source": [
    "print(11/40)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "The print function allows you to perform other formatting and interesting value referencing."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 32,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Bob is 40 years old and spent 11 in school, that is 27.5% of his life.\n"
     ]
    }
   ],
   "source": [
    "print('{} is {} years old and spent {} in school, that is {}% of his life.'.format('Bob',40, 11,100*11/40))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "In this print statement, the ```str.format()``` form has been used as argument, where â€œplaceholdersâ€ or format fields indicated by ```{}```, are replaced by arguments specified in format argument. The arguments are used in the order used inside the parentheses, and must be equal to the number of the ```{}``` in the ```str``` part. You can also specify which positional argument should go where by including numbering in the format fields."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 33,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Bob is 40 years old and spent 11 in school, that is 27.5% of his life.\n"
     ]
    }
   ],
   "source": [
    "print('{0} is {1} years old and spent {2} in school, that is {3}% of his life.'.format('Bob',40, 11,100*11/40))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "By using numbered fields, the arguments are used depending on which number they are, with the first argument in format numbered as 0.\n",
    "Using print in this way is especially useful when you want to combine different data types in your print statement as illustrated above. You can also control how the formatting should be done instead of relying on Python's default behavior. For example, if you don't care about the decimal in the percentage, you can call print as follows:"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 34,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Bob is 40 years old and spent 11 in school, that is 28% of his life.\n"
     ]
    }
   ],
   "source": [
    "print('{0} is {1} years old and spent {2} in school, that is {3:.0f}% of his life.'.format('Bob',40,11,100*11/40))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Notice the value has only been rounded in the print output but not its representation in memory."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<br>\n",
    "<div class=\"alert alert-info\">\n",
    "<b>Exercise 1 Start: Printing strings.</b>\n",
    "</div>\n",
    "\n",
    "### Instructions\n",
    "1. Set your first and last names as separate variables (\"firstname\" and \"lastname\", respectively).\n",
    "2. Print your first name and last name using the \"``str.format()``\" form discussed above. Include a whitespace character between your first and last name in the print output."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 35,
   "metadata": {},
   "outputs": [],
   "source": [
    "# Your code here\n",
    "\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Edric Smith \n"
     ]
    }
   ],
   "source": [
    "firstname = 'Edric'\n",
    "lastname = 'Smith'\n",
    "print('{0} {1} '.format(firstname,lastname))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<br>\n",
    "<div class=\"alert alert-info\">\n",
    "<b>Exercise 1 End.</b>\n",
    "</div>\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "> **Exercise complete**:\n",
    "    \n",
    "> This is a good time to \"Save and Checkpoint\"."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 2.7 Aggregate data types: lists and tuples\n",
    "\n",
    "Variables store information that may change over time. When you need to store longer lists of information, there are additional options available. You will be introduced to lists and tuples as basic elements, and can read more about native Python data structures in the [Python documentation](https://docs.python.org/3/tutorial/datastructures.html). During this course, you will be exposed to examples using the [Pandas](http://pandas.pydata.org/) and [NumPy](http://www.numpy.org/) libraries, which offer additional options for data analysis and manipulation.\n",
    "\n",
    "### 2.7.1 Lists\n",
    "[Lists](https://docs.python.org/3/tutorial/introduction.html#lists) are changeable sequences of values. They are stored within square brackets, and items within a list are separated by commas. Lists can also be modified, appended, and sorted, among other [methods](https://docs.python.org/3/tutorial/datastructures.html#more-on-lists)."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "#### Create and print a list"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 36,
   "metadata": {
    "scrolled": true
   },
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "['this', 'is', 'a', 'list']\n",
      "The list contains 4 elements.\n"
     ]
    }
   ],
   "source": [
    "# Lists.\n",
    "lst = ['this', 'is', 'a', 'list']\n",
    "print(lst)\n",
    "\n",
    "# Print the number of elements in the list.\n",
    "print('The list contains {} elements.'.format(len(lst)))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "#### Selecting an element in a list\n",
    "Remember that Python uses zero indexing, that is, the index starts at zero. You can use a negative index to select the last element in the list."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 37,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "this\n",
      "a\n",
      "list\n"
     ]
    }
   ],
   "source": [
    "# Print the first element in the list.\n",
    "print(lst[0])\n",
    "\n",
    "# Print the third element in the list.\n",
    "print(lst[2])\n",
    "\n",
    "# Print the last element in the list.\n",
    "print(lst[-1])"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "#### Append to a list"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 38,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "['this', 'is', 'a', 'list']\n",
      "['this', 'is', 'a', 'list', 'with', 'appended', 'elements']\n",
      "The updated list contains 7 elements.\n"
     ]
    }
   ],
   "source": [
    "# Appending a list.\n",
    "print(lst)\n",
    "lst.append('with')\n",
    "lst.append('appended')\n",
    "lst.append('elements')\n",
    "print(lst)\n",
    "\n",
    "# Print the number of elements in the list.\n",
    "print('The updated list contains {} elements.'.format(len(lst)))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "> **Note**:\n",
    "\n",
    "> When selecting and executing the cell again, you will continue to add values to the list.\n",
    "\n",
    "> **Try this**: Select the cell above again and execute it to see how the input and output content changes.\n",
    "\n",
    "> This can come in handy when working with loops."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Changing a list**\n",
    "\n",
    "This course will not cover string methods in detail. You can read more about [string methods](https://docs.python.org/3/library/stdtypes.html?highlight=upper#sequence-types-list-tuple-range) in the Python documentation, if you are interested."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 39,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "['THIS', 'is', 'a', 'LIST', 'with', 'appended', 'elements']\n"
     ]
    }
   ],
   "source": [
    "# Changing a list.\n",
    "# Note: Remember that Python starts with index 0.\n",
    "lst[0] = 'THIS'\n",
    "lst[3] = lst[3].upper()\n",
    "print(lst)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "#### Define a list of numbers"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 40,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[0, 10, 2, 7, 8, 5, 6, 3, 4, 1, 9]\n"
     ]
    }
   ],
   "source": [
    "# Define a list of numbers.\n",
    "numlist = [0, 10, 2, 7, 8, 5, 6, 3, 4, 1, 9]\n",
    "print(numlist)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "#### Sort and filter a list"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 41,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[5, 6, 7, 8, 9, 10]\n"
     ]
    }
   ],
   "source": [
    "# Sort and filter list.\n",
    "sorted_and_filtered_numlist = sorted(i for i in numlist if i >= 5)\n",
    "print(sorted_and_filtered_numlist)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "#### Remove the last element from a list"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 42,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[5, 6, 7, 8, 9]\n"
     ]
    }
   ],
   "source": [
    "# Remove the last element from the list.\n",
    "list.pop(sorted_and_filtered_numlist)\n",
    "print(sorted_and_filtered_numlist)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### 2.7.2 Tuples\n",
    "[Tuples](https://docs.python.org/3/tutorial/datastructures.html?highlight=tuples#tuples-and-sequences) are similar to lists, except that they are defined in parentheses and are unchangeable, which means that their values cannot be modified."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 43,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "('this', 'is', 'a', 'bigger', 'tuple')\n"
     ]
    }
   ],
   "source": [
    "tup = ('this', 'is', 'a', 'bigger', 'tuple')\n",
    "print(tup)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 44,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "'bigger'"
      ]
     },
     "execution_count": 44,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "tup[3]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 45,
   "metadata": {},
   "outputs": [
    {
     "ename": "TypeError",
     "evalue": "'tuple' object does not support item assignment",
     "output_type": "error",
     "traceback": [
      "\u001b[0;31m---------------------------------------------------------------------------\u001b[0m",
      "\u001b[0;31mTypeError\u001b[0m                                 Traceback (most recent call last)",
      "\u001b[0;32m<ipython-input-45-5b7c30070c94>\u001b[0m in \u001b[0;36m<module>\u001b[0;34m()\u001b[0m\n\u001b[1;32m      1\u001b[0m \u001b[0;31m# Tuples cannot be changed and will fail with an error if you try to change an element.\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0;32m----> 2\u001b[0;31m \u001b[0mtup\u001b[0m\u001b[0;34m[\u001b[0m\u001b[0;36m3\u001b[0m\u001b[0;34m]\u001b[0m \u001b[0;34m=\u001b[0m \u001b[0;34m'new'\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0m",
      "\u001b[0;31mTypeError\u001b[0m: 'tuple' object does not support item assignment"
     ]
    }
   ],
   "source": [
    "# Tuples cannot be changed and will fail with an error if you try to change an element.\n",
    "tup[3] = 'new'"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 2.8 Loops, sequences, and conditionals\n",
    "Conditions and loops are control structures that can be used to repeat statements based on the conditions or loops specified. This can be employed to cycle through data sets or perform a sequence of steps on (or based on) input variables."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 2.9 Range\n",
    "[Range](https://docs.python.org/3/library/stdtypes.html#range) (start, stop, step) is used to create lists containing arithmetic progressions. If you call a range with only one argument specified, it will use the value as the stop value and default to zero as the start value. The step argument is optional and can be a positive or negative integer."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 46,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]"
      ]
     },
     "execution_count": 46,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Generate a list of 10 values.\n",
    "myrange = list(range(10))\n",
    "myrange"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 47,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "[1, 4, 7]"
      ]
     },
     "execution_count": 47,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Generate a list with start value equal to one, stop value equal to ten that increments by three.\n",
    "myrange2 = list(range(1, 10, 3))\n",
    "myrange2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 48,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "[0, -1, -2, -3, -4, -5, -6, -7, -8, -9]"
      ]
     },
     "execution_count": 48,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Generate a negative list.\n",
    "myrange3 = list(range(0, -10, -1))\n",
    "myrange3"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 2.10 Basic loops\n",
    "Python uses ``for`` and ``while``  loops to repeat sections of statements. A ``for`` loop runs for a set number of times, whereas a ``while`` loop repeats a statement until a certain condition is met. The statements to be repeated must be indented for the interpreter to recognise them as such.\n",
    "\n",
    "The example below demonstrates how to do the following:\n",
    "- Cycle through the generated list and:\n",
    "  - Print the current element in the list; and\n",
    "  - Print Xs, which are repeated per element.\n",
    "- Exit the loop and print a line that is not repeated."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 49,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "0\n",
      "\n",
      "1\n",
      "X\n",
      "2\n",
      "XX\n",
      "3\n",
      "XXX\n",
      "4\n",
      "XXXX\n",
      "5\n",
      "XXXXX\n",
      "6\n",
      "XXXXXX\n",
      "7\n",
      "XXXXXXX\n",
      "8\n",
      "XXXXXXXX\n",
      "9\n",
      "XXXXXXXXX\n",
      "End of loop (not included in the loop)\n"
     ]
    }
   ],
   "source": [
    "# An example of a loop that uses the \"for\" construct.\n",
    "\n",
    "# You can specify the list manually or use a variable containing the list as input.\n",
    "# The syntax for manual input is: `for item in [1, 2, 3]:`\n",
    "\n",
    "for item in myrange:\n",
    "    print(item)\n",
    "    print(item * 'X')\n",
    "print('End of loop (not included in the loop)')"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 50,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "0\n",
      "\n",
      "1\n",
      "X\n",
      "2\n",
      "XX\n",
      "3\n",
      "XXX\n",
      "4\n",
      "XXXX\n",
      "5\n",
      "XXXXX\n",
      "6\n",
      "XXXXXX\n",
      "7\n",
      "XXXXXXX\n",
      "8\n",
      "XXXXXXXX\n",
      "9\n",
      "XXXXXXXXX\n",
      "End of loop (not included in the loop)\n"
     ]
    }
   ],
   "source": [
    "# An example of a loop that uses the \"while\" construct.\n",
    "\n",
    "# Firstly, set a counter variable to check whether the end of the list has been reached.\n",
    "\n",
    "i = 0\n",
    "while i < len(myrange):\n",
    "    print(myrange[i])\n",
    "    print(myrange[i] * 'X')\n",
    "    i = i + 1\n",
    "print('End of loop (not included in the loop)')"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 2.11 Conditionals\n",
    "Conditionals are used to determine which statements are executed. In the example below, we import the \"random\" library and generate a random number smaller than 2. Assume 0 means heads and 1 means tails. The conditional statement is then used to print the result of the coin flip, as well as \"Heads\" or \"Tails\"."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 51,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "1\n",
      "Tails\n"
     ]
    }
   ],
   "source": [
    "# Flip a coin.\n",
    "\n",
    "import random\n",
    "coin_result = random.randrange(0,2)\n",
    "\n",
    "print(coin_result)\n",
    "\n",
    "if coin_result == 0:\n",
    "    print('Heads')\n",
    "else:\n",
    "    print('Tails')"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### 2.11.1 Importing modules:\n",
    "Code reuse is an integral component in programming, and is critical for extending basic functionality of an underlying programmming environment. In Python, modules exists that contain functions, classes, variables and other code that we can reuse in our own code. In most cases, these modules are provided under permissive free software license such as the MIT license. Assuming you know the name of the module you want to use, there are a number of ways you can tell Python that you want to access that module.\n",
    "- ```import X ```\n",
    "> This imports the module X, and creates a reference to that module in the current namespace. After running this statement, you can use X.name to refer to things defined in module X. In the above example, we import the **random** module, and used the ```random.randrange(0,2)``` to call a function called ```randrange``` in that module. It is also common to use an alias for ``X`` by importing the module as ```import X as alias```. Now we use ```alias.name``` to refer things defined in module X. \n",
    "\n",
    "- ```from X import * ```\n",
    "> This statement imports the module X, and creates references in the current namespace to all public objects defined by that module (that is, everything that doesnâ€™t have a name starting with \"``_``\"). After youâ€™ve run this statement, you can simply use a name to refer to things defined in module X without prepending ``X.`` to it. Although there are cases where this is necessary, it is best to avoid this in the majority of cases as it can lead to unexpected behaviour.\n",
    "\n",
    "- ``from X import a, b, c`` \n",
    "> This works like the previous statement by importing the module X, but creates references in the current namespace only to the objects provided (implying you should know that these are defined in the module). Thus, you can now use ``a`` and ``b`` and ``c`` in your program."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 2.12 Functions\n",
    "Functions allow for code reuse within and across applications. When defining a function, you would use the â€œ```def```â€ statement. The desired function code is then placed into the body of the statement. A function usually takes in an argument and returns a value as determined by the code in the body of the function. Whenever referring to the function, outside of the function body itself, this action is known as a function call."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 52,
   "metadata": {},
   "outputs": [],
   "source": [
    "# Function 'myfirstfunction' with argument 'x'.\n",
    "def myfirstfunction(x):\n",
    "    y = x * 6\n",
    "    return y"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "You can now call the function as in the next example."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 53,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "36\n"
     ]
    }
   ],
   "source": [
    "# Call your function.   \n",
    "z = myfirstfunction(6)\n",
    "print(z)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Function definitions, loops, and conditionals can be combined to produce something useful. The example below will simulate a variable number of coin flips and then produce the summary of results as output."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 54,
   "metadata": {},
   "outputs": [],
   "source": [
    "import random"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 55,
   "metadata": {},
   "outputs": [],
   "source": [
    "def coinflip(total_number_of_flips):\n",
    "    '''\n",
    "    function 'coinflip' with argument 'total_number_of_flips' for the number of repetitions \n",
    "    that returns the number of 'tail' occurrences\n",
    "    '''\n",
    "    # Set all starting variables to 0.\n",
    "    heads = 0\n",
    "    tails = 0\n",
    "    current_number_of_flips = 0\n",
    "    # Start a loop that executes statements while the conditional specified results in 'True'.\n",
    "    while current_number_of_flips < total_number_of_flips:\n",
    "        # Generate a random number smaller than 2.\n",
    "        current_flip = random.randrange(0,2)\n",
    "        # Increment heads by 1 if the generated number is 0.\n",
    "        if current_flip == 0:\n",
    "            heads = heads + 1\n",
    "        # Increment tails by 1 if the generated number is larger than 0.\n",
    "        if current_flip == 1:\n",
    "            tails = tails + 1\n",
    "        # Increment the flip variable by 1.\n",
    "        current_number_of_flips += 1\n",
    "    return [heads, tails]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "In the above function definition, there is a â€œdocstringâ€ to describe what the function does in lieu of the comment that has been used. This is considered best practice when defining functions in Python. The docstring is included just after the ```def``` statement, and is included between a pair of three single or double quotation marks.\n",
    "\n",
    "In the \"```coinflip```\" function, you are simulating the number of times an unbiased coin returns heads or tails on being flipped. To track these values, initialize the counts to zero for both the heads and tails variables. Moreover, it is also important to include a variable flip that tracks the number of flips in the simulation. The simulation ends when the number of flips required, as specified in the function argument, is reached. To simulate the actual coin flip or flip event, call the function â€œ```randrange```â€ from the Python \"```random```\" module, which accepts a minimum of two parameters: the start of the range from which you want to simulate, and the end of the range (stop) from which point and above you do not care about. You can see what this \"``randrange``\" function does by calling it for the given parameters."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 56,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "1\n",
      "0\n",
      "0\n",
      "0\n",
      "1\n",
      "1\n",
      "0\n",
      "1\n",
      "0\n",
      "1\n"
     ]
    }
   ],
   "source": [
    "import datetime \n",
    "now = datetime.datetime.now() \n",
    "random.seed(now)\n",
    "for k in range(0,10):\n",
    "    print(random.randrange(0,2))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Every time you call \"```randrange```\", either a 0 or 1 is returned with equal probability. Hence, it is a good approximation to flipping an unbiased coin in our example. This example also does something that is slightly complex to describe. Before entering the loop, set your random seed generator to the current time. This ensures you do not always get the same sequence, as random number generation inside the program is not truly random, but follows a deterministic algorithm. \n",
    "> **Note:**\n",
    ">\n",
    "> Later modules will exploit this determinism by setting the random seed for reproducibility of expected outcomes.\n",
    "\n",
    "Going back to the coin flip function, when you flip the coin, a 0 or 1 is obtained as a value. You check whether this is 0, and if so, you increment your count of heads by 1. If it is a 1, you increment the count of tails by 1. Recall that these two states are mutually exclusive, and only one can occur on each flip. After these checks, you also increase your count of flips tracked in â€œ```current_number_of_flips```â€. You repeat this until you have reached the â€œ```total_number_of_flips```â€.\n",
    "\n",
    "Finally, the function returns the counts of both heads and tails obtained from your simulation as an array, where the first entry is number of heads. Letâ€™s invoke the function for 100 flips."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 57,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[47, 53]\n"
     ]
    }
   ],
   "source": [
    "# Set the number of repetitions.\n",
    "num_flips = 100\n",
    "\n",
    "# Call the function and set the output to the variable 'tails'.\n",
    "coinflip_results = coinflip(num_flips)\n",
    "\n",
    "# Output the values returned.\n",
    "print(coinflip_results)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Is this coin balanced? You would need to run more simulations for a more definitive answer. Try 10000 simulations. Since you have a function already written, you can simply reuse it, as long as you specify a different value for the argument. This is the power of writing functions for tasks that follow the same design pattern."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 58,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Heads returned: 51%\n"
     ]
    }
   ],
   "source": [
    "num_flips = 10000\n",
    "coinflip_results = coinflip(num_flips)\n",
    "print('Heads returned: {:.0f}%'.format(100*float(coinflip_results[0])/sum(coinflip_results)))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Notice how this example has used a number of the ideas introduced in this notebook in computing the proportion of heads."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<br>\n",
    "<div class=\"alert alert-info\">\n",
    "<b>Exercise 2 Start: Rolling Dice.</b>\n",
    "</div>\n",
    "\n",
    "### Instructions\n",
    "\n",
    "> Use the \"coinflip\" example above and change it to simulate rolling dice. Your output should contain summary statistics for the number of times you rolled the dice, and occurrences of each of the 6 sides.\n",
    "\n",
    "> **Hints**:\n",
    "\n",
    "> - Replace \"Heads\" and \"Tails\" with six new variables: \"Side_1\", \"Side_2\", â€œSide_3â€, etc.\n",
    "> - Replace ```random.randrange(0,2)``` with ```random.randrange(1,7)```\n",
    "> - Test for whether each state of the random variable (which side comes up after a die throw), and increase the counter for the relevant variable.\n",
    "> - Return final states of each variable as a vector (i.e., [Side_1, Side_2, Side_3, etc.])."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 28,
   "metadata": {},
   "outputs": [],
   "source": [
    "# Your code here.\n",
    "import random\n",
    "def dice_roll(total_number_of_rolls):\n",
    "    '''\n",
    "    function 'dice_roll' with argument 'total_number_of_rolls' for the number of repetitions \n",
    "    that returns the number of observations\n",
    "    '''\n",
    "    # Set all starting variables to 0.\n",
    "    side_1 = 0\n",
    "    side_2 = 0\n",
    "    side_3 = 0\n",
    "    side_4 = 0\n",
    "    side_5 = 0\n",
    "    side_6 = 0\n",
    "    current_number_of_rolls = 0\n",
    "    # Start a loop that executes statements while the conditional specified results in 'True'.\n",
    "    while current_number_of_rolls < total_number_of_rolls:\n",
    "        # Generate a random number between 1 and 3 (included)\n",
    "        current_roll = random.randrange(1,7)\n",
    "        # Increment heads by 1 if the generated number is 1.\n",
    "        if current_roll == 1:\n",
    "            side_1 = side_1 + 1\n",
    "        # Increment heads by 1 if the generated number is 2.\n",
    "        if current_roll == 2:\n",
    "            side_2 = side_2 + 1\n",
    "        # Increment heads by 1 if the generated number is 3.\n",
    "        if current_roll == 3:\n",
    "            side_3 = side_3 + 1\n",
    "        # Increment heads by 1 if the generated number is 4.\n",
    "        if current_roll == 4:\n",
    "            side_4 = side_4 + 1\n",
    "        # Increment heads by 1 if the generated number is 5.\n",
    "        if current_roll == 5:\n",
    "            side_5 = side_5 + 1\n",
    "        # Increment heads by 1 if the generated number is 6.\n",
    "        if current_roll == 6:\n",
    "            side_6 = side_6 + 1\n",
    "        # Increment the flip variable by 1.\n",
    "        current_number_of_rolls += 1\n",
    "    return [side_1,side_2,side_3,side_4,side_5,side_6]\n",
    "\n",
    "\n",
    "\n",
    "\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 29,
   "metadata": {},
   "outputs": [],
   "source": [
    "numrolls=50"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 30,
   "metadata": {},
   "outputs": [],
   "source": [
    "diceroll_results =  dice_roll(numrolls)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 31,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "[7, 9, 8, 12, 7, 7]"
      ]
     },
     "execution_count": 31,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "diceroll_results"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<br>\n",
    "<div class=\"alert alert-info\">\n",
    "<b>Exercise 2 End.</b>\n",
    "</div>\n",
    "\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "> **Exercise complete**:\n",
    "    \n",
    "> This is a good time to \"Save and Checkpoint\"."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "The basic random function was used in the example above, but you can visit Big Data Examiner to see an example of [implementing other probability distributions](http://bigdata-madesimple.com/how-to-implement-these-5-powerful-probability-distributions-in-python/)."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# 3. Graphics and visualization\n",
    "\n",
    "Matplotlib is the standard library commonly used to display graphics and plots in Python. "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 3.1 Matplotlib\n",
    "\n",
    "The examples below come from the [Matplotlib Screenshots](http://matplotlib.org/users/screenshots.html) page.\n",
    "\n",
    "> **Note**: \n",
    "\n",
    "> One of the options that you will need to remember to set when you use Matplotlib is \"%matplotlib inline\", which instructs the notebook to plot inline instead of opening a separate window for your graph.\n",
    "\n",
    "You can find additional information on Matplotlib through the following resources:\n",
    "- [Matplotlib Documentation](http://matplotlib.org/)\n",
    "\n",
    "- [Matplotlib Beginners](http://matplotlib.org/users/beginner.html)\n",
    "\n",
    "- [Matplotlib Gallery](http://matplotlib.org/gallery.html)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {
    "collapsed": true
   },
   "source": [
    "### 3.1.1 Simple plot\n",
    "The graph below does not contain any real significance other than demonstrating how easy it is to plot graphs. "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 23,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 1080x648 with 1 Axes>"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "# Import matplotlib library and set notebook plotting options.\n",
    "import matplotlib.pyplot as plt\n",
    "import numpy as np\n",
    "# Instruct the notebook to plot inline. \n",
    "%matplotlib inline     \n",
    "plt.rcParams['figure.figsize'] = (15, 9) \n",
    "plt.rcParams['axes.titlesize'] = 'large'\n",
    "\n",
    "# Generate data.\n",
    "t = np.arange(0.0, 2.0, 0.01)\n",
    "s = np.sin(2*np.pi*t)\n",
    "\n",
    "# Create plot.\n",
    "plt.plot(t, s)\n",
    "\n",
    "# Set plot options.\n",
    "plt.xlabel('time (s)')\n",
    "plt.ylabel('voltage (mV)')\n",
    "plt.title('About as simple as it gets, folks')\n",
    "plt.grid(True)\n",
    "\n",
    "# Saving as file can be achieved by uncommenting the line below.\n",
    "# plt.savefig(\"test.png\")\n",
    "\n",
    "# Display the plot in the notebook.\n",
    "# The '%matplotlib inline' option set earlier ensure that the plot is displayed inline.\n",
    "plt.show()"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### 3.1.2 Subplots\n",
    "\"Subplots\" is another useful feature where you can display multiple plots. This is typically used to visually compare data sets."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 61,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 432x288 with 2 Axes>"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "\"\"\"\n",
    "Simple demo with multiple subplots.\n",
    "\"\"\"\n",
    "import numpy as np\n",
    "import matplotlib.pyplot as plt\n",
    "\n",
    "\n",
    "x1 = np.linspace(0.0, 5.0)\n",
    "x2 = np.linspace(0.0, 2.0)\n",
    "\n",
    "y1 = np.cos(2 * np.pi * x1) * np.exp(-x1)\n",
    "y2 = np.cos(2 * np.pi * x2)\n",
    "\n",
    "plt.subplot(2, 1, 1)\n",
    "plt.plot(x1, y1, 'yo-')\n",
    "plt.title('A tale of 2 subplots')\n",
    "plt.ylabel('Damped oscillation')\n",
    "\n",
    "plt.subplot(2, 1, 2)\n",
    "plt.plot(x2, y2, 'r.-')\n",
    "plt.xlabel('time (s)')\n",
    "plt.ylabel('Undamped')\n",
    "\n",
    "plt.show()"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### 3.1.3 Histogram \n",
    "Here is another example of a plot that will be utilized in future modules. The example demonstrates syntax, and provides ideas of what is possible."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 62,
   "metadata": {},
   "outputs": [
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "/opt/conda/lib/python3.6/site-packages/matplotlib/axes/_axes.py:6462: UserWarning: The 'normed' kwarg is deprecated, and has been replaced by the 'density' kwarg.\n",
      "  warnings.warn(\"The 'normed' kwarg is deprecated, and has been \"\n",
      "/opt/conda/lib/python3.6/site-packages/ipykernel_launcher.py:27: MatplotlibDeprecationWarning: scipy.stats.norm.pdf\n"
     ]
    },
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "\"\"\"\n",
    "Demo of the histogram (hist) function with a few features.\n",
    "\n",
    "In addition to the basic histogram, this demo shows a few optional features:\n",
    "\n",
    "    * Setting the number of data bins\n",
    "    * The ``normed`` flag, which normalizes bin heights so that the integral of\n",
    "      the histogram is 1. The resulting histogram is a probability density.\n",
    "    * Setting the face color of the bars\n",
    "    * Setting the opacity (alpha value).\n",
    "\n",
    "\"\"\"\n",
    "import numpy as np\n",
    "import matplotlib.mlab as mlab\n",
    "import matplotlib.pyplot as plt\n",
    "\n",
    "\n",
    "# Example data.\n",
    "mu = 100  # Mean of distribution.\n",
    "sigma = 15  # Standard deviation of distribution.\n",
    "x = mu + sigma * np.random.randn(10000)\n",
    "\n",
    "num_bins = 50\n",
    "# The histogram of the data.\n",
    "n, bins, patches = plt.hist(x, num_bins, normed=1, facecolor='green', alpha=0.5)\n",
    "# Add a 'best fit' line.\n",
    "y = mlab.normpdf(bins, mu, sigma)\n",
    "plt.plot(bins, y, 'r--')\n",
    "plt.xlabel('Smarts')\n",
    "plt.ylabel('Probability')\n",
    "plt.title(r'Histogram of IQ: $\\mu=100$, $\\sigma=15$')\n",
    "\n",
    "# Tweak spacing to prevent clipping of ylabel.\n",
    "plt.subplots_adjust(left=0.15)\n",
    "plt.show()"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### 3.1.4 Visualizing coin flip distribution\n",
    "\n",
    "This is a continuation of your coin flip simulation from the previous section. Although you already have a fairly accurate idea of whether or not the coin is biased, in statistics, the typical approach requires sampling from the underlying distribution multiple times, and then plotting the sampling distribution. To this end, a handle is required on the actual value for the probability of landing heads between 0 and 1 (probability of landing tails will then be 1 minus that value), which can be generated using the \"```random()```\" method from the **random** module, that is the call \"```random.random()```\". In the case of a fair coin, designate as heads anytime the value generated is below 0.5, otherwise it is assigned as tails. An unfair coin can be simulated by adjusting this threshold; the closer the value is to 0 (and below 0.5) the less likely the chance of getting heads in multiple trials. This is an involved complex statistical procedure, and is captured here for illustrative purposes. \n",
    "\n",
    "In the next code cell, we simulate flipping a fair coin by specifying the threshold as 0.5. You will flip the coin 10 times and note the number of times it falls heads in those trials. This is repeated 1000 times, from which a plot of the sampling distribution of the underlying distribution (known as the binomial distribution) is generated."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 63,
   "metadata": {},
   "outputs": [],
   "source": [
    "threshold = 0.5\n",
    "ntrials = 10 # Flips per trial.\n",
    "size = 1000 # Repetitions.\n",
    "M = [0 for x in range(0,size)] \n",
    "for i in range(0,size):\n",
    "    M[i] = sum([random.random()< threshold for x in range(0,ntrials)])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 64,
   "metadata": {},
   "outputs": [],
   "source": [
    "# Cross tabulation for frequency of occurence of values.\n",
    "M_xtab = [0 for i in range(0, ntrials)]\n",
    "for i in range(0,ntrials):\n",
    "    M_xtab[i] = sum([x == i for x in M])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 65,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[2, 8, 38, 108, 206, 237, 227, 117, 40, 16]\n"
     ]
    }
   ],
   "source": [
    "print(M_xtab)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 66,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Text(0.5,1,'Coin flip distribution')"
      ]
     },
     "execution_count": 66,
     "metadata": {},
     "output_type": "execute_result"
    },
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "# The histogram of the data.\n",
    "plt.hist(M, range=(0,ntrials),bins=ntrials)\n",
    "plt.xlabel('Number  of heads')\n",
    "plt.ylabel('Frequency')\n",
    "plt.title('Coin flip distribution')"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "As before, the chance of our coin landing heads is as one would expect from an unbiased coin."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<br>\n",
    "<div class=\"alert alert-info\">\n",
    "<b>Exercise 3 Start: Coin flip distribution.</b>\n",
    "</div>\n",
    "\n",
    "### Instructions\n",
    "\n",
    "> Using the \"coinflip\" example above, simulate the distribution one would get for a biased coin that has an *80%* probability of landing tails for *1000* simulations, where the coin is flipped *20* times at each simulation. Plot the histogram using the Matplotlib.\n",
    "\n",
    "> **Hints**:\n",
    "\n",
    "> - Change \"ntrials\", \"size\", and \"threshold\" in the coin simulation code from above.\n",
    "> - The probability of getting tails is given. You need to compute the probability of getting heads from this value, which you will then use as the threshold value."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 67,
   "metadata": {},
   "outputs": [],
   "source": [
    "# Your code here."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 24,
   "metadata": {},
   "outputs": [],
   "source": [
    "threshold = 1-0.8\n",
    "ntrials = 20 # Flips per trial.\n",
    "size = 1000 # Repetitions.\n",
    "M = [0 for x in range(0,size)] \n",
    "for i in range(0,size):\n",
    "    M[i] = sum([random.random()< threshold for x in range(0,ntrials)])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 25,
   "metadata": {},
   "outputs": [],
   "source": [
    "# Cross tabulation for frequency of occurence of values.\n",
    "M_xtab = [0 for i in range(0, ntrials)]\n",
    "for i in range(0,ntrials):\n",
    "    M_xtab[i] = sum([x == i for x in M])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 27,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Text(0.5,1,'Coin flip distribution')"
      ]
     },
     "execution_count": 27,
     "metadata": {},
     "output_type": "execute_result"
    },
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "# The histogram of the data.\n",
    "plt.hist(M, range=(-0.5,ntrials),bins=ntrials)\n",
    "plt.xlabel('Number  of heads')\n",
    "plt.ylabel('Frequency')\n",
    "plt.title('Coin flip distribution')"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<br>\n",
    "<div class=\"alert alert-info\">\n",
    "<b>Exercise 3 End.</b>\n",
    "</div>\n",
    "\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {
    "collapsed": true
   },
   "source": [
    "# 4. Submit your notebook\n",
    "\n",
    "Please make sure that you:\n",
    "- Perform a final \"Save and Checkpoint\";\n",
    "- Download a copy of the notebook in \".ipynb\" format to your local machine using \"File\", \"Download as\", and \"IPython Notebook (.ipynb)\"; and\n",
    "- Submit a copy of this file to the Online Campus."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {
    "collapsed": true
   },
   "source": [
    "# 5. Additional resources\n",
    "\n",
    "> **Note**:\n",
    "\n",
    "> This resource is optional and is only included for students who wish to complete additional exercises in Python.\n",
    "\n",
    "- Additional [Python course](http://www.python-course.eu/course.php).\n",
    "- [Python tips for beginners](http://www.techbeamers.com/top-10-python-coding-tips-for-beginners/)\n",
    "- [30 essential Python tips and tricks](http://www.techbeamers.com/essential-python-tips-tricks-programmers/)\n",
    "\n",
    "    "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {
    "collapsed": true
   },
   "source": [
    "# 6. References\n",
    "Python Software Foundation. 2016. â€œGeneral Python FAQ - Python 3.6.2 documentation.â€Last accessed August 20, 2017. https://docs.python.org/3/faq/general.html#what-is-python. \n",
    "\n",
    "MIT OpenCourseWare. 2011. â€œ6.096 Introduction to C++.â€ Accessed September 20. https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-096-introduction-to-c-january-iap-2011/lecture-notes/MIT6_096IAP11_lec02.pdf. "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "anaconda-cloud": {},
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.6.5"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 1
}
