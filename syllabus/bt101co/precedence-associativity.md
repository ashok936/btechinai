---
layout: default
title: 3.2 Operator Precedence and Associativity
course_code: BT101CO
permalink: /syllabus/bt101co/precedence-associativity/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>When multiple operators appear in a single expression, Python follows a specific order of priority to decide which calculation to perform first. This rule is similar to BODMAS or PEMDAS in mathematics.</p>
</div>

<div class="syllabus-section">
  <h2>1. Operator Precedence (The hierarchy)</h2>
  <div class="unit">
    <p>The hierarchy of operations is as follows (from highest priority to lowest):</p>
    <ol>
      <li><strong>Parentheses <code>()</code>:</strong> Highest priority. Anything inside parentheses is calculated first.</li>
      <li><strong>Exponentiation <code>**</code>:</strong> Power calculations come second.</li>
      <li><strong>Multiplication, Division, Floor Division, Modulus <code>*</code>, <code>/</code>, <code>//</code>, <code>%</code>:</strong> These are evaluated third, from left to right.</li>
      <li><strong>Addition, Subtraction <code>+</code>, <code>-</code>:</strong> These are evaluated last, from left to right.</li>
    </ol>
    
    <p><strong>Example:</strong></p>
    <pre><code class="language-python">result = 10 + 2 * 3 ** 2
# 1. Power first: 3 ** 2 = 9
# 2. Multiply second: 2 * 9 = 18
# 3. Add last: 10 + 18 = 28
print(result) # Output: 28</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Understanding Associativity</h2>
  <div class="unit">
    <p>What happens when two operators have the same level of priority? This is where <strong>associativity</strong> comes in. It determines whether the expression is evaluated from left to right or right to left.</p>
    
    <ul>
      <li><strong>Left-to-Right Associativity:</strong> Most operators in Python are left-associative.
        <br>Example: <code>100 / 10 * 2</code> &rarr; <code>(100 / 10) * 2</code> &rarr; <code>20.0</code>
      </li>
      <li><strong>Right-to-Left Associativity:</strong> The exponentiation operator (<code>**</code>) is right-associative.
        <br>Example: <code>2 ** 3 ** 2</code> &rarr; <code>2 ** (3 ** 2)</code> &rarr; <code>2 ** 9</code> &rarr; <code>512</code>
      </li>
    </ul>
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/arithmetic-operators/">← Previous: 3.1 Arithmetic Operators</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/bitwise-operator/">Next: 3.3 Bitwise Operator →</a>
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
