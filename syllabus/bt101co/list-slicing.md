---
layout: default
title: "5.9 List Slicing"
course_code: BT101CO
permalink: /syllabus/bt101co/list-slicing/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p><strong>List Slicing</strong> is a powerful feature in Python that allows you to extract a specific portion (a "slice") of a list to create a new list. While indexing retrieves a single item, slicing retrieves a <strong>sub-sequence</strong>.</p>
</div>

<div class="syllabus-section">
  <h2>1. The Three Parameters</h2>
  <div class="unit">
    <p>The standard syntax for slicing is: <code>list_name[start : stop : step]</code></p>
    <ul>
      <li><strong><code>start</code></strong>: The index where the slice begins (inclusive). If omitted, it defaults to <strong>0</strong>.</li>
      <li><strong><code>stop</code></strong>: The index where the slice ends (<strong>exclusive</strong>). The element at this index is <strong>not</strong> included. If omitted, it defaults to the end of the list.</li>
      <li><strong><code>step</code></strong>: The increment between each index (optional). If omitted, it defaults to <strong>1</strong>.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Basic Slicing Examples</h2>
  <div class="unit">
    <p>Assume we have the following list: <code>letters = ['A', 'B', 'C', 'D', 'E', 'F']</code></p>
    <table class="exam-table">
      <thead>
        <tr>
          <th>Slice Code</th>
          <th>Result</th>
          <th>Explanation</th>
        </tr>
      </thead>
      <tbody>
        <tr><td><code>letters[1:4]</code></td><td><code>['B', 'C', 'D']</code></td><td>From index 1 to 3 (stops before 4).</td></tr>
        <tr><td><code>letters[:3]</code></td><td><code>['A', 'B', 'C']</code></td><td>From the beginning to index 2.</td></tr>
        <tr><td><code>letters[2:]</code></td><td><code>['C', 'D', 'E', 'F']</code></td><td>From index 2 to the very end.</td></tr>
        <tr><td><code>letters[:]</code></td><td><code>['A', 'B', 'C', 'D', 'E', 'F']</code></td><td>Creates a full copy of the list.</td></tr>
      </tbody>
    </table>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Slicing with a <code>step</code></h2>
  <div class="unit">
    <p>The <code>step</code> value determines how many items to skip.</p>
    <pre><code class="language-python">numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

# Get every second element
print(numbers[::2])   # Output: [0, 2, 4, 6, 8]

# Get elements from index 1 to 7, skipping every other one
print(numbers[1:8:2]) # Output: [1, 3, 5, 7]</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Negative Slicing and Reversing</h2>
  <div class="unit">
    <p>You can use negative numbers for any of the three parameters. This is particularly useful for working from the end of the list or reversing data.</p>
    <ul>
      <li><strong>Last three items:</strong> <code>letters[-3:]</code> &rarr; <code>['D', 'E', 'F']</code></li>
      <li><strong>Reverse the entire list:</strong> <code>letters[::-1]</code> &rarr; <code>['F', 'E', 'D', 'C', 'B', 'A']</code></li>
      <li><strong>Everything except the last two:</strong> <code>letters[:-2]</code> &rarr; <code>['A', 'B', 'C', 'D']</code></li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Modifying Lists via Slicing</h2>
  <div class="unit">
    <p>Because lists are <strong>mutable</strong>, you can actually use slicing on the left side of the assignment operator to replace multiple elements at once.</p>
    <pre><code class="language-python">colors = ["red", "green", "blue", "yellow"]
colors[1:3] = ["pink", "black"]
print(colors) # Output: ['red', 'pink', 'black', 'yellow']</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>Summary Checklist for Slicing</h2>
  <table class="exam-table">
    <thead>
      <tr>
        <th>Goal</th>
        <th>Shortcut</th>
      </tr>
    </thead>
    <tbody>
      <tr><td><strong>First <em>n</em> elements</strong></td><td><code>list[:n]</code></td></tr>
      <tr><td><strong>Last <em>n</em> elements</strong></td><td><code>list[-n:]</code></td></tr>
      <tr><td><strong>Skip every <em>n</em>-th item</strong></td><td><code>list[::n]</code></td></tr>
      <tr><td><strong>Reverse the list</strong></td><td><code>list[::-1]</code></td></tr>
    </tbody>
  </table>
  <p style="margin-top: 20px; font-style: italic;">Slicing is a core skill for data manipulation, allowing for concise and readable code.</p>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/accessing-lists/">← Previous: 5.8 Accessing elements of a List</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/list-functions/">Next: 5.10 Built-in List Functions →</a>
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
