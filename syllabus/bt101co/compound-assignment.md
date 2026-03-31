---
layout: default
title: "3.4 Compound Assignment, Boolean, and Relational Operators"
course_code: BT101CO
permalink: /syllabus/bt101co/compound-assignment/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>This section covers operators that are essential for updating variables, comparing values, and building logical conditions. These form the building blocks of <strong>Decision Making</strong> in programming.</p>
</div>

<div class="syllabus-section">
  <h2>1. Augmented (Compound) Assignment Operators</h2>
  <div class="unit">
    <p>These are shorthand ways to update a variable based on its current value. Instead of writing <code>x = x + 5</code>, you can simply write <code>x += 5</code>.</p>
    <table class="exam-table">
      <thead>
        <tr>
          <th>Operator</th>
          <th>Name</th>
          <th>Example</th>
          <th>Equivalent to</th>
        </tr>
      </thead>
      <tbody>
        <tr><td><code>+=</code></td><td>Addition Assignment</td><td><code>a += 5</code></td><td><code>a = a + 5</code></td></tr>
        <tr><td><code>-=</code></td><td>Subtraction Assignment</td><td><code>a -= 3</code></td><td><code>a = a - 3</code></td></tr>
        <tr><td><code>*=</code></td><td>Multiplication Assignment</td><td><code>a *= 2</code></td><td><code>a = a * 2</code></td></tr>
        <tr><td><code>/=</code></td><td>Division Assignment</td><td><code>a /= 4</code></td><td><code>a = a / 4</code></td></tr>
        <tr><td><code>//=</code></td><td>Floor Division Assignment</td><td><code>a //= 3</code></td><td><code>a = a // 3</code></td></tr>
        <tr><td><code>%=</code></td><td>Modulus Assignment</td><td><code>a %= 2</code></td><td><code>a = a % 2</code></td></tr>
        <tr><td><code>**=</code></td><td>Exponent Assignment</td><td><code>a **= 2</code></td><td><code>a = a ** 2</code></td></tr>
      </tbody>
    </table>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Relational Operators (Comparison Tools)</h2>
  <div class="unit">
    <p>Relational operators are the "questions" that Python asks to return a <strong>Boolean</strong> (<code>True</code> or <code>False</code>). They are used to compare two values.</p>
    <table class="exam-table">
      <thead>
        <tr>
          <th>Operator</th>
          <th>Meaning</th>
          <th>Example</th>
          <th>Result</th>
        </tr>
      </thead>
      <tbody>
        <tr><td><code>==</code></td><td>Equal to</td><td><code>5 == 5</code></td><td><code>True</code></td></tr>
        <tr><td><code>!=</code></td><td>Not equal to</td><td><code>5 != 3</code></td><td><code>True</code></td></tr>
        <tr><td><code>></code></td><td>Greater than</td><td><code>5 > 8</code></td><td><code>False</code></td></tr>
        <tr><td><code><</code></td><td>Less than</td><td><code>2 < 4</code></td><td><code>True</code></td></tr>
        <tr><td><code>>=</code></td><td>Greater than or equal to</td><td><code>5 >= 5</code></td><td><code>True</code></td></tr>
        <tr><td><code><=</code></td><td>Less than or equal to</td><td><code>3 <= 2</code></td><td><code>False</code></td></tr>
      </tbody>
    </table>
    
    <div style="background: #fff5f5; border-left: 4px solid #ff4d4d; padding: 15px; margin-top: 20px;">
      <strong>⚠️ Common Mistake: <code>=</code> vs <code>==</code></strong>
      <p><code>=</code> is for <strong>Assignment</strong> (storing a value).<br>
      <code>==</code> is for <strong>Comparison</strong> (checking if values are equal).</p>
      <p><em>Example: <code>if age = 18:</code> will cause a Syntax Error. Use <code>if age == 18:</code></em></p>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Logical Operators (Boolean Operators)</h2>
  <div class="unit">
    <p>Sometimes a single comparison isn't enough. Logical operators allow you to combine multiple conditions.</p>
    <ul>
      <li><strong><code>and</code>:</strong> Returns <code>True</code> only if <strong>both</strong> sides are True.</li>
      <li><strong><code>or</code>:</strong> Returns <code>True</code> if <strong>at least one</strong> side is True.</li>
      <li><strong><code>not</code>:</strong> Inverts the result (True becomes False, False becomes True).</li>
    </ul>
    
    <p><strong>Example: Scholarship Eligibility</strong></p>
    <pre><code class="language-python">gpa = 3.8
attendance = 95

# Both conditions must be met
if gpa >= 3.5 and attendance >= 90:
    print("Eligible for scholarship")</code></pre>
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/bitwise-operator/">← Previous: 3.3 Bitwise Operator</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/decision-making/">Next: 4.1 Decision Making →</a>
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
