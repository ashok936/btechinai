---
layout: default
title: "5.7 Creating Lists"
course_code: BT101CO
permalink: /syllabus/bt101co/creating-lists/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>In Python, a <strong>List</strong> is a versatile, ordered collection of items that can hold different data types (integers, strings, even other lists). Lists are <strong>mutable</strong>, meaning you can change their content after they are created.</p>
</div>

<div class="syllabus-section">
  <h2>1. Simple Assignment (Square Brackets)</h2>
  <div class="unit">
    <p>The most common way to create a list is by placing comma-separated values inside square brackets <code>[]</code>.</p>
    <ul>
      <li><strong>Empty List:</strong> <code>my_list = []</code></li>
      <li><strong>Homogeneous List (Same types):</strong> <code>numbers = [10, 20, 30, 40]</code></li>
      <li><strong>Heterogeneous List (Mixed types):</strong> <code>student = ["Ashok", 101, 85.5, True]</code></li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Using the <code>list()</code> Constructor</h2>
  <div class="unit">
    <p>You can convert other "iterable" objects (like strings, tuples, or ranges) into a list using the built-in <code>list()</code> function.</p>
    <ul>
      <li><strong>From a String:</strong> <code>chars = list("PYTHON")</code> &rarr; <code>['P', 'Y', 'T', 'H', 'O', 'N']</code></li>
      <li><strong>From a Range:</strong> <code>nums = list(range(1, 6))</code> &rarr; <code>[1, 2, 3, 4, 5]</code></li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. List Comprehension</h2>
  <div class="unit">
    <p>List comprehension offers a shorter syntax to create a new list based on the values of an existing list or range. It combines a <code>for</code> loop and an optional <code>if</code> condition into one line.</p>
    <p><strong>Syntax:</strong> <code>[expression for item in iterable if condition]</code></p>
    <p><strong>Example: Creating a list of squares</strong></p>
    <pre><code class="language-python"># Standard way
squares = []
for x in range(1, 6):
    squares.append(x**2)

# List Comprehension way
squares = [x**2 for x in range(1, 6)]
# Result: [1, 4, 9, 16, 25]</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Input-Based List Creation</h2>
  <div class="unit">
    <p>In many programming problems, you need to create a list from user input. There are two common patterns for this:</p>
    
    <h3>A. Using a Loop and <code>append()</code></h3>
    <pre><code class="language-python">n = int(input("How many items? "))
my_list = []
for i in range(n):
    val = input(f"Enter item {i+1}: ")
    my_list.append(val)</code></pre>

    <h3>B. Using <code>split()</code> (Single Line Input)</h3>
    <p>If the user enters items separated by spaces (e.g., <code>10 20 30</code>), you can capture them all at once.</p>
    <pre><code class="language-python">data = input("Enter numbers separated by space: ").split()
# if input is "10 20 30", data becomes ['10', '20', '30']</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Summary Table: List Creation Methods</h2>
  <table class="exam-table">
    <thead>
      <tr>
        <th>Method</th>
        <th>Syntax Example</th>
        <th>Best Used For...</th>
      </tr>
    </thead>
    <tbody>
      <tr><td><strong>Square Brackets</strong></td><td><code>L = [1, 2, 3]</code></td><td>When you already know the items.</td></tr>
      <tr><td><strong><code>list()</code> Constructor</strong></td><td><code>L = list(range(5))</code></td><td>Converting other types to a list.</td></tr>
      <tr><td><strong>Comprehension</strong></td><td><code>[x for x in L]</code></td><td>Transforming or filtering existing data.</td></tr>
      <tr><td><strong><code>append()</code> loop</strong></td><td><code>L.append(x)</code></td><td>Building a list dynamically.</td></tr>
    </tbody>
  </table>
</div>

<div class="syllabus-section">
  <h2>Key List Properties to Remember</h2>
  <div class="unit">
    <ul>
      <li><strong>Ordered:</strong> The items have a defined order that will not change.</li>
      <li><strong>Indexed:</strong> You access items by their position (starting from <strong>0</strong>).</li>
      <li><strong>Mutable:</strong> You can add, remove, or change items.</li>
      <li><strong>Dynamic:</strong> A list can grow or shrink in size as needed.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/lambda-functions/">← Previous: 5.6 The lambda function</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/accessing-lists/">Next: 5.8 Accessing elements of a List →</a>
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
