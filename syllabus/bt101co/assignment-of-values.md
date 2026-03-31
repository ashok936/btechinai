---
layout: default
title: 2.5 Assignment of Values to Variables
course_code: BT101CO
permalink: /syllabus/bt101co/assignment-of-values/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>Assigning values to variables is the process of storing data in a memory location and giving it a specific name for future reference. In Python, the <strong><code>=</code></strong> (equals sign) is used as the <strong>Assignment Operator</strong>.</p>
  <p>It is important to remember that in an assignment statement, the right-hand side is evaluated first, and the resulting value is then "tagged" with the name on the left-hand side.</p>
</div>

<div class="syllabus-section">
  <h2>1. Basic Assignment</h2>
  <div class="unit">
    <p>The most common way to assign a value is by using a single variable name and a single value.</p>
    <ul>
      <li><strong>Syntax:</strong> <code>Variable_Name = Value</code></li>
      <li><strong>Example:</strong> <code>age = 25</code></li>
    </ul>
    <p>Here, <code>age</code> is the identifier (name) and <code>25</code> is the integer literal (value).</p>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Multiple Assignment (Same Value)</h2>
  <div class="unit">
    <p>Python allows you to assign the same value to multiple variables in a single line. This is useful for initializing several counters or flags to the same starting point.</p>
    <ul>
      <li><strong>Syntax:</strong> <code>Var1 = Var2 = Var3 = Value</code></li>
      <li><strong>Example:</strong> <code>x = y = z = 0</code></li>
    </ul>
    <p>All three variables (<code>x</code>, <code>y</code>, and <code>z</code>) now point to the same memory object <code>0</code>.</p>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Multiple Assignment (Different Values)</h2>
  <div class="unit">
    <p>You can also assign different values to multiple variables simultaneously in one line. This is often called <strong>Tuple Unpacking</strong>.</p>
    <ul>
      <li><strong>Syntax:</strong> <code>Var1, Var2, Var3 = Val1, Val2, Val3</code></li>
      <li><strong>Example:</strong> <code>name, roll_no, marks = "Ashok", 10, 85.5</code></li>
    </ul>
    <p><code>"Ashok"</code> is assigned to <code>name</code>, <code>10</code> to <code>roll_no</code>, and <code>85.5</code> to <code>marks</code>.</p>
    <p><em>Note:</em> The number of variables on the left must exactly match the number of values on the right.</p>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Re-assignment</h2>
  <div class="unit">
    <p>Because Python is <strong>dynamically typed</strong>, you can re-assign a variable to a completely different data type later in the program.</p>
    <p><strong>Example:</strong></p>
    <pre><code class="language-python">data = 100      # 'data' is an integer
data = "Python" # 'data' is now a string</code></pre>
    <p>The previous value (<code>100</code>) is orphaned in memory and eventually cleaned up by Python's garbage collector.</p>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Augmented (Compound) Assignment</h2>
  <div class="unit">
    <p>Python provides shorthand operators to perform a mathematical operation and an assignment in one step. These are common in loops and counters.</p>
    
    <table class="exam-table">
      <thead>
        <tr>
          <th>Operator</th>
          <th>Example</th>
          <th>Equivalent to</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><code>+=</code></td>
          <td><code>x += 5</code></td>
          <td><code>x = x + 5</code></td>
        </tr>
        <tr>
          <td><code>-=</code></td>
          <td><code>x -= 2</code></td>
          <td><code>x = x - 2</code></td>
        </tr>
        <tr>
          <td><code>*=</code></td>
          <td><code>x *= 3</code></td>
          <td><code>x = x * 3</code></td>
        </tr>
        <tr>
          <td><code>/=</code></td>
          <td><code>x /= 4</code></td>
          <td><code>x = x / 4</code></td>
        </tr>
        <tr>
          <td><code>%=</code></td>
          <td><code>x %= 2</code></td>
          <td><code>x = x % 2</code></td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<div class="syllabus-section">
  <h2>6. Dynamic Typing and Memory</h2>
  <div class="unit">
    <p>When you assign a value, Python does the following:</p>
    <ol>
      <li>Creates an <strong>object</strong> in memory for the value (e.g., <code>5</code>).</li>
      <li>Creates a <strong>variable</strong> (e.g., <code>a</code>).</li>
      <li>Links the variable to that object.</li>
    </ol>
    <p>If you then say <code>b = a</code>, Python does not create a new <code>5</code>. It simply links the variable <code>b</code> to the <strong>existing</strong> object <code>5</code> that <code>a</code> is already pointing to.</p>
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/variables/">← Previous: 2.4 Variables</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/input-function/">Next: 2.6 The input() Function →</a>
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
