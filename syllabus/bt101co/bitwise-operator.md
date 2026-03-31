---
layout: default
title: 3.3 Bitwise Operator
course_code: BT101CO
permalink: /syllabus/bt101co/bitwise-operator/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>Bitwise operators are used to perform operations at the <strong>binary level</strong> (0s and 1s). While most programming happens at a higher level, bitwise operations are extremely fast and memory-efficient.</p>
</div>

<div class="syllabus-section">
  <h2>1. The Core Bitwise Operators</h2>
  <table class="exam-table">
    <thead>
      <tr>
        <th>Operator</th>
        <th>Name</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><code>&</code></td>
        <td><strong>AND</strong></td>
        <td>Sets bit to 1 if <strong>both</strong> bits are 1.</td>
      </tr>
      <tr>
        <td><code>|</code></td>
        <td><strong>OR</strong></td>
        <td>Sets bit to 1 if <strong>one or both</strong> bits are 1.</td>
      </tr>
      <tr>
        <td><code>^</code></td>
        <td><strong>XOR</strong></td>
        <td>Sets bit to 1 if <strong>only one</strong> bit is 1 (exclusive OR).</td>
      </tr>
      <tr>
        <td><code>~</code></td>
        <td><strong>NOT</strong></td>
        <td>Inverts all bits (1 becomes 0, 0 becomes 1).</td>
      </tr>
      <tr>
        <td><code><<</code></td>
        <td><strong>Left Shift</strong></td>
        <td>Shifts bits to the left, filling with 0s from the right.</td>
      </tr>
      <tr>
        <td><code>>></code></td>
        <td><strong>Right Shift</strong></td>
        <td>Shifts bits to the right, discarding bits on the right.</td>
      </tr>
    </tbody>
  </table>
</div>

<div class="syllabus-section">
  <h2>2. Solved Examples</h2>
  <div class="unit">
    <h3>Example A: Bitwise AND (<code>&</code>)</h3>
    <p><strong>Problem:</strong> Calculate <code>12 & 7</code></p>
    <ol>
      <li>Binary of 12: <code>1 1 0 0</code></li>
      <li>Binary of 7: <code>0 1 1 1</code></li>
      <li>Apply AND:
        <ul>
          <li><code>1 & 0 = 0</code></li>
          <li><code>1 & 1 = 1</code></li>
          <li><code>0 & 1 = 0</code></li>
          <li><code>0 & 1 = 0</code></li>
        </ul>
      </li>
    </ol>
    <p><strong>Result:</strong> <code>0 1 0 0</code> (which is <strong>4</strong> in decimal).</p>

    <h3>Example B: Bitwise OR (<code>|</code>)</h3>
    <p><strong>Problem:</strong> Calculate <code>12 | 7</code></p>
    <ol>
      <li>Binary of 12: <code>1 1 0 0</code></li>
      <li>Binary of 7: <code>0 1 1 1</code></li>
      <li>Apply OR:
        <ul>
          <li><code>1 | 0 = 1</code></li>
          <li><code>1 | 1 = 1</code></li>
          <li><code>0 | 1 = 1</code></li>
          <li><code>0 | 1 = 1</code></li>
        </ul>
      </li>
    </ol>
    <p><strong>Result:</strong> <code>1 1 1 1</code> (which is <strong>15</strong> in decimal).</p>

    <h3>Example C: Bitwise XOR (<code>^</code>)</h3>
    <p><strong>Problem:</strong> Calculate <code>12 ^ 7</code></p>
    <ol>
      <li>Binary of 12: <code>1 1 0 0</code></li>
      <li>Binary of 7: <code>0 1 1 1</code></li>
      <li>Apply XOR (1 if bits are different):
        <ul>
          <li><code>1 ^ 0 = 1</code></li>
          <li><code>1 ^ 1 = 0</code></li>
          <li><code>0 ^ 1 = 1</code></li>
          <li><code>0 ^ 1 = 1</code></li>
        </ul>
      </li>
    </ol>
    <p><strong>Result:</strong> <code>1 0 1 1</code> (which is <strong>11</strong> in decimal).</p>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Bitwise Shift Operators</h2>
  <div class="unit">
    <p>These move bits like a conveyor belt. They are often used for very fast multiplication or division by powers of 2.</p>
    <ul>
      <li><strong>Left Shift (<code><<</code>):</strong> <code>x << n</code> is equivalent to x &times; 2<sup>n</sup>.
        <br><code>5 << 1</code> &rarr; Binary <code>101</code> becomes <code>1010</code> (<strong>10</strong>).
      </li>
      <li><strong>Right Shift (<code>>></code>):</strong> <code>x >> n</code> is equivalent to x // 2<sup>n</sup>.
        <br><code>20 >> 2</code> &rarr; Binary <code>10100</code> becomes <code>101</code> (<strong>5</strong>).
      </li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Bitwise NOT (<code>~</code>) and Two's Complement</h2>
  <div class="unit">
    <p>The NOT operator is often confusing because it involves <strong>Two's Complement</strong> (how computers store negative numbers).</p>
    <ul>
      <li><strong>Formula:</strong> <code>~x</code> is equal to <code>-(x + 1)</code>.</li>
      <li><strong>Example:</strong> <code>~12</code>
        <ul>
          <li>12 + 1 = 13</li>
          <li>Result: <strong>-13</strong>.</li>
        </ul>
      </li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Practical Use Cases</h2>
  <div class="unit">
    <p>While you might not use these in every script, they are essential for:</p>
    <ol>
      <li><strong>Setting Permissions:</strong> (e.g., Linux file permissions like Read/Write/Execute).</li>
      <li><strong>Compression Algorithms:</strong> Packing multiple boolean flags into a single integer to save memory.</li>
      <li><strong>Graphics and Cryptography:</strong> Manipulating pixel colors or encrypting data at the byte level.</li>
    </ol>
    <blockquote style="border-left: 3px solid var(--secondary); padding-left: 20px; font-style: italic; margin: 20px 0; background: var(--bg-secondary); padding-top: 10px; padding-bottom: 10px;">
      <strong>Tip:</strong> You can use the <code>bin()</code> function in Python to see the binary representation of any number: <code>bin(12)</code> returns <code>'0b1100'</code>.
    </blockquote>
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/precedence-associativity/">← Previous: 3.2 Operator Precedence and Associativity</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/compound-assignment/">Next: 3.4 Compound Assignment Operators →</a>
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
