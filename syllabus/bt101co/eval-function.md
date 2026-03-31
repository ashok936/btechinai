---
layout: default
title: 2.8 The eval() Function
course_code: BT101CO
permalink: /syllabus/bt101co/eval-function/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>The <code>eval()</code> function is a powerful, built-in Python tool that takes a <strong>string</strong> as an argument, parses it as a <strong>Python expression</strong>, and executes it as code. Essentially, it allows Python to run code that is generated or received as text during the program's execution.</p>
</div>

<div class="syllabus-section">
  <h2>1. Basic Syntax</h2>
  <div class="unit">
    <p>The syntax for the <code>eval()</code> function is:</p>
    <p><code>Result = eval("Expression_String")</code></p>
    <ul>
      <li><strong>Expression_String:</strong> A string containing a valid Python expression (like math or a function call).</li>
      <li><strong>Result:</strong> The value returned after the expression is evaluated.</li>
    </ul>
    <p><strong>Example:</strong></p>
    <pre><code class="language-python">x = 10
result = eval("x + 5")
print(result) # Output: 15</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Using eval() with input()</h2>
  <div class="unit">
    <p>A common use case for <code>eval()</code> is to handle user input that might be an integer, a float, or even a list, without needing multiple <code>int()</code> or <code>float()</code> conversions. It "guesses" the correct data type based on what the user types.</p>
    <p><strong>Example:</strong></p>
    <pre><code class="language-python">data = eval(input("Enter something (number/list/tuple): "))
print(type(data)) 
# If user enters 10.5, type is <class 'float'>
# If user enters [1, 2], type is <class 'list'></code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Advanced eval() Examples</h2>
  <div class="unit">
    <p><strong>Example: Dynamic Math Formula Solver</strong></p>
    <p>The <code>eval()</code> function is perfect when you want the user to provide a full mathematical expression rather than just a single number.</p>
    <pre><code class="language-python"># A simple "Formula Solver"
formula = input("Enter a math expression (e.g., 2 + 3 * 5): ")

# eval() handles the order of operations (BODMAS/PEMDAS) automatically
result = eval(formula)

print(f"The result of '{formula}' is: {result}")</code></pre>

    <p><strong>Example: Parsing Data Structures</strong></p>
    <p>One of the most unique features of <code>eval()</code> is its ability to recognize Python's "Sequence" types (Lists, Tuples, Dictionaries) directly from a string.</p>
    <pre><code class="language-python"># User inputs a list: [10, 20, 30]
user_list = eval(input("Enter a list of numbers: "))

print("You entered a:", type(user_list))
print("The first element is:", user_list[0])
print("The sum is:", sum(user_list))</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. The Security Risk (Important!)</h2>
  <div class="unit">
    <p>While <code>eval()</code> is convenient, it is considered <strong>dangerous</strong> when used with untrusted user input. Because <code>eval()</code> executes any string as code, a malicious user could type a command to delete files or crash your system.</p>
    
    <blockquote style="border-left: 3px solid #ff4d4d; padding-left: 20px; color: #d32f2f; font-style: italic; margin: 20px 0; background: #fff5f5; padding-top: 10px; padding-bottom: 10px;">
      <strong>Warning:</strong> Never use <code>eval()</code> on input from a source you do not trust. For safer numerical evaluation, many developers prefer using <code>ast.literal_eval()</code>.
    </blockquote>
  </div>
</div>

<div class="syllabus-section">
  <h2>Summary Table</h2>
  
  <table class="exam-table">
    <thead>
      <tr>
        <th>Feature</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><strong>Input</strong></td>
        <td>A string representing a Python expression.</td>
      </tr>
      <tr>
        <td><strong>Action</strong></td>
        <td>Parses and executes the string as live code.</td>
      </tr>
      <tr>
        <td><strong>Return</strong></td>
        <td>The result of the evaluated expression.</td>
      </tr>
      <tr>
        <td><strong>Limitation</strong></td>
        <td>Cannot execute statements (like loops or assignments).</td>
      </tr>
      <tr>
        <td><strong>Risk</strong></td>
        <td>Can execute harmful code if input is not controlled.</td>
      </tr>
    </tbody>
  </table>
  
  <p><code>eval()</code> is often described as a "double-edged sword"—it provides incredible flexibility for dynamic problem solving, but requires careful handling to keep your program secure.</p>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/print-function/">← Previous: 2.7 The print() Function</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/arithmetic-operators/">Next: 3.1 Arithmetic Operators →</a>
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
