---
layout: default
title: "4.2 Loop Control: while loop, for loop"
course_code: BT101CO
permalink: /syllabus/bt101co/loop-control/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>Loop control allows you to execute a block of code repeatedly. This is essential for tasks like processing items in a list, performing repetitive calculations, or running a program until a specific condition changes.</p>
</div>

<div class="syllabus-section">
  <h2>1. The <code>while</code> Loop</h2>
  <div class="unit">
    <p>The <code>while</code> loop is <strong>condition-based</strong>. It repeats as long as a certain boolean condition remains <strong>True</strong>. It is best used when you don't know exactly how many times you need to repeat the task.</p>
    
    <pre><code class="language-python"># Syntax:
while condition:
    # code to repeat
    # update condition</code></pre>

    <div style="background: #fff9db; border-left: 4px solid #fcc419; padding: 15px; margin: 20px 0;">
      <strong>⚠️ The "Infinite Loop" Warning:</strong> If the condition never becomes False, the loop will run forever. You must always include a statement that updates the variables used in the condition.
    </div>

    <p><strong>Solved Example (Counting):</strong></p>
    <pre><code class="language-python">count = 1
while count <= 5:
    print("Iteration:", count)
    count += 1  # Incrementing the counter</code></pre>

    <div style="text-align: center; margin: 30px 0;">
      <pre class="mermaid" style="background: transparent;">
graph TD
    A[Start] --> B{Condition True?}
    B -- Yes --> C[Execute Code Block]
    C --> D[Update Condition]
    D --> B
    B -- No --> E[End]
      </pre>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. The <code>for</code> Loop</h2>
  <div class="unit">
    <p>The <code>for</code> loop is <strong>collection-based</strong>. It is used to iterate over a sequence (like a list, string, or range). It is best used when you know the number of iterations in advance.</p>
    
    <pre><code class="language-python"># Syntax:
for variable in sequence:
    # code to repeat</code></pre>

    <p><strong>Solved Example (String Iteration):</strong></p>
    <pre><code class="language-python">for char in "PYTHON":
    print(char, end="-")
# Output: P-Y-T-H-O-N-</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. The <code>range()</code> Function</h2>
  <div class="unit">
    <p>The <code>for</code> loop is frequently used with the <code>range()</code> function to generate a sequence of numbers.</p>
    <ul>
      <li><code>range(5)</code> &rarr; 0, 1, 2, 3, 4</li>
      <li><code>range(1, 6)</code> &rarr; 1, 2, 3, 4, 5</li>
      <li><code>range(1, 10, 2)</code> &rarr; 1, 3, 5, 7, 9 (starts at 1, ends before 10, steps by 2)</li>
    </ul>

    <p><strong>Solved Example (Sum of first N numbers):</strong></p>
    <pre><code class="language-python">n = 5
total = 0
for i in range(1, n + 1):
    total += i
print(f"The sum of first {n} numbers is {total}")
# Output: The sum of first 5 numbers is 15</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Loop Control Statements</h2>
  <div class="unit">
    <p>Sometimes you need to change the behavior of a loop while it is running. Python provides three keywords for this:</p>
    <ul>
      <li><strong><code>break</code>:</strong> Exits the loop immediately, regardless of the condition.</li>
      <li><strong><code>continue</code>:</strong> Skips the rest of the current iteration and jumps to the next one.</li>
      <li><strong><code>pass</code>:</strong> A "do nothing" placeholder used when a statement is syntactically required but you don't want any command to execute.</li>
    </ul>

    <p><strong>Example of <code>break</code> and <code>continue</code>:</strong></p>
    <pre><code class="language-python">for num in range(1, 10):
    if num == 5:
        break  # Stops the loop entirely when num is 5
    if num % 2 == 0:
        continue  # Skips printing even numbers
    print(num, end=" ")
# Output: 1 3</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Nested Loops & Pattern Solving</h2>
  <div class="unit">
    <p>You can place a loop inside another loop. This is commonly used for working with multi-dimensional data or creating patterns.</p>

    <h3>Example A: Multiplication Table</h3>
    <pre><code class="language-python">for i in range(1, 3):       # Outer loop (rows)
    for j in range(1, 4):   # Inner loop (columns)
        print(f"{i}*{j}={i*j}", end="\t")
    print() # New line after inner loop finishes</code></pre>

    <h3>Example B: Star Patterns (Ladders)</h3>
    <div class="pattern-box">
      <strong>1. Right-Angled Triangle</strong>
      <pre><code class="language-python">for i in range(1, 6):
    for j in range(1, i + 1):
        print("*", end=" ")
    print()</code></pre>
      <pre class="pattern-output">
* 
* * 
* * * 
* * * * 
* * * * *</pre>
    </div>

    <div class="pattern-box">
      <strong>2. Inverted Triangle</strong>
      <pre><code class="language-python">for i in range(5, 0, -1):
    for j in range(1, i + 1):
        print("*", end=" ")
    print()</code></pre>
      <pre class="pattern-output">
* * * * * 
* * * * 
* * * 
* * 
* </pre>
    </div>

    <div class="pattern-box">
      <strong>3. Number-Based Triangle</strong>
      <pre><code class="language-python">for i in range(1, 6):
    for j in range(1, i + 1):
        print(j, end=" ")
    print()</code></pre>
      <pre class="pattern-output">
1 
1 2 
1 2 3 
1 2 3 4 
1 2 3 4 5</pre>
    </div>

    <div class="pattern-box">
      <strong>4. Mirrored Right-Triangle (with Spaces)</strong>
      <pre><code class="language-python">n = 5
for i in range(1, n + 1):
    # Print leading spaces
    for j in range(n - i):
        print(" ", end=" ")
    # Print stars
    for k in range(i):
        print("*", end=" ")
    print()</code></pre>
      <pre class="pattern-output">
        * 
      * * 
    * * * 
  * * * * 
* * * * *</pre>
    </div>

    <div class="pattern-box">
      <strong>5. The Pyramid</strong>
      <pre><code class="language-python">n = 5
for i in range(1, n + 1):
    print(" " * (n - i) + "*" * (2 * i - 1))</code></pre>
      <pre class="pattern-output">
    *
   ***
  *****
 *******
*********</pre>
    </div>

    <div class="pattern-box">
      <strong>6. Hollow Square</strong>
      <pre><code class="language-python">n = 5
for i in range(n):
    for j in range(n):
        if i == 0 or i == n-1 or j == 0 or j == n-1:
            print("*", end=" ")
        else:
            print(" ", end=" ")
    print()</code></pre>
      <pre class="pattern-output">
* * * * * 
*       * 
*       * 
*       * 
* * * * *</pre>
    </div>

    <div class="pattern-box">
      <strong>7. Floyd's Triangle (Number Ladder)</strong>
      <pre><code class="language-python">num = 1
for i in range(1, 6):
    for j in range(1, i + 1):
        print(num, end=" ")
        num += 1
    print()</code></pre>
      <pre class="pattern-output">
1 
2 3 
4 5 6 
7 8 9 10 
11 12 13 14 15</pre>
    </div>
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/decision-making/">← Previous: 4.1 Decision Making</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/">Next: Unit 5 Functions →</a>
    </div>
  </div>
  <div style="text-align: center; margin-top: 30px;">
    <a href="/syllabus/bt101co/" class="back-link">Back to Course Syllabus</a>
  </div>
</div>

<style>
.pattern-box {
  margin: 20px 0;
  padding: 15px;
  background: var(--bg-secondary);
  border-radius: 6px;
}
.pattern-output {
  background: #000;
  color: #fff;
  padding: 10px;
  border-radius: 4px;
  font-family: 'Courier New', Courier, monospace;
  margin-top: 10px;
}
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

<!-- Load Mermaid for Flowcharts -->
<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
<script>mermaid.initialize({startOnLoad:true});</script>
