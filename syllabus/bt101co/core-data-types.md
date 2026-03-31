---
layout: default
title: 2.2 Python Core Data Types
course_code: BT101CO
permalink: /syllabus/bt101co/core-data-types/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>In Python, every value has a data type. Since everything in Python is an object, data types are actually classes and variables are instances (objects) of these classes. Understanding these core types is essential for effective programming.</p>
</div>

<div class="syllabus-section">
  <h2>1. Numeric Types</h2>
  <div class="unit">
    <p>These represent numbers and are the most basic building blocks for mathematical problem-solving.</p>
    <ul>
      <li><strong>Integer (<code>int</code>):</strong> Represents whole numbers (positive, negative, or zero) without a decimal point. <br><em>Example:</em> <code>10</code>, <code>-5</code>, <code>1002</code>.</li>
      <li><strong>Floating Point (<code>float</code>):</strong> Represents real numbers with a decimal point. <br><em>Example:</em> <code>10.5</code>, <code>3.14</code>, <code>-0.001</code>.</li>
      <li><strong>Complex (<code>complex</code>):</strong> Used for scientific calculations, represented as $a + bj$, where $a$ is the real part and $b$ is the imaginary part. <br><em>Example:</em> <code>3 + 4j</code>.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Sequence Types</h2>
  <div class="unit">
    <p>Sequences are ordered collections of items. A critical concept here is the difference between <strong>mutable</strong> (changeable) and <strong>immutable</strong> (unchangeable) sequences.</p>
    <ul>
      <li><strong>String (<code>str</code>):</strong> An immutable sequence of characters enclosed in single (<code>' '</code>), double (<code>" "</code>), or triple (<code>''' '''</code>) quotes.</li>
      <li><strong>List (<code>list</code>):</strong> A <strong>mutable</strong> ordered collection of items (can be of different types). Defined using square brackets <code>[]</code>. <br><em>Example:</em> <code>[1, "Ashok", 3.4]</code>.</li>
      <li><strong>Tuple (<code>tuple</code>):</strong> An <strong>immutable</strong> ordered collection. Once created, its elements cannot be changed. Defined using parentheses <code>()</code>. <br><em>Example:</em> <code>(1, 2, 3)</code>.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Mapping Type (Dictionary)</h2>
  <div class="unit">
    <p><strong>Dictionary (<code>dict</code>):</strong> An unordered collection of key-value pairs. Each key must be unique and is used to retrieve its corresponding value. Defined using curly braces <code>{}</code>.</p>
    <p><em>Example:</em> <code>{"Name": "Ashok", "RollNo": 101}</code>.</p>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Set Types</h2>
  <div class="unit">
    <p><strong>Set (<code>set</code>):</strong> An unordered collection of unique items. Sets are used to eliminate duplicate values and perform mathematical set operations like union and intersection.</p>
    <p><em>Example:</em> <code>{1, 2, 3, 3}</code> becomes <code>{1, 2, 3}</code>.</p>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Boolean Type</h2>
  <div class="unit">
    <p><strong>Boolean (<code>bool</code>):</strong> Represents one of two values: <code>True</code> or <code>False</code>. These are essential for control flow (if-statements and loops). Note that in Python, <code>True</code> is internally treated as <code>1</code> and <code>False</code> as <code>0</code>.</p>
  </div>
</div>

<div class="syllabus-section">
  <h2>6. None Type</h2>
  <div class="unit">
    <p><strong>None:</strong> A special data type that represents the absence of a value or a null value. It is often used to initialize variables that will be assigned a value later.</p>
  </div>
</div>

<div class="syllabus-section">
  <h2>Summary: Mutability vs. Immutability</h2>
  <p>Understanding <strong>mutability</strong> is crucial as it affects how memory is managed and how data is passed between functions:</p>
  
  <table class="exam-table">
    <thead>
      <tr>
        <th>Data Type</th>
        <th>Category</th>
        <th>Mutable?</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><strong>int, float, complex</strong></td>
        <td>Numeric</td>
        <td>No</td>
      </tr>
      <tr>
        <td><strong>str</strong></td>
        <td>Sequence</td>
        <td>No</td>
      </tr>
      <tr>
        <td><strong>tuple</strong></td>
        <td>Sequence</td>
        <td>No</td>
      </tr>
      <tr>
        <td><strong>list</strong></td>
        <td>Sequence</td>
        <td><strong>Yes</strong></td>
      </tr>
      <tr>
        <td><strong>dict</strong></td>
        <td>Mapping</td>
        <td><strong>Yes</strong></td>
      </tr>
      <tr>
        <td><strong>set</strong></td>
        <td>Set</td>
        <td><strong>Yes</strong></td>
      </tr>
    </tbody>
  </table>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/character-set/">← Previous: 2.1 Character Set</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/tokens/">Next: 2.3 Tokens →</a>
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
