---
layout: default
title: "5.4 Local and global scope of a variable"
course_code: BT101CO
permalink: /syllabus/bt101co/variable-scope/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>In Python, the <strong>Scope</strong> of a variable refers to the specific region of a program where that variable is recognized and can be accessed. A variable's scope is determined by where it is first defined.</p>
</div>

<div class="syllabus-section">
  <h2>1. Local vs. Global Scope</h2>
  <div class="unit">
    <h3>Local Scope</h3>
    <p>A variable defined <strong>inside a function</strong> has a local scope. It is created when the function starts and is destroyed as soon as the function finishes execution.</p>
    <ul>
      <li><strong>Access:</strong> It can only be accessed inside that specific function.</li>
      <li><strong>Isolation:</strong> You can have a local variable with the same name in different functions without interference.</li>
    </ul>

    <h3>Global Scope</h3>
    <p>A variable defined <strong>outside of all functions</strong> (usually at the top of the script) has a global scope.</p>
    <ul>
      <li><strong>Access:</strong> It can be accessed by any function within the same program.</li>
      <li><strong>Lifetime:</strong> It exists as long as the entire program is running.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. The <code>global</code> Keyword</h2>
  <div class="unit">
    <p>By default, you can <strong>read</strong> a global variable inside a function, but you cannot <strong>modify</strong> it. If you try to assign a new value to a global variable name inside a function, Python simply creates a <em>new</em> local variable with that same name.</p>
    <p>To modify a global variable inside a function, you must use the <code>global</code> keyword.</p>
    <pre><code class="language-python">count = 0  # Global

def increment():
    global count  # Tells Python to use the global 'count'
    count += 1

increment()
print(count)  # Output: 1</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Shadowing (Variable Masking)</h2>
  <div class="unit">
    <p>If a local variable and a global variable have the <strong>same name</strong>, the local variable "shadows" or masks the global one within that function's scope.</p>
    <pre><code class="language-python">name = "Global Ashok"

def greet():
    name = "Local Amit"  # Shadowing occurs here
    print(name)

greet()         # Output: Local Amit
print(name)     # Output: Global Ashok</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. The LEGB Rule (Search Hierarchy)</h2>
  <div class="unit">
    <p>The <strong>LEGB Rule</strong> is the specific hierarchy Python uses to search for a variable name. It searches through four distinct layers of scope in a very specific order:</p>
    
    <ol>
      <li><strong>Local (L):</strong> Names assigned within a function.</li>
      <li><strong>Enclosing (E):</strong> Names in the local scope of any enclosing (outer) functions.</li>
      <li><strong>Global (G):</strong> Names assigned at the top-level of a module file.</li>
      <li><strong>Built-in (B):</strong> Names pre-installed in the Python interpreter (e.g., <code>print</code>, <code>len</code>).</li>
    </ol>
    
    <p><strong>Example of LEGB in action:</strong></p>
    <pre><code class="language-python">x = "Global Value"

def outer_func():
    x = "Enclosing Value"
    
    def inner_func():
        x = "Local Value"
        print(x)  # Python finds 'x' in Local (L) and stops.
        
    inner_func()

outer_func() # Output: Local Value</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. The <code>nonlocal</code> Keyword</h2>
  <div class="unit">
    <p>Just as we use <code>global</code> to modify a global variable, we use <code>nonlocal</code> to modify a variable in the <strong>Enclosing</strong> scope of a nested function.</p>
    <pre><code class="language-python">def counter():
    count = 0  # Enclosing scope
    def increment():
        nonlocal count
        count += 1
        return count
    return increment

my_counter = counter()
print(my_counter()) # Output: 1</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>Summary Table: Scope Types</h2>
  <table class="exam-table">
    <thead>
      <tr>
        <th>Scope</th>
        <th>Defined In</th>
        <th>Accessibility</th>
        <th>Search Order</th>
      </tr>
    </thead>
    <tbody>
      <tr><td><strong>Local (L)</strong></td><td>Function body</td><td>Within that function only</td><td>1st</td></tr>
      <tr><td><strong>Enclosing (E)</strong></td><td>Outer function</td><td>Within inner functions</td><td>2nd</td></tr>
      <tr><td><strong>Global (G)</strong></td><td>Module level</td><td>Throughout the program</td><td>3rd</td></tr>
      <tr><td><strong>Built-in (B)</strong></td><td>Python itself</td><td>Available everywhere</td><td>4th</td></tr>
    </tbody>
  </table>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/parameters-arguments/">← Previous: 5.3 Parameters and Arguments</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/recursive-functions/">Next: 5.5 Recursive functions →</a>
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
