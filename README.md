# SQL Query Compiler

This is a SQL query compiler implemented using Flex and Bison.

## Overview

The SQL Query Compiler is designed to analyze and compile SQL queries written in a specific grammar. It utilizes the Flex lexical analyzer and the Bison parser generator to perform lexical and syntax analysis of the input queries.

## Features

- Lexical analysis: The Flex analyzer tokenizes the input SQL queries, identifying individual tokens such as types, identifiers, conditions, and symbols.
- Syntax analysis: The Bison parser generates a parse tree based on the grammar rules defined for the SQL language. It checks the validity of the queries and detects any syntax errors.
- Query compilation: The compiler processes the valid SQL queries and generates appropriate output, such as an optimized query plan or intermediate code representation.

## Getting Started

### Prerequisites

Make sure you have the following tools installed:

- Flex 
- Bison
- C compiler (MinGW)

### Building the Compiler

1. Clone this repository to your local machine.
2. Navigate to the project directory.
3. Run the following commands to build the compiler:

   ```bash
   flex mini.l
   bison -d mini.y
   gcc mini.yy.c mini.tab.c -o sql_compiler

### Running the Compiler

    ```bash
      ./sql_compiler < input.txt

with input.txt being a file that contains a SQL Query
