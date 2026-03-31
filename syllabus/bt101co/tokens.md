---
layout: default
title: 2.3 Python Tokens
course_code: BT101CO
permalink: /syllabus/bt101co/tokens/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>In a Python program, <strong>Tokens</strong> are the smallest individual units that the interpreter recognizes. Just as words and punctuation marks form sentences in English, tokens are the building blocks that form Python statements.</p>
</div>

<div class="syllabus-section">
  <h2>1. Keywords</h2>
  <div class="unit">
    <p>Keywords are reserved words that have a fixed, predefined meaning for the Python interpreter. They cannot be used as names for variables, functions, or any other identifiers.</p>
    <ul>
      <li><strong>Examples:</strong> <code>if</code>, <code>else</code>, <code>while</code>, <code>for</code>, <code>break</code>, <code>import</code>, <code>def</code>, <code>return</code>, <code>True</code>, <code>False</code>.</li>
      <li><strong>Note:</strong> Python keywords are <strong>case-sensitive</strong>.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Identifiers</h2>
  <div class="unit">
    <p>Identifiers are names given to various program elements, such as variables, functions, classes, and objects. The book outlines specific rules for naming identifiers:</p>
    <ul>
      <li>Must begin with a letter (<code>A-Z</code>, <code>a-z</code>) or an underscore (<code>_</code>).</li>
      <li>Can be followed by any number of letters, digits (<code>0-9</code>), or underscores.</li>
      <li>Cannot be a keyword.</li>
      <li>Special symbols (except underscore) like <code>@</code>, <code>$</code>, and <code>%</code> are not allowed.</li>
      <li><strong>Examples:</strong> <code>student_name</code>, <code>total_sum</code>, <code>_temp</code>.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Literals (Values)</h2>
  <div class="unit">
    <p>Literals represent fixed data values in a program. The Kamthanes categorize them by the type of data they hold:</p>
    <ul>
      <li><strong>String Literals:</strong> Text enclosed in quotes (e.g., <code>"Ashok"</code>, <code>'Python'</code>).</li>
      <li><strong>Numeric Literals:</strong> Whole numbers or decimals (e.g., <code>100</code>, <code>3.14</code>).</li>
      <li><strong>Boolean Literals:</strong> <code>True</code> and <code>False</code>.</li>
      <li><strong>Special Literal:</strong> <code>None</code>, used to indicate the absence of a value.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Operators</h2>
  <div class="unit">
    <p>Operators are special symbols used to perform computations on data (operands). The textbook focuses on several categories:</p>
    <ul>
      <li><strong>Arithmetic Operators:</strong> <code>+</code>, <code>-</code>, <code>*</code>, <code>/</code>, <code>%</code> (modulus), <code>**</code> (exponent), <code>//</code> (floor division).</li>
      <li><strong>Relational Operators:</strong> <code>==</code>, <code>!=</code>, <code><</code>, <code>></code>, <code><=</code>, <code>>=</code>.</li>
      <li><strong>Logical Operators:</strong> <code>and</code>, <code>or</code>, <code>not</code>.</li>
      <li><strong>Assignment Operators:</strong> <code>=</code>, <code>+=</code>, <code>-=</code>, etc.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Punctuators (Delimiters)</h2>
  <div class="unit">
    <p>Punctuators are symbols used to organize the code structure and indicate the boundaries of expressions or blocks.</p>
    <ul>
      <li><strong>Common Punctuators:</strong> <code>( )</code>, <code>[ ]</code>, <code>{ }</code>, <code>@</code>, <code>,</code>, <code>:</code>, <code>.</code>, <code>=</code>, <code>;</code>.</li>
      <li>For example, the colon (<code>:</code>) is used at the end of <code>if</code> or <code>for</code> headers to signify the start of an indented block.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>Comparison of Tokens in a Statement</h2>
  <p>To illustrate how these tokens work together, consider this line of code:</p>
  <p><code>if amount > 100 :</code></p>
  
  <table class="exam-table">
    <thead>
      <tr>
        <th>Token</th>
        <th>Type</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><code>if</code></td>
        <td>Keyword</td>
      </tr>
      <tr>
        <td><code>amount</code></td>
        <td>Identifier</td>
      </tr>
      <tr>
        <td><code>></code></td>
        <td>Operator (Relational)</td>
      </tr>
      <tr>
        <td><code>100</code></td>
        <td>Literal (Numeric)</td>
      </tr>
      <tr>
        <td><code>:</code></td>
        <td>Punctuator</td>
      </tr>
    </tbody>
  </table>
  
  <p>By recognizing these tokens, the Python interpreter understands that it needs to check if the value stored in the variable <code>amount</code> is greater than the constant <code>100</code>.</p>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/core-data-types/">← Previous: 2.2 Core Data Types</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/variables/">Next: 2.4 Variables →</a>
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
</style>
