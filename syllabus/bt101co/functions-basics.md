---
layout: default
title: "5.1 Syntax and basics of a function"
course_code: BT101CO
permalink: /syllabus/bt101co/functions-basics/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>In the logic of problem-solving, a <strong>Function</strong> is a self-contained block of code that performs a specific task. Functions allow you to write code once and "call" it multiple times, which follows the <strong>DRY (Don't Repeat Yourself)</strong> principle.</p>
</div>

<div class="syllabus-section">
  <h2>1. Function Syntax</h2>
  <div class="unit">
    <p>To define a function in Python, you use the <code>def</code> keyword.</p>
    <pre><code class="language-python"># Structure:
def function_name(parameters):
    """Docstring: Optional description of the function"""
    # Body of the function (indented)
    return value # Optional</code></pre>

    <ul>
      <li><strong><code>def</code></strong>: The keyword that starts the function definition.</li>
      <li><strong>Function Name</strong>: A unique identifier following the same rules as variables.</li>
      <li><strong>Parameters</strong>: Inputs listed inside parentheses (optional).</li>
      <li><strong>Colon (<code>:</code>)</strong>: Marks the end of the header.</li>
      <li><strong>Indentation</strong>: The code block belonging to the function must be indented.</li>
      <li><strong><code>return</code></strong>: Sends a result back to the caller and exits the function.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Basic Components of a Function</h2>
  <div class="unit">
    <h3>Defining vs. Calling</h3>
    <p>Defining a function just stores the logic. To actually execute the code, you must "call" it by its name followed by parentheses.</p>
    <pre><code class="language-python"># 1. Defining
def greet():
    print("Hello! Welcome to Python.")

# 2. Calling
greet() </code></pre>

    <h3>Parameters and Arguments</h3>
    <ul>
      <li><strong>Parameters</strong>: The variables listed in the function definition (the "placeholders").</li>
      <li><strong>Arguments</strong>: The actual values passed to the function when it is called.</li>
    </ul>
    <pre><code class="language-python">def add_numbers(a, b): # a and b are parameters
    sum = a + b
    print(f"The sum is: {sum}")

add_numbers(10, 20)    # 10 and 20 are arguments</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. The <code>return</code> Statement</h2>
  <div class="unit">
    <p>A function can either perform an action (like <code>print()</code>) or calculate a result and <strong>return</strong> it to the main program. Once a <code>return</code> is executed, the function stops immediately.</p>
    <pre><code class="language-python">def multiply(x, y):
    return x * y

# The returned value is stored in a variable
result = multiply(5, 4)
print(result) # Output: 20</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Types of Functions</h2>
  <div class="unit">
    <ol>
      <li><strong>Built-in Functions</strong>: Functions already provided by Python (e.g., <code>print()</code>, <code>input()</code>, <code>len()</code>, <code>range()</code>).</li>
      <li><strong>User-defined Functions</strong>: Functions created by the programmer to solve specific problems.</li>
    </ol>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Why Use Functions?</h2>
  <div class="unit">
    <p>From a "Problem Solving" perspective, functions are essential for:</p>
    <ul>
      <li><strong>Modularity</strong>: Breaking a complex problem into smaller, manageable pieces.</li>
      <li><strong>Reusability</strong>: Writing the logic once and using it across different parts of the program.</li>
      <li><strong>Readability</strong>: Code is much easier to read when tasks are named clearly (e.g., <code>calculate_tax()</code>).</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>Summary Checklist</h2>
  <table class="exam-table">
    <thead>
      <tr>
        <th>Component</th>
        <th>Required?</th>
        <th>Purpose</th>
      </tr>
    </thead>
    <tbody>
      <tr><td><strong><code>def</code> keyword</strong></td><td>Yes</td><td>Tells Python you are starting a function.</td></tr>
      <tr><td><strong>Parentheses <code>()</code></strong></td><td>Yes</td><td>Holds input parameters.</td></tr>
      <tr><td><strong>Colon <code>:</code></strong></td><td>Yes</td><td>Indicates the start of the code block.</td></tr>
      <tr><td><strong>Indentation</strong></td><td>Yes</td><td>Defines the scope of the function.</td></tr>
      <tr><td><strong><code>return</code></strong></td><td>No</td><td>Used if you need to send a value back.</td></tr>
    </tbody>
  </table>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/extra-control/">← Previous: 4.3 Control Statements</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/use-of-functions/">Next: 5.2 Use of a Function →</a>
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
