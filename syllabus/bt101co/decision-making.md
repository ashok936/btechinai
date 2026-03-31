---
layout: default
title: "4.1 Decision Making: if-else, if-elif-else"
course_code: BT101CO
permalink: /syllabus/bt101co/decision-making/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>Decision making in Python allows a program to execute specific blocks of code only when certain conditions are met. These are often called <strong>Conditional Statements</strong>.</p>
</div>

<div class="syllabus-section">
  <h2>1. The <code>if</code> Statement</h2>
  <div class="unit">
    <p>The simplest form of decision making. If the condition is <strong>True</strong>, the indented block of code runs. If it is <strong>False</strong>, Python skips it.</p>
    <pre><code class="language-python"># Syntax:
if condition:
    # code to execute if True

# Example:
age = 20
if age >= 18:
    print("You are an adult.")</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. The <code>if-else</code> Statement</h2>
  <div class="unit">
    <p>This provides an alternative path. If the <code>if</code> condition is <strong>False</strong>, the <code>else</code> block executes. It is an "either-or" scenario.</p>
    <pre><code class="language-python"># Syntax:
if condition:
    # runs if True
else:
    # runs if False

# Example:
marks = 35
if marks >= 40:
    print("Result: Pass")
else:
    print("Result: Fail")</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. The <code>if-elif-else</code> Ladder</h2>
  <div class="unit">
    <p>When you have <strong>multiple conditions</strong> to check, you use <code>elif</code> (short for "else if"). Python checks them in order from top to bottom. As soon as one is <strong>True</strong>, it executes that block and exits the entire ladder.</p>
    <pre><code class="language-python"># Syntax:
if condition1:
    # Block 1
elif condition2:
    # Block 2
else:
    # Default Block

# Example (Grading System):
score = 85
if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
elif score >= 70:
    print("Grade: C")
else:
    print("Grade: F")</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Key Rules to Remember</h2>
  <div class="unit">
    <ol>
      <li><strong>The Colon (<code>:</code>):</strong> Every <code>if</code>, <code>elif</code>, and <code>else</code> line must end with a colon.</li>
      <li><strong>Indentation:</strong> Python uses whitespace to define blocks of code. All lines inside a specific condition must be indented equally (usually 4 spaces).</li>
      <li><strong>The <code>else</code> is Optional:</strong> You can have an <code>if</code> without an <code>else</code>, but you cannot have an <code>else</code> without a preceding <code>if</code>.</li>
    </ol>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Nested <code>if</code> Statements</h2>
  <div class="unit">
    <p>You can place an <code>if</code> statement inside another <code>if</code> statement for more complex "Problem Solving" logic.</p>
    <p><strong>Example:</strong></p>
    <pre><code class="language-python">num = 10
if num >= 0:
    if num == 0:
        print("Zero")
    else:
        print("Positive number")
else:
    print("Negative number")</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>6. Solved Example: BMI (Body Mass Index) Calculator</h2>
  <div class="unit">
    <p>Let's build a program that takes weight and height, calculates BMI, and categorizes it.</p>
    <pre><code class="language-python"># Step 1: Get user input
weight = float(input("Enter your weight in kg: "))
height = float(input("Enter your height in meters: "))

# Step 2: Calculate BMI formula: weight / height^2
bmi = weight / (height ** 2)
print(f"Your BMI is: {bmi:.2f}")

# Step 3: Decision Making with if-elif-else
if bmi < 18.5:
    print("Category: Underweight")
elif bmi >= 18.5 and bmi < 25:
    print("Category: Normal weight")
elif bmi >= 25 and bmi < 30:
    print("Category: Overweight")
else:
    print("Category: Obese")</code></pre>
    
    <table class="exam-table" style="margin-top: 20px;">
      <thead>
        <tr>
          <th>Tool</th>
          <th>Type</th>
          <th>Purpose in Example</th>
        </tr>
      </thead>
      <tbody>
        <tr><td><code>float()</code></td><td>Type Casting</td><td>Converted text input into numbers.</td></tr>
        <tr><td><code>**</code></td><td>Arithmetic</td><td>Squared the height for the formula.</td></tr>
        <tr><td><code>bmi:.2f</code></td><td>Formatting</td><td>Rounded the output for readability.</td></tr>
        <tr><td><code>if-elif-else</code></td><td>Decision</td><td>Categorized the result.</td></tr>
      </tbody>
    </table>
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/compound-assignment/">← Previous: 3.4 Compound Assignment, Boolean, and Relational Operators</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/">Next: 4.2 Loop Control →</a>
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
