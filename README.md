# Static Analyzer for Python Code

This Python application implements a static analyzer designed to perform quality checks and ensure coding standards. The analyzer covers several key areas to identify potential issues and improve code quality.

## Features

- Attribute Check: Validates function attributes for correctness.  
- Unreachable Code Detection: Identifies code that appears after a return statement.  
- Parameter Count Check: Ensures functions do not have more than three parameters.  
- Division by Zero: Detects potential division by zero errors.  
- Magic Number Detection: Identifies "magic numbers" in the code.

## Usage

### 1. Attribute Check
The analyzer performs two main tasks:

- **Function Signature Validation**: Checks if the function's signature contains specific attributes. Attributes are verified based on their position and type.
- **Value Check**: Ensures that attribute values meet specified criteria.

**Implementation:**

- Reads the code file line by line.
- Identifies function definitions and extracts function arguments.
- Checks the type and format of attributes.
- Validates attribute values based on specified rules.

**Example:**

```python
def example_function(int_param: int, str_param1: str, str_param2: str):
    pass
```
### 2. Unreachable Code Detection
This feature identifies lines of code that appear after a return statement.

**Implementation:**

- Reads the code file to find return statements.
- Checks if subsequent lines contain code that should not be executed.

### 3. Parameter Count Check
Ensures that functions do not exceed three parameters.

**Implementation:**

- Counts the number of commas in function definitions.
- Generates an error if a function exceeds the parameter limit.
  
**Example:**

```python
def many_params(a, b, c, d):
    pass
```
### 4. Division by Zero Detection
Detects potential division by zero errors.

**Implementation:**

- Reads each line to find division operations.
- Checks if the divisor is zero and generates an error message if so.

### 5. Magic Number Detection
Identifies magic numbers in the code.

**Implementation:**
- Checks for direct comparisons with numbers, comparisons without meaningful context, or use of numbers in specific contexts.

**Example:**

```python
if value == 42:
    pass
```


