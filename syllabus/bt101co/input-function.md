---
layout: default
title: 2.6 The input() Function
course_code: BT101CO
permalink: /syllabus/bt101co/input-function/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>The <code>input()</code> function is the primary way to make a program interactive by allowing it to accept data from the user during execution. In Python, this function pauses the program and waits for the user to type something and press the <strong>Enter</strong> key.</p>
</div>

<div class="syllabus-section">
  <h2>1. Basic Syntax</h2>
  <div class="unit">
    <p>The syntax for the <code>input()</code> function is:</p>
    <p><code>Variable_Name = input("Optional Prompt Message")</code></p>
    <ul>
      <li><strong>Prompt Message:</strong> A string displayed on the screen to tell the user what kind of data is expected.</li>
      <li><strong>Return Value:</strong> Whatever the user types is assigned to the variable on the left.</li>
    </ul>
    <p><strong>Example:</strong></p>
    <pre><code class="language-python">name = input("Enter your name: ")
print("Hello", name)</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. The "String" Rule</h2>
  <div class="unit">
    <p>A critical concept is that the <code>input()</code> function <strong>always returns a string (<code>str</code>)</strong>, even if the user types a number.</p>
    <p>If you type <code>25</code>, Python treats it as the text <code>"25"</code>, not the mathematical value <code>25</code>. This means you cannot perform arithmetic on it directly without conversion.</p>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Type Casting (Conversion)</h2>
  <div class="unit">
    <p>To use the input as a number (integer or float), you must wrap the <code>input()</code> function inside a conversion function like <code>int()</code> or <code>float()</code>. This is known as <strong>Type Casting</strong>.</p>
    <ul>
      <li><strong>For Integers:</strong><br><code>age = int(input("Enter your age: "))</code></li>
      <li><strong>For Decimals:</strong><br><code>price = float(input("Enter the price: "))</code></li>
    </ul>
    <p><strong>What happens if you don't cast?</strong></p>
    <pre><code class="language-python">val = input("Enter a number: ")
print(val * 2) 
# If you enter 5, the output is '55' (string repetition), not 10.</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Reading Multiple Inputs</h2>
  <div class="unit">
    <p>While <code>input()</code> reads a single line, you can read multiple values at once using the <code>.split()</code> method. This is a common technique for competitive programming and quick data entry.</p>
    <p><strong>Example:</strong></p>
    <pre><code class="language-python"># User enters: Ashok 25 Kathmandu
name, age, city = input("Enter Name, Age, and City (separated by space): ").split()

print(f"User {name} is {age} years old and lives in {city}.")</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Summary Table</h2>
  
  <table class="exam-table">
    <thead>
      <tr>
        <th>Feature</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><strong>Purpose</strong></td>
        <td>To accept user input from the keyboard.</td>
      </tr>
      <tr>
        <td><strong>Default Type</strong></td>
        <td>Always returns data as a <strong>String</strong>.</td>
      </tr>
      <tr>
        <td><strong>Execution</strong></td>
        <td>Pauses the program until <strong>Enter</strong> is pressed.</td>
      </tr>
      <tr>
        <td><strong>Arithmetic</strong></td>
        <td>Requires <code>int()</code> or <code>float()</code> conversion before math.</td>
      </tr>
    </tbody>
  </table>
  
<div class="syllabus-section">
  <h2>6. Practical Example: The Interactive "Bill Calculator"</h2>
  <div class="unit">
    <p>This example combines <code>input()</code>, type casting, and formatted <code>print()</code> to solve a common real-world task.</p>
    <pre><code class="language-python"># Accepting user input
item_name = input("Enter the item name: ")
price = float(input(f"Enter the price of {item_name}: "))
quantity = int(input("How many are you buying? "))

# Calculating the total
total_cost = price * quantity

# Using f-string for a clean output
print(f"\n--- Receipt ---")
print(f"Item: {item_name}")
print(f"Total Amount: ${total_cost:.2f}")</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <p>By using <code>input()</code>, you transition from writing static scripts to creating dynamic applications that respond to real-world data.</p>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/assignment-of-values/">← Previous: 2.5 Assignment of Values</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/print-function/">Next: 2.7 The print() Function →</a>
    </div>
  </div>
  <div style="text-align: center; margin-top: 30px;">
    <a href="/syllabus/bt101co/" class="back-link">Back to Course Syllabus</a>
  </div>
</div>

<style>
.back-link {
  font-size: 0.9rem;
  font-weight: 600;
  text-decoration: none;
  color: var(--text-muted);
  border-bottom: 1px solid var(--border-color);
  padding-bottom: 4px;
  transition: all 0.2s ease;
}
.back-link:hover {
  color: var(--text-main);
  border-color: var(--text-main);
}
.topic-navigation {
  display: flex;
  justify-content: space-between;
  border-top: 1px solid var(--border-color);
  padding-top: 25px;
}
.topic-navigation a {
  text-decoration: none;
  font-weight: 700;
  color: var(--text-main);
  font-size: 0.95rem;
}
.topic-navigation a:hover {
  color: var(--secondary);
}
pre {
  background: var(--bg-secondary);
  padding: 15px;
  border-radius: 6px;
  overflow-x: auto;
}
code {
  font-family: 'Courier New', Courier, monospace;
}
</style>
