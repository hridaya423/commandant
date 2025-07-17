# Commandant

A war-themed esoteric programming language that brings military terminology to code. Write programs using battlefield commands and tactical operations.

## Features

### Core Language Features

**Variables & Assignment**

- `enlist variable_name = value` - Declare and initialize variables
- `variable_name = new_value` - Reassign variables

**Output & Input**

- `shout "message"` - Print output to console
- `interrogate "prompt"` - Get user input with a prompt

**Arithmetic Operations**

- `reinforce` - Addition (+)
- `expend` - Subtraction (-)
- `amplify` - Multiplication (\*)
- `decimate` - Division (/)

**Comparison Operations**

- `outranks` - Greater than (>)
- `outranks or holds` - Greater than or equal (>=)
- `is outranked by` - Less than (<)
- `is outranked or held by` - Less than or equal (<=)
- `is equal to` - Equality (==)
- `is not equal to` - Not equal (!=)

**Logical Operations**

- `and also` - Logical AND
- `or else` - Logical OR

**Control Flow**

- `recon condition:` ... `secure.` - If statements
- `else recon condition:` - Else if
- `fallback position:` - Else clause
- `while under siege condition:` ... `break siege.` - While loops
- `patrol through variable in array:` ... `end patrol.` - For-each loops

**Functions**

- `mission function_name with param1, param2:` ... `retreat.` - Function definition
- `execute function_name with arg1, arg2` - Function calls
- `report value` - Return statement

**Arrays/Lists**

- `[element1, element2, element3]` - Array literals
- `array[index]` - Array element access
- `array[index] = value` - Array element assignment
- `execute deploy with array, element` - Add element to end (push)
- `execute extract with array` - Remove and return last element (pop)
- `execute headcount with array` - Get array length
- `execute reinforce_at with array, index, element` - Insert element at position
- `execute evacuate_at with array, index` - Remove element at position

**Comments**

- `// comment` - Single-line comments

## Installation

```bash
npm install
```

## Usage

### Run a Commandant file

```bash
node index.js <file_path>
```

### Interactive REPL

```bash
node index.js
```

### Example

```bash
node index.js examples/example.war
```

## Language Examples

### Hello World

```bash
shout "Hello, Commander!"
```

### Variables and Arithmetic

```bash
enlist soldiers = 100
enlist reinforcements = 50
enlist total_force = soldiers reinforce reinforcements
shout "Total forces: " reinforce total_force
```

### Conditional Logic

```bash
enlist threat_level = 3

recon threat_level outranks 5:
    shout "High threat detected!"
else recon threat_level outranks 2:
    shout "Medium threat level"
fallback position:
    shout "All clear"
secure.
```

### Functions

```bash
mission calculate_casualties with initial, losses:
    enlist survivors = initial expend losses
    report survivors
retreat.

enlist result = execute calculate_casualties with 100, 25
shout "Survivors: " reinforce result
```

### Loops

```bash
enlist countdown = 5
while under siege countdown outranks 0:
    shout "T-minus " reinforce countdown
    countdown = countdown expend 1
break siege.
```

### User Input

```bash
enlist commander = interrogate "Enter your name, Commander: "
shout "Welcome to the battlefield, " reinforce commander
```

### Arrays

```bash
// Create and manipulate arrays
enlist squad = [10, 20, 30, 40, 50]
enlist roster = ["Alpha", "Bravo", "Charlie"]

shout "Squad strength: " reinforce squad[0]
squad[1] = 25

// Array operations
execute deploy with squad, 60
enlist total = execute headcount with squad
shout "Total soldiers: " reinforce total

enlist extracted = execute extract with squad
shout "Extracted: " reinforce extracted
```

### For-Each Loops

```bash
enlist units = ["Alpha", "Bravo", "Charlie"]
patrol through unit in units:
    shout "Unit " reinforce unit reinforce " reporting"
end patrol.
```
## Future Features

### Planned Enhancements

- **Objects/Structures**: `base headquarters = { troops: 500, supplies: 1000 }` - Command structures
- **File I/O**: `intel_report = reconnaissance "data.txt"` - File reading operations
- **Error Handling**: `ambush ... rescue ...` - Try-catch equivalent
- **String Operations**: `decode message`, `encrypt intel` - String manipulation
- **Math Functions**: `artillery_range`, `trajectory_calc` - Built-in math operations
- **Modules/Imports**: `get backup from "support.war"` - Code organization

