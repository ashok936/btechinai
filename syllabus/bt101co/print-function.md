---
layout: default
title: 2.7 The print() Function
course_code: BT101CO
permalink: /syllabus/bt101co/print-function/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>The <code>print()</code> function is the primary way to output data to the standard output device (usually the screen). In Python, it is a versatile tool that can display text, numbers, variables, and the results of expressions.</p>
</div>

<div class="syllabus-section">
  <h2>1. Basic Syntax</h2>
  <div class="unit">
    <p>The simplest form of the <code>print()</code> function is:</p>
    <p><code>print(value1, value2, ..., sep=' ', end='\n')</code></p>
    <ul>
      <li><strong>Values:</strong> You can pass one or multiple items (strings, integers, etc.) separated by commas.</li>
      <li><strong>Comma Separation:</strong> When you use a comma to separate multiple items, Python automatically adds a <strong>space</strong> between them.</li>
    </ul>
    <p><strong>Example:</strong></p>
    <pre><code class="language-python">name = "Ashok"
age = 25
print("Name:", name, "Age:", age)
# Output: Name: Ashok Age: 25</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Standard Arguments: sep and end</h2>
  <div class="unit">
    <p>Python provides two special "keyword arguments" that allow you to control how the output is formatted.</p>
    
    <h4>The <strong>sep</strong> (Separator) Argument</h4>
    <p>By default, <code>sep</code> is a space (<code>' '</code>). You can change it to any string, such as a hyphen, a slash, or even a newline.</p>
    <ul>
      <li><code>print("12", "05", "2026", sep="-")</code> $\rightarrow$ <strong>12-05-2026</strong></li>
    </ul>

    <h4>The <strong>end</strong> Argument</h4>
    <p>By default, <code>print()</code> adds a newline (<code>\n</code>) at the end of the output, meaning the next <code>print()</code> statement will start on a new line. You can change this to stay on the same line.</p>
    <ul>
      <li><code>print("Hello", end=" ")</code></li>
      <li><code>print("World")</code> $\rightarrow$ <strong>Hello World</strong> (on one line)</li>
    </ul>

    <p><strong>Example: Custom Layouts</strong></p>
    <pre><code class="language-python"># Using 'sep' to create a date format
print("Date", "03", "31", "2026", sep="/") 
# Output: Date/03/31/2026

# Using 'end' to keep output on the same line (like a loading bar)
print("Loading", end="...")
print(" [||||||||||]", end=" ")
print("100% Complete")
# Output: Loading... [||||||||||] 100% Complete</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Printing Expressions</h2>
  <div class="unit">
    <p>You don't just have to print variables; you can perform calculations or logic directly inside the parentheses.</p>
    <ul>
      <li><code>print("Result:", 10 * 5 + 2)</code> $\rightarrow$ <strong>Result: 52</strong></li>
      <li><code>print("Is 10 > 5?", 10 > 5)</code> $\rightarrow$ <strong>Is 10 > 5? True</strong></li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Formatted Output (f-strings)</h2>
  <div class="unit">
    <p>While there are older ways to format strings (like <code>%</code> or <code>.format()</code>), modern Python uses <strong>f-strings</strong> (formatted string literals). They are highly readable and efficient.</p>
    <p><strong>Example:</strong></p>
    <pre><code class="language-python">price = 49.99
print(f"The total cost is ${price}")
# Output: The total cost is $49.99</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Escape Sequences</h2>
  <div class="unit">
    <p>To print special characters that are otherwise hard to type (like a tab or a quote), you use a backslash (<code>\</code>) followed by a specific character.</p>
    
    <table class="exam-table">
      <thead>
        <tr>
          <th>Escape Sequence</th>
          <th>Result</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><code>\n</code></td>
          <td>Newline (starts a new line)</td>
        </tr>
        <tr>
          <td><code>\t</code></td>
          <td>Horizontal Tab (adds space)</td>
        </tr>
        <tr>
          <td><code>\'</code></td>
          <td>Single Quote</td>
        </tr>
        <tr>
          <td><code>\"</code></td>
          <td>Double Quote</td>
        </tr>
        <tr>
          <td><code>\\</code></td>
          <td>Backslash</td>
        </tr>
      </tbody>
    </table>
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
        <td><strong>Purpose</strong></td>
        <td>To display output on the screen.</td>
      </tr>
      <tr>
        <td><strong>Multiple Items</strong></td>
        <td>Separated by commas; adds a space by default.</td>
      </tr>
      <tr>
        <td><strong>Default End</strong></td>
        <td>Automatically moves to a new line (<code>\n</code>).</td>
      </tr>
      <tr>
        <td><strong>Flexibility</strong></td>
        <td>Can print literals, variables, and expressions.</td>
      </tr>
    </tbody>
  </table>
  
  <p>The <code>print()</code> function is the "voice" of your program, allowing it to communicate results, status updates, and errors to the user.</p>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/input-function/">← Previous: 2.6 The input() Function</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/eval-function/">Next: 2.8 The eval() Function →</a>
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
