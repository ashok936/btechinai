---
layout: default
title: 1.5 Python Documentation
course_code: BT101CO
permalink: /syllabus/bt101co/documentation/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>Python's official documentation is widely considered one of the best in the programming world. It is the ultimate source of truth for everything—from basic syntax to advanced library details.</p>
</div>

<div class="syllabus-section">
  <h2>Importance of Official Docs</h2>
  <p>While many blogs and tutorials exist, the official documentation remains the <strong>single source of truth</strong> for several reasons:</p>
  <div class="unit">
    <ul>
      <li><strong>Always Up-to-Date:</strong> It is maintained by the Python developers themselves, ensuring it reflects the latest features and changes.</li>
      <li><strong>Complete Coverage:</strong> It includes every built-in function, keyword, and module, providing answers for niche cases that tutorials often miss.</li>
      <li><strong>Standard Best Practices:</strong> Documentation often highlights the "Pythonic" way of doing things, guiding you toward efficient and readable code.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>The Official Link</h2>
  <div class="unit">
    <p>You can access the full documentation suite at the official website:</p>
    <a href="https://docs.python.org/3/" target="_blank" class="external-link">docs.python.org/3/</a>
  </div>
</div>

<div class="syllabus-section">
  <h2>What’s Included?</h2>
  <p>The documentation is organized into sections to help you find exactly what you need:</p>
  <div class="unit">
    <ul>
      <li><strong>Tutorial:</strong> A great place for beginners to get a tour of the language.</li>
      <li><strong>Library Reference:</strong> A massive "dictionary" of every built-in function, constant, and module (like <code>math</code>, <code>os</code>, and <code>datetime</code>).</li>
      <li><strong>Language Reference:</strong> A technical deep-dive into Python's syntax and core rules.</li>
      <li><strong>Setup and Usage:</strong> Explains how to configure Python on different platforms.</li>
      <li><strong>FAQs:</strong> Quick answers to the most common questions.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>Tips for Using Documentation</h2>
  <div class="unit">
    <ul>
      <li><strong>Version Selection:</strong> Always ensure you are looking at the documentation for the version you have installed (e.g., 3.11, 3.12, etc.) using the version switcher in the top-left corner.</li>
      <li><strong>The Search bar:</strong> Use it to quickly jump to specific functions like <code>print()</code> or <code>len()</code>.</li>
      <li><strong>The "Quick Search" (offline):</strong> If you are in the REPL, you can type <code>help(object)</code> or <code>help("topic")</code> to see high-level documentation directly in your terminal.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/installing-python/">← Previous: 1.3/1.4 Installation & CLI</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/comparing-python/">Next: 1.6 Comparing Python →</a>
    </div>
  </div>
  <div style="text-align: center; margin-top: 30px;">
    <a href="/syllabus/bt101co/" class="back-link">Back to Course Syllabus</a>
  </div>
</div>

<style>
.external-link {
  display: inline-block;
  font-size: 1.1rem;
  font-weight: 700;
  color: var(--text-main);
  border: 1px solid var(--text-main);
  padding: 10px 20px;
  border-radius: 6px;
  text-decoration: none;
  transition: all 0.2s ease;
}
.external-link:hover {
  background: var(--text-main);
  color: #fff;
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
</style>
