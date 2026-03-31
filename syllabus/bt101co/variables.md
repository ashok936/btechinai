---
layout: default
title: 2.4 Python Variables
course_code: BT101CO
permalink: /syllabus/bt101co/variables/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>Variables are named locations in a computer's memory used to store data that can be manipulated during program execution. Think of a variable as a <strong>label</strong> or a <strong>reference</strong> attached to a specific value.</p>
</div>

<div class="syllabus-section">
  <h2>1. The Core Concept: Labels, Not Boxes</h2>
  <div class="unit">
    <p>In many older languages, a variable is like a "box" where you drop a value. In Python, it is more accurate to view a variable as a <strong>tag</strong> or <strong>pointer</strong> tied to an object in memory.</p>
    <ul>
      <li>When you write <code>x = 10</code>, an object <code>10</code> is created in memory, and the label <code>x</code> is pointed at it.</li>
      <li>If you then write <code>y = x</code>, you aren't creating a second "10"; you are simply attaching a second label (<code>y</code>) to the same memory location.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Rules for Naming (Identifiers)</h2>
  <div class="unit">
    <p>To ensure the interpreter recognizes a variable, it must follow these strict syntax rules:</p>
    <ul>
      <li><strong>Start with</strong> a letter (<code>A-Z</code>, <code>a-z</code>) or an underscore (<code>_</code>).</li>
      <li><strong>No Digits at the start:</strong> <code>1variable</code> is invalid; <code>variable1</code> is fine.</li>
      <li><strong>Case-Sensitivity:</strong> <code>Age</code>, <code>age</code>, and <code>AGE</code> are three completely different variables.</li>
      <li><strong>No Keywords:</strong> Reserved words like <code>if</code>, <code>while</code>, or <code>class</code> cannot be used as names.</li>
      <li><strong>No Special Characters:</strong> Symbols like <code>@</code>, <code>$</code>, and <code>%</code> are prohibited (except for the underscore).</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Dynamic Typing</h2>
  <div class="unit">
    <p>Python uses <strong>Dynamic Typing</strong>, meaning you don't have to tell the computer what kind of data a variable will hold (like <code>int</code> or <code>string</code>) beforehand. The type is automatically determined by the value assigned to it:</p>
    <ul>
      <li><code>score = 100</code> $\rightarrow$ The variable is an <strong>Integer</strong>.</li>
      <li><code>score = "High"</code> $\rightarrow$ The same variable now points to a <strong>String</strong>.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Assignment Methods</h2>
  <div class="unit">
    <p>Values are assigned using the <code>=</code> operator (the assignment operator).</p>
    <ul>
      <li><strong>Single Assignment:</strong> <code>price = 99.99</code></li>
      <li><strong>Multiple Assignment (Same Value):</strong> <code>a = b = c = 0</code> (All three point to zero).</li>
      <li><strong>Multiple Assignment (Different Values):</strong> <code>name, age = "Ashok", 25</code> (Assigns "Ashok" to <code>name</code> and <code>25</code> to <code>age</code> simultaneously).</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Scope: Where the Variable Lives</h2>
  <div class="unit">
    <p>A variable's "Scope" determines where in the code it can be accessed:</p>
    <ul>
      <li><strong>Local Variables:</strong> Defined inside a function; they only exist while that function is running.</li>
      <li><strong>Global Variables:</strong> Defined outside functions; they are accessible throughout the entire script.</li>
    </ul>
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
        <td><strong>Declaration</strong></td>
        <td>Not required (created at the moment of assignment).</td>
      </tr>
      <tr>
        <td><strong>Typing</strong></td>
        <td>Dynamic (type changes based on the value).</td>
      </tr>
      <tr>
        <td><strong>Memory</strong></td>
        <td>Acts as a reference/pointer to an object.</td>
      </tr>
      <tr>
        <td><strong>Naming</strong></td>
        <td>Must start with a letter/underscore; case-sensitive.</td>
      </tr>
    </tbody>
  </table>
  
  <p>By mastering variables, you gain the ability to store, track, and change information—the fundamental requirement for any problem-solving logic.</p>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/tokens/">← Previous: 2.3 Tokens</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/assignment-of-values/">Next: 2.5 Assignment of Values →</a>
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
