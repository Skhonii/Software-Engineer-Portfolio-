
# Software Engineer Portfolio 

Helping machines learn to think critically, explain clearly, and debug with precision.  

This portfolio simulates real-world onboarding tasks for Outlier AI — designed to test annotation fluency, code reasoning, and production-grade debugging across Python and JavaScript.  

Every task reflects how I think, teach, and engineer: strategically, fast, and with intention. Whether it’s recursion, async logic, or prompt clarity, I build systems that help AI reason better.  

**Ready to contribute to Outlier AI’s mission — today.**



## **Task 1: Multi-Language Code Review — Python and JavaScript**

**Prompt:**  

Review the following recursive Python function and suggest improvements.

**Original Python Function:**

```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return 1 * factorial(n - 1)
```

**Response:**  

Correct, but the implementation lacks robustness. It doesn't validate input and risks stack overflow for large numbers.

**Optimized Python Version:**

```python
def factorial(n):
    if not isinstance(n, int) or n < 0:
        raise ValueError("n must be a non-negative integer")
    if n == 0:
        return 1
    return n * factorial(n - 1)
```

**JavaScript Version:**

```javascript
function factorial(n) {
  if (typeof n !== "number" || n < 0) {
    throw new Error("n must be a non-negative number");
  }
  if (n === 0) {
    return 1;
  } else {
    return n * factorial(n - 1);
  }
}
```



## **Task 2: Functional Debugging — JavaScript**

**Prompt:**  

Debug the following code and explain the issue.

**Original Code:**

```javascript
let x = 2;
let y = 5;
let z = y - x;
```

**Response:**  

This code is syntactically correct but lacks context. To make it functional, wrap it inside a function and return the result.

**Fixed Version:**

```javascript
function calculateDifference() {
  let x = 2;
  let y = 5;
  let z = y - x;
  return z;
}

calculateDifference(); // Returns: 3
```



## **Task 3: Production-Grade Debugging — JavaScript**

**Prompt:**  

Fix the following async function.

**Original Code:**

```javascript
async function fetchData() {
  let response = fetch('https://...');
  let data = await response.json();
  console.log(data);
}
```

**Issues:**

- Missing `await` before `fetch`
- No error handling
- No check for HTTP response status

**Fixed Version:**

```javascript
async function fetchData() {
  try {
    const response = await fetch('https://...');
    if (!response.ok) throw new Error("Network response was not ok");
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error("Fetch failed:", error);
  }
}
```



## **Task 4: Codebase Analysis and AI Training Prompt**

**Prompt:** 

Teach AI to explain recursion to a beginner.

**Response:**  

Recursion solves problems by calling the same function with simpler inputs. It’s useful for tasks like calculating factorials, generating Fibonacci numbers, or traversing tree structures.

**Example (Python):**

```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)
```

**Teaching Strategy:**

- Explain the base case (`n == 0`)
- Explain the recursive case (`n > 0`)
- Show how each call moves toward the base case



## **Task 5: Refactoring for Clarity — Python**

**Prompt:** 

Refactor the following function to improve readability, performance, and error handling.

**Original Code:**

```python
def process(data):
    for i in range(len(data)):
        if data[i] != None:
            data[i] = data[i].strip().lower()
    return data
```

**Refactored Version:**

```python
def process(data):
    if not isinstance(data, list):
        raise TypeError("Input must be a list")
    
    cleaned = []
    for item in data:
        if isinstance(item, str):
            cleaned.append(item.strip().lower())
        else:
            cleaned.append(None)
    
    return cleaned
```



## **Task 6: Refactoring for Clarity — JavaScript**

**Prompt:** 

Refactor the following function to improve readability and robustness.

**Original Code:**

```javascript
function process(data) {
  for (let i = 0; i < data.length; i++) {
    if (data[i] !== null) {
      data[i] = data[i].trim().toLowerCase();
    }
  }
  return data;
}
```

**Refactored Version:**

```javascript
function process(data) {
  if (!Array.isArray(data)) {
    throw new TypeError("Input must be an array");
  }

  return data.map(item => {
    if (typeof item === "string") {
      return item.trim().toLowerCase();
    }
    return null;
  });
}
```


## **Why It Works**

- AI is trained with code  
- Recursion is foundational  
- Clear structure avoids infinite loops  
- Teaching with examples improves model reasoning  
- Refactoring shows engineering maturity  
- Async handling reflects production standards



## **Closing Statement**

This portfolio reflects how I think, debug, and teach — strategically, clearly, and with precision.  
Each task simulates real-world annotation and engineering challenges, showing not just technical fluency but the ability to guide AI systems toward better reasoning.  

I’m ready to contribute to **Outlier AI’s mission** with clarity, speed, and intention.

