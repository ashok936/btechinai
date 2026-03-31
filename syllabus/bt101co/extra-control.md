---
layout: default
title: "4.3 Control Statements: continue, assert, pass, return"
course_code: BT101CO
permalink: /syllabus/bt101co/extra-control/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>Beyond standard loops and conditions, Python provides specific keywords to control the flow of execution, handle errors, and return data from blocks of code.</p>
</div>

<div class="syllabus-section">
  <h2>1. <code>continue</code> and <code>pass</code></h2>
  <div class="unit">
    <p>These keywords are primarily used inside loops to control iteration behavior.</p>
    <ul>
      <li><strong><code>continue</code>:</strong> Skips the rest of the code in the current iteration and jumps to the next one.</li>
      <li><strong><code>pass</code>:</strong> A placeholder statement that does absolutely nothing. Use it when code is required syntactically (like inside an empty function or loop) but you aren't ready to implement logic.</li>
    </ul>
    <pre><code class="language-python"># Example of pass
def future_function():
    pass  # To be implemented later

# Example of continue
for i in range(5):
    if i == 2:
        continue # Skips printing 2
    print(i, end=" ") # Output: 0 1 3 4</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. The <code>assert</code> Statement</h2>
  <div class="unit">
    <p>The <code>assert</code> keyword is used for debugging. It checks if a condition is <strong>True</strong>. If the condition is False, it raises an <code>AssertionError</code> and stops the program.</p>
    <pre><code class="language-python"># Syntax: assert condition, "Error Message"

age = -5
assert age >= 0, "Age cannot be negative!"
# Since -5 is not >=0, this will crash with an AssertionError</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. The <code>return</code> Statement</h2>
  <div class="unit">
    <p>The <code>return</code> statement is used inside functions to send a value back to the caller. It exits the function immediately.</p>
    <pre><code class="language-python">def add(a, b):
    return a + b

result = add(10, 20)
print(result) # Output: 30</code></pre>
    <p><em>Note: We will explore functions in depth in Unit 5.</em></p>
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/loop-control/">← Previous: 4.2 Loop Control</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/functions-basics/">Next: 5.1 Syntax and basics of a function →</a>
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
