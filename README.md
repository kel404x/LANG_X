
# LANG X 

Welcome to **LANG X**, a pseudocode-based programming tool designed to turn your high-level logic into working JavaScript code. This guide will walk you through creating `.xl` files and using our CLI to translate them into runnable JavaScript.

---

## **Getting Started**

### Prerequisites
Ensure you have the following installed:
- **Node.js** (v16+ recommended)

### Installation
1. Clone the LANG X repository:
   ```bash
   git clone https://github.com/kel404x/LANG_X.git
   cd LANG_X
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

---

## **Using LANG X (JavaScript)**

### Writing a `.xl` File
1. Create a new `.xl` file:
   ```bash
   touch factorial.xl
   ```

2. Add your LANG X pseudocode:
   ```plaintext
   TARGET_LANGUAGE: JavaScript

   DEFINE FUNCTION main
   PROMPT: Calculate the factorial of a given number recursively.
   Input: n (integer)
   Output: factorial of n
   ```

---

### Running LANG X

1. Translate your `.xl` file into JavaScript:
   ```bash
   node src/cli.js factorial.xl output.js
   ```

2. Open the `output.js` file to review the generated code:
   ```javascript
   // Function to calculate factorial recursively
   function factorial(n) {
       if (n === 0 || n === 1) {
           return 1;
       }
       return n * factorial(n - 1);
   }

   // Main function
   function main() {
       let number = 5; // Example input
       let result = factorial(number);
       console.log("Factorial of " + number + " is: " + result);
   }

   main();
   ```

3. Run the JavaScript file:
   ```bash
   node output.js
   ```

   Output:
   ```
   Factorial of 5 is: 120
   ```

---

### Troubleshooting
- **Missing Input File**:  
  Ensure your `.xl` file exists and the path is correct. Example:  
  ```
  Error: Source file not found at "path/to/factorial.xl"
  ```

- **Invalid File Extension**:  
  Only `.xl` files are allowed. Example:  
  ```
  Error: Source file must have a .xl extension
  ```

- **Output Issues**:  
  Ensure your pseudocode follows LANG X conventions for syntax and inputs.

---

## **Contributing**
This is a JavaScript-first implementation of LANG X. Contributions are welcome! Feel free to submit pull requests or suggestions for improvements.

---

## **License**
This project is licensed under the MIT License. See the `LICENSE` file for details.

---
