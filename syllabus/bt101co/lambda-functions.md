---
layout: default
title: "5.6 The lambda function"
course_code: BT101CO
permalink: /syllabus/bt101co/lambda-functions/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>In Python, a <strong>Lambda Function</strong> is a small, anonymous function that is defined without a name using the <code>lambda</code> keyword. Unlike standard functions defined with <code>def</code>, lambdas are restricted to a <strong>single expression</strong>.</p>
</div>

<div class="syllabus-section">
  <h2>1. Syntax of a Lambda Function</h2>
  <div class="unit">
    <p>The structure of a lambda function is very concise:</p>
    <p><code>lambda arguments : expression</code></p>
    <ul>
      <li><strong><code>lambda</code></strong>: The keyword that initiates the function.</li>
      <li><strong>Arguments</strong>: One or more inputs (separated by commas).</li>
      <li><strong>Colon (<code>:</code>)</strong>: Separates the arguments from the logic.</li>
      <li><strong>Expression</strong>: The single line of code that is executed and <strong>automatically returned</strong>.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Basic Example: Standard vs. Lambda</h2>
  <div class="unit">
    <p>Let's compare a standard function with a lambda function that calculates the square of a number.</p>
    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px;">
      <div>
        <strong>Standard Way:</strong>
        <pre><code class="language-python">def square(x):
    return x * x

print(square(5)) # 25</code></pre>
      </div>
      <div>
        <strong>Lambda Way:</strong>
        <pre><code class="language-python">square_lambda = lambda x: x * x

print(square_lambda(5)) # 25</code></pre>
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Key Characteristics</h2>
  <div class="unit">
    <ul>
      <li><strong>Anonymous:</strong> They don't have a name unless you assign them to a variable.</li>
      <li><strong>Single Expression:</strong> You cannot have multiple lines, loops, or complex <code>if-else</code> blocks.</li>
      <li><strong>Implicit Return:</strong> You don't type the word <code>return</code>; the result of the expression is returned by default.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Advanced "Problem Solving" Uses</h2>
  <div class="unit">
    <p>The true power of lambda functions is revealed when they are used as arguments inside higher-order functions.</p>

    <h3>A. Using with <code>filter()</code></h3>
    <p><code>filter()</code> keeps only items where the function returns <strong>True</strong>.</p>
    <pre><code class="language-python">nums = [1, 2, 3, 4, 5, 6]
# Keep only even numbers
evens = list(filter(lambda x: x % 2 == 0, nums))
print(evens) # Output: [2, 4, 6]</code></pre>

    <h3>B. Using with <code>map()</code></h3>
    <p><code>map()</code> applies the function to every item in a list.</p>
    <pre><code class="language-python">nums = [1, 2, 3, 4]
# Double every number
doubled = list(map(lambda x: x * 2, nums))
print(doubled) # Output: [2, 4, 6, 8]</code></pre>

    <h3>C. Using with <code>sorted()</code></h3>
    <p>You can use a lambda as a "key" to sort complex data structures (like tuples).</p>
    <pre><code class="language-python">students = [("Ashok", 85), ("Amit", 92), ("Suman", 78)]
# Sort by grade (the second element in the tuple)
students.sort(key=lambda x: x[1])
print(students) # Output: [('Suman', 78), ('Ashok', 85), ('Amit', 92)]</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>Summary Table</h2>
  <table class="exam-table">
    <thead>
      <tr>
        <th>Feature</th>
        <th><code>def</code> Function</th>
        <th><code>lambda</code> Function</th>
      </tr>
    </thead>
    <tbody>
      <tr><td><strong>Keyword</strong></td><td><code>def</code></td><td><code>lambda</code></td></tr>
      <tr><td><strong>Name</strong></td><td>Required</td><td>Anonymous</td></tr>
      <tr><td><strong>Body</strong></td><td>Multiple lines allowed</td><td>Single expression only</td></tr>
      <tr><td><strong>Return</strong></td><td>Explicit <code>return</code></td><td>Implicit return</td></tr>
    </tbody>
  </table>
  <p style="margin-top: 20px; font-style: italic;">Lambda functions are like disposable tools—great for quick tasks inside other functions, but not intended for building entire systems.</p>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/recursive-functions/">← Previous: 5.5 Recursive functions</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/creating-lists/">Next: 5.7 Creating Lists →</a>
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
