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
