---
layout: default
title: "5.5 Recursive functions"
course_code: BT101CO
permalink: /syllabus/bt101co/recursive-functions/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>In the logic of problem-solving, <strong>Recursion</strong> is a technique where a function <strong>calls itself</strong> to solve a smaller version of the same problem. It is based on the "divide and conquer" strategy: you break a complex problem into simpler sub-problems until you reach a version that is easy to solve directly.</p>
</div>

<div class="syllabus-section">
  <h2>1. The Two Essential Parts of Recursion</h2>
  <div class="unit">
    <p>Every recursive function <strong>must</strong> have these two components to work correctly:</p>
    <ol>
      <li><strong>Base Case:</strong> The condition under which the function stops calling itself. Without a base case, the function will call itself infinitely, leading to a <code>RecursionError</code> (stack overflow).</li>
      <li><strong>Recursive Step:</strong> The part of the function where it calls itself with a modified (usually smaller) argument, moving closer to the base case.</li>
    </ol>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Classic Example: Factorial</h2>
  <div class="unit">
    <p>The factorial of a number <em>n</em> (written as <em>n!</em>) is defined as n &times; (n-1) &times; (n-2) &times; ... &times; 1.</p>
    <ul>
      <li><strong>Recursive Logic:</strong> n! = n &times; (n-1)!</li>
      <li><strong>Base Case:</strong> 0! or 1! = 1</li>
    </ul>
    <p><strong>Implementation:</strong></p>
    <pre><code class="language-python">def factorial(n):
    if n == 1:             # Base Case
        return 1
    else:
        return n * factorial(n - 1)  # Recursive Step

print(factorial(5)) # Output: 120</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. How Recursion Works (The Call Stack)</h2>
  <div class="unit">
    <p>When a function calls itself, Python doesn't finish the first call immediately. Instead, it "suspends" the current function and starts a new one. These suspended functions are stored in the <strong>Call Stack</strong>.</p>
    <ul>
      <li><strong>Winding Phase:</strong> The functions are added to the stack one by one until the base case is hit.</li>
      <li><strong>Unwinding Phase:</strong> Once the base case returns a value, the stack "unwinds," passing the result back up through each suspended function until the final answer is calculated.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Recursion vs. Iteration (Loops)</h2>
  <div class="unit">
    <table class="exam-table">
      <thead>
        <tr>
          <th>Feature</th>
          <th>Recursion</th>
          <th>Iteration (Loops)</th>
        </tr>
      </thead>
      <tbody>
        <tr><td><strong>Code Style</strong></td><td>Elegant and shorter.</td><td>Longer and more explicit.</td></tr>
        <tr><td><strong>Memory</strong></td><td>Uses more memory (stack).</td><td>Uses less memory.</td></tr>
        <tr><td><strong>Speed</strong></td><td>Can be slower for simple tasks.</td><td>Generally faster.</td></tr>
        <tr><td><strong>Best For</strong></td><td>Trees, sorting, complex math.</td><td>Repetitive tasks, counters.</td></tr>
      </tbody>
    </table>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Tracing Recursive Traces</h2>
  <div class="unit">
    <h3>Example A: Sum of Natural Numbers</h3>
    <pre><code class="language-python">def recursive_sum(n):
    if n == 1:
        return 1
    else:
        return n + recursive_sum(n - 1)</code></pre>
    <p><strong>The Trace (Stack Winding):</strong></p>
    <ol>
      <li><code>recursive_sum(5)</code> &rarr; <code>5 + recursive_sum(4)</code></li>
      <li><code>recursive_sum(4)</code> &rarr; <code>4 + recursive_sum(3)</code></li>
      <li><code>...</code> &rarr; until <code>recursive_sum(1)</code> returns <strong>1</strong> (Base Case Hit!)</li>
    </ol>
    <p><strong>The Unwinding:</strong> 1 &rarr; (2+1) &rarr; (3+3) &rarr; (4+6) &rarr; (5+10) = <strong>15</strong>.</p>
  </div>
</div>

<div class="syllabus-section">
  <h2>6. Practical Exercise Examples</h2>
  <div class="unit">
    <h3>Fibonacci Series</h3>
    <pre><code class="language-python">def fibonacci(n):
    if n <= 1:
        return n 
    else:
        return fibonacci(n - 1) + fibonacci(n - 2)

print(fibonacci(6)) # Output: 8</code></pre>

    <h3>Reversing a String</h3>
    <pre><code class="language-python">def reverse_string(s):
    if len(s) == 0:
        return s
    else:
        return reverse_string(s[1:]) + s[0]

print(reverse_string("PYTHON")) # Output: NOHTYP</code></pre>

    <h3>Greatest Common Divisor (GCD)</h3>
    <pre><code class="language-python">def gcd(a, b):
    if b == 0:
        return a
    else:
        return gcd(b, a % b)

print(gcd(48, 18)) # Output: 6</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>Summary Table: Recursive Mindset</h2>
  <table class="exam-table">
    <thead>
      <tr>
        <th>Problem</th>
        <th>Sample Base Case</th>
        <th>Sample Recursive Step</th>
      </tr>
    </thead>
    <tbody>
      <tr><td><strong>Math Sum</strong></td><td>n = 1</td><td>n + sum(n-1)</td></tr>
      <tr><td><strong>String</strong></td><td>length = 0</td><td>reverse(rem) + first</td></tr>
      <tr><td><strong>Power</strong></td><td>exp = 0</td><td>base * pow(rem)</td></tr>
    </tbody>
  </table>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/variable-scope/">← Previous: 5.4 Local and global scope of a variable</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/lambda-functions/">Next: 5.6 The lambda function →</a>
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
