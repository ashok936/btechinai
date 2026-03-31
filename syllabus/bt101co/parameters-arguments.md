---
layout: default
title: "5.3 Parameters and Arguments in a function"
course_code: BT101CO
permalink: /syllabus/bt101co/parameters-arguments/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>In Python, <strong>Parameters</strong> and <strong>Arguments</strong> are the mechanisms used to pass data into a function. While these terms are often used interchangeably, they represent two different stages of a function's life cycle.</p>
</div>

<div class="syllabus-section">
  <h2>1. Parameters vs. Arguments</h2>
  <div class="unit">
    <ul>
      <li><strong>Parameters:</strong> These are the variables listed in the function's <strong>definition</strong>. They act as placeholders for the data the function expects to receive.</li>
      <li><strong>Arguments:</strong> These are the actual values passed to the function when it is <strong>called</strong>.</li>
    </ul>
    <p><strong>Example:</strong></p>
    <pre><code class="language-python">def greet(name):      # 'name' is a parameter
    print(f"Hello, {name}!")

greet("Ashok")        # "Ashok" is an argument</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Types of Arguments</h2>
  <div class="unit">
    <p>Python provides several flexible ways to pass arguments into a function:</p>
    
    <h3>A. Positional Arguments</h3>
    <p>The most common type. Arguments are assigned to parameters based on their <strong>order</strong> (position).</p>
    <pre><code class="language-python">def display_info(name, age):
    print(f"Name: {name}, Age: {age}")

display_info("Amit", 25) # "Amit" goes to name, 25 goes to age</code></pre>

    <h3>B. Keyword Arguments</h3>
    <p>You can specify the parameter name during the function call. This allows you to ignore the order of arguments, making the code more readable.</p>
    <pre><code class="language-python">display_info(age=30, name="Suman") # Order doesn't matter here</code></pre>

    <h3>C. Default Arguments</h3>
    <p>You can provide a default value to a parameter in the function definition. If the caller doesn't provide an argument, the default value is used.</p>
    <pre><code class="language-python">def greet(name, message="Welcome"):
    print(f"{message}, {name}!")

greet("Ashok")            # Output: Welcome, Ashok!
greet("Ashok", "Hi")      # Output: Hi, Ashok!</code></pre>
    <div style="background: #fff9db; border-left: 4px solid #fcc419; padding: 10px; margin: 10px 0;">
      <strong>Note:</strong> Default parameters must always follow non-default parameters.
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Variable-Length Arguments (*args and **kwargs)</h2>
  <div class="unit">
    <p>Sometimes you don't know in advance how many arguments will be passed. These are handled using the <code>*</code> (asterisk) and <code>**</code> (double asterisk) symbols.</p>

    <h3>A. *args (Non-Keyword)</h3>
    <p>Allows a function to accept any number of <strong>positional</strong> arguments. Inside the function, these are stored in a <strong>Tuple</strong>.</p>
    <pre><code class="language-python">def sum_all(*numbers):
    total = 0
    for num in numbers:
        total += num
    return total

print(sum_all(10, 20))         # Output: 30
print(sum_all(1, 2, 3, 4, 5))  # Output: 15</code></pre>

    <h3>B. **kwargs (Keyword)</h3>
    <p>Allows a function to accept any number of <strong>keyword</strong> (named) arguments. Inside the function, these are stored in a <strong>Dictionary</strong>.</p>
    <pre><code class="language-python">def show_profile(**details):
    for key, value in details.items():
        print(f"{key}: {value}")

show_profile(Name="Ashok", Age=25, City="Lalitpur")</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Pass by Object Reference</h2>
  <div class="unit">
    <p>Python uses <strong>Pass by Object Reference</strong> to handle data internally:</p>
    <ol>
      <li><strong>Mutable Objects (e.g., List, Dict):</strong> If you modify it inside the function, the change <strong>will</strong> reflect outside the function.</li>
      <li><strong>Immutable Objects (e.g., Integer, String):</strong> The function cannot change the original value; it creates a local copy if modified.</li>
    </ol>
    <p><strong>Example with a List (Mutable):</strong></p>
    <pre><code class="language-python">def add_item(my_list):
    my_list.append(4)

nums = [1, 2, 3]
add_item(nums)
print(nums) # Output: [1, 2, 3, 4]</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Unpacking Operators (* and **)</h2>
  <div class="unit">
    <p>You can use these symbols in reverse to "unpack" a collection into a function call.</p>
    <ul>
      <li><strong>Unpacking a List/Tuple:</strong> Use <code>*</code> to spread elements into positional arguments.</li>
      <li><strong>Unpacking a Dictionary:</strong> Use <code>**</code> to spread key-value pairs into keyword arguments.</li>
    </ul>
    <pre><code class="language-python">def add(a, b, c):
    return a + b + c

nums = [1, 2, 3]
print(add(*nums)) # Equivalent to add(1, 2, 3)</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>Summary Checklist</h2>
  <table class="exam-table">
    <thead>
      <tr>
        <th>Type</th>
        <th>Data Structure</th>
        <th>When to Use?</th>
      </tr>
    </thead>
    <tbody>
      <tr><td><strong>Positional</strong></td><td>Order-based</td><td>For simple, few-parameter functions.</td></tr>
      <tr><td><strong>Keyword</strong></td><td>Name-based</td><td>For functions with many parameters.</td></tr>
      <tr><td><strong>Default</strong></td><td>Pre-set values</td><td>For optional settings.</td></tr>
      <tr><td><strong><code>*args</code></strong></td><td>**Tuple**</td><td>When handling unknown number of items.</td></tr>
      <tr><td><strong><code>**kwargs</code></strong></td><td>**Dictionary**</td><td>When handling unknown named settings.</td></tr>
    </tbody>
  </table>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/use-of-functions/">← Previous: 5.2 Use of a function</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/variable-scope/">Next: 5.4 Scope of a variable →</a>
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
