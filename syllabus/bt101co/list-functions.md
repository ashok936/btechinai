---
layout: default
title: "5.10 Python in-built functions for Lists"
course_code: BT101CO
permalink: /syllabus/bt101co/list-functions/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>To master list manipulation, you must distinguish between <strong>Functions</strong> (which take the list as an input and usually return a new value) and <strong>Methods</strong> (which are called on the list itself and often modify it in-place).</p>
</div>

<div class="syllabus-section">
  <h2>1. Built-in List Functions</h2>
  <div class="unit">
    <p>These functions are standalone and take the list as an argument. They are highly optimized for analyzing data.</p>
    <ul>
      <li><strong><code>len(list)</code></strong>: Returns the total number of elements.</li>
      <li><strong><code>max(list)</code></strong>: Returns the item with the maximum value.</li>
      <li><strong><code>min(list)</code></strong>: Returns the item with the minimum value.</li>
      <li><strong><code>sum(list)</code></strong>: Calculates the total sum of numerical elements.</li>
      <li><strong><code>sorted(list)</code></strong>: Returns a <strong>new</strong> sorted list.</li>
      <li><strong><code>list(reversed(list))</code></strong>: Returns an iterator to access the list backward.</li>
    </ul>
    <p><strong>Example:</strong></p>
    <pre><code class="language-python">scores = [85, 92, 78, 90, 88]
print(len(scores))  # 5
print(max(scores))  # 92
print(sum(scores))  # 433</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Common List Methods</h2>
  <div class="unit">
    <p>Methods use the <code>list.method()</code> syntax. Most of these change the original list in memory (mutability).</p>
    <table class="exam-table">
      <thead>
        <tr>
          <th>Method</th>
          <th>Action</th>
          <th>Resulting List example</th>
        </tr>
      </thead>
      <tbody>
        <tr><td><strong><code>.append(x)</code></strong></td><td>Adds <code>x</code> to the end.</td><td><code>[1, 2, 3]</code></td></tr>
        <tr><td><strong><code>.extend(L)</code></strong></td><td>Appends all items of list <code>L</code>.</td><td>Concatenated list</td></tr>
        <tr><td><strong><code>.insert(i, x)</code></strong></td><td>Inserts <code>x</code> at index <code>i</code>.</td><td>Shifted list</td></tr>
        <tr><td><strong><code>.remove(x)</code></strong></td><td>Deletes the first occurrence of <code>x</code>.</td><td>Value removed</td></tr>
        <tr><td><strong><code>.pop(i)</code></strong></td><td>Removes and <strong>returns</strong> item at <code>i</code>.</td><td>Index removed</td></tr>
        <tr><td><strong><code>.sort()</code></strong></td><td>Sorts the list **in-place**.</td><td>Sorted original</td></tr>
      </tbody>
    </table>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Exam-Oriented Solved Examples</h2>
  <div class="unit">
    <h3>A. Removing Duplicates (The <code>set</code> shortcut)</h3>
    <pre><code class="language-python">nums = [1, 2, 2, 3, 4, 4, 5]
unique_nums = list(set(nums)) # Order might change
# Output: [1, 2, 3, 4, 5]</code></pre>

    <h3>B. Finding Frequency (The <code>count</code> logic)</h3>
    <pre><code class="language-python">words = ["python", "Java", "Python", "C++", "PYTHON"]
target = "python"
count = 0
for w in words:
    if w.lower() == target:
        count += 1
print(f"Occurrences: {count}") # Output: 3</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Critical Exam "Traps"</h2>
  <div class="unit">
    <ul>
      <li><strong>Trap 1: <code>append()</code> vs <code>extend()</code></strong>
        <p><code>L.append([3, 4])</code> &rarr; <code>[1, 2, [3, 4]]</code> (Nested list)<br>
        <code>L.extend([3, 4])</code> &rarr; <code>[1, 2, 3, 4]</code> (Flattened list)</p>
      </li>
      <li><strong>Trap 2: <code>sort()</code> vs <code>sorted()</code></strong>
        <p><code>my_list.sort()</code> returns <strong>None</strong> and modifies the list.<br>
        <code>new_list = sorted(my_list)</code> returns a <strong>New List</strong>.</p>
      </li>
      <li><strong>Trap 3: Assignment vs Copying</strong>
        <p><code>list_b = list_a</code> points to the <strong>same</strong> object.<br>
        <code>list_b = list_a[:]</code> creates a <strong>True Copy</strong>.</p>
      </li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Advanced Logic: Negative Indexing Masterclass</h2>
  <div class="unit">
    <p>Negative indexing starts at <strong><code>-1</code></strong> (the last element). It is essential for accessing data without knowing the list length.</p>
    
    <h3>Negative Indexing in Slicing</h3>
    <p>Example: <code>L = [10, 20, 30, 40, 50, 60]</code></p>
    <table class="exam-table">
      <thead>
        <tr>
          <th>Slice</th>
          <th>Result</th>
          <th>Logic</th>
        </tr>
      </thead>
      <tbody>
        <tr><td><strong><code>L[-3:]</code></strong></td><td><code>[40, 50, 60]</code></td><td>Start at 3rd from end to the end.</td></tr>
        <tr><td><strong><code>L[:-2]</code></strong></td><td><code>[10, 20, 30, 40]</code></td><td>Start at beginning to 2nd from end.</td></tr>
        <tr><td><strong><code>L[-4:-1]</code></strong></td><td><code>[30, 40, 50]</code></td><td>Between 4th from end and last.</td></tr>
      </tbody>
    </table>

    <h3>Exam "Trap" Questions</h3>
    <ul>
      <li><strong>The Out-of-Bounds Trap:</strong> <code>L[-4]</code> on <code>[1, 2, 3]</code> raises an <code>IndexError</code>.</li>
      <li><strong>The Empty Slice Trick:</strong> <code>L[-1:-3]</code> results in <code>[]</code> because the default step is <code>+1</code>. Use <code>L[-1:-3:-1]</code> to fix it.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/list-slicing/">← Previous: 5.9 List Slicing</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/">Next: Back to Syllabus →</a>
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
