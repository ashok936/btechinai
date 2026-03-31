---
layout: default
title: 3.1 Arithmetic Operators
course_code: BT101CO
permalink: /syllabus/bt101co/arithmetic-operators/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>Arithmetic operators are used to perform mathematical calculations such as addition, subtraction, multiplication, and division. They are the most common tokens used for numerical problem-solving.</p>
</div>

<div class="syllabus-section">
  <h2>1. Basic Arithmetic Operators</h2>
  <div class="unit">
    <p>These operators follow the standard rules of mathematics.</p>
    <ul>
      <li><strong>Addition (<code>+</code>):</strong> Adds two operands.
        <br><code>10 + 5</code> &rarr; <code>15</code>
      </li>
      <li><strong>Subtraction (<code>-</code>):</strong> Subtracts the right operand from the left.
        <br><code>10 - 5</code> &rarr; <code>5</code>
      </li>
      <li><strong>Multiplication (<code>*</code>):</strong> Multiplies two operands.
        <br><code>10 * 5</code> &rarr; <code>50</code>
      </li>
      <li><strong>Division (<code>/</code>):</strong> Divides the left operand by the right and <strong>always</strong> returns a float (decimal).
        <br><code>10 / 4</code> &rarr; <code>2.5</code>
      </li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Specialized Arithmetic Operators</h2>
  <div class="unit">
    <p>Python includes specific operators for handling remainders, powers, and integer-only division.</p>
    
    <h3>Modulus (<code>%</code>)</h3>
    <p>Returns the <strong>remainder</strong> of a division. It is highly useful for checking if a number is even or odd (e.g., <code>x % 2 == 0</code>).</p>
    <p><code>10 % 3</code> &rarr; <code>1</code> (because 3 goes into 10 three times with 1 left over).</p>

    <h3>Exponentiation (<code>**</code>)</h3>
    <p>Calculates the power of a number (Left operand raised to the power of the right).</p>
    <p><code>2 ** 3</code> &rarr; <code>8</code> (2 &times; 2 &times; 2)</p>

    <h3>Floor Division (<code>//</code>)</h3>
    <p>Divides the operands and <strong>discards the fractional part</strong>, returning only the whole number (integer).</p>
    <ul>
      <li><code>10 // 4</code> &rarr; <code>2</code> (the <code>.5</code> is dropped).</li>
      <li><code>-10 // 4</code> &rarr; <code>-3</code> (it rounds toward the lower integer).</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Arithmetic with Different Data Types</h2>
  <div class="unit">
    <p>Python handles calculations between integers and floats automatically through <strong>Implicit Type Conversion</strong>.</p>
    <ul>
      <li><strong>Int + Int = Int</strong> (<code>5 + 5 = 10</code>)</li>
      <li><strong>Int + Float = Float</strong> (<code>5 + 5.0 = 10.0</code>)</li>
      <li><strong>Float + Float = Float</strong> (<code>5.2 + 4.8 = 10.0</code>)</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>Summary Table</h2>
  <table class="exam-table">
    <thead>
      <tr>
        <th>Operator</th>
        <th>Name</th>
        <th>Example</th>
        <th>Result</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><code>+</code></td>
        <td>Addition</td>
        <td><code>5 + 2</code></td>
        <td><code>7</code></td>
      </tr>
      <tr>
        <td><code>-</code></td>
        <td>Subtraction</td>
        <td><code>5 - 2</code></td>
        <td><code>3</code></td>
      </tr>
      <tr>
        <td><code>*</code></td>
        <td>Multiplication</td>
        <td><code>5 * 2</code></td>
        <td><code>10</code></td>
      </tr>
      <tr>
        <td><code>/</code></td>
        <td>Division</td>
        <td><code>5 / 2</code></td>
        <td><code>2.5</code></td>
      </tr>
      <tr>
        <td><code>//</code></td>
        <td>Floor Division</td>
        <td><code>5 // 2</code></td>
        <td><code>2</code></td>
      </tr>
      <tr>
        <td><code>%</code></td>
        <td>Modulus</td>
        <td><code>5 % 2</code></td>
        <td><code>1</code></td>
      </tr>
      <tr>
        <td><code>**</code></td>
        <td>Exponent</td>
        <td><code>5 ** 2</code></td>
        <td><code>25</code></td>
      </tr>
    </tbody>
  </table>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/eval-function/">← Previous: 2.8 The eval() Function</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/precedence-associativity/">Next: 3.2 Operator Precedence and Associativity →</a>
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
