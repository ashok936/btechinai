---
layout: default
title: "5.8 Accessing the elements of a List"
course_code: BT101CO
permalink: /syllabus/bt101co/accessing-lists/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>Accessing elements in a list is done through <strong>Indexing</strong>. In Python, every item in a list has a specific position, and Python allows you to count these positions from both the beginning and the end of the list.</p>
</div>

<div class="syllabus-section">
  <h2>1. Positive Indexing (Starting from 0)</h2>
  <div class="unit">
    <p>Python uses zero-based indexing. The first element is at index <code>0</code>, the second at index <code>1</code>, and so on.</p>
    <p><strong>Syntax:</strong> <code>list_name[index]</code></p>
    <pre><code class="language-python">fruits = ["Apple", "Banana", "Cherry", "Date"]
print(fruits[0])  # Output: Apple
print(fruits[2])  # Output: Cherry</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Negative Indexing (Starting from -1)</h2>
  <div class="unit">
    <p>Negative indexing allows you to access items from the end of the list without knowing its total length. <code>-1</code> refers to the <strong>last</strong> item, and <code>-2</code> refers to the second-to-last item.</p>
    <pre><code class="language-python">fruits = ["Apple", "Banana", "Cherry", "Date"]
print(fruits[-1]) # Output: Date
print(fruits[-3]) # Output: Banana</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Accessing Nested Lists</h2>
  <div class="unit">
    <p>If a list contains another list (a nested list), you use multiple square brackets to "drill down" into the data.</p>
    <pre><code class="language-python">matrix = [[1, 2], [3, 4], [5, 6]]

# Access the second list [3, 4]
sub_list = matrix[1]     # Output: [3, 4]

# Access the number '4' inside that list
number = matrix[1][1]    # Output: 4</code></pre>
  </div>
</div>

<div class="syllabus-section">
  <h2>The "IndexError"</h2>
  <div class="unit">
    <p>If you try to access an index that doesn't exist (e.g., <code>fruits[10]</code> when the list only has 4 items), Python will raise an <strong><code>IndexError: list index out of range</code></strong>. Always ensure your index is less than the <code>len(list_name)</code>.</p>
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/creating-lists/">← Previous: 5.7 Creating Lists</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/list-slicing/">Next: 5.9 List Slicing →</a>
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
