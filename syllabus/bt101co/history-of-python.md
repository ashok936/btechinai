---
layout: default
title: 1.2 History of Python
course_code: BT101CO
permalink: /syllabus/bt101co/history-of-python/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>The history of Python is a story of a "hobby project" that evolved into one of the most dominant forces in modern computing. It was designed to bridge the gap between low-level system languages (like C) and shell scripts, prioritizing human readability above all else.</p>
</div>

<div class="syllabus-section">
  <h2>1. The Origin (Late 1980s)</h2>
  <p>Python was conceived in <strong>December 1989</strong> by <strong>Guido van Rossum</strong> at the Centrum Wiskunde & Informatica (CWI) in the Netherlands.</p>
  <div class="unit">
    <ul>
      <li><strong>The Motivation:</strong> Van Rossum wanted a successor to the <strong>ABC language</strong> (which he had helped develop). ABC was easy to learn but lacked features like exception handling and interfacing with the Amoeba operating system.</li>
      <li><strong>The Name:</strong> Despite the popular snake logo, the name is actually a tribute to the British comedy troupe <strong>Monty Python</strong>. Van Rossum was a fan of <em>"Monty Python's Flying Circus"</em> and wanted a name that was short, unique, and slightly mysterious.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Major Version Milestones</h2>
  <p>The evolution of Python is generally categorized into three major eras:</p>
  
  <div class="unit">
    <h3>Python 1.x (1991–2000): The Foundation</h3>
    <ul>
      <li><strong>0.9.0 (1991):</strong> The first public code release. It already included classes, inheritance, exception handling, and core data types like <code>list</code> and <code>dict</code>.</li>
      <li><strong>1.0 (1994):</strong> Introduced functional programming tools: <code>lambda</code>, <code>map</code>, <code>filter</code>, and <code>reduce</code>.</li>
    </ul>
  </div>

  <div class="unit">
    <h3>Python 2.x (2000–2020): Mass Adoption</h3>
    <ul>
      <li><strong>2.0 (2000):</strong> Introduced <strong>list comprehensions</strong> and a <strong>cycle-detecting garbage collector</strong>. This version shifted the development process to be more community-backed.</li>
      <li><strong>2.7 (2010):</strong> The final release of the 2.x series. It was maintained for an unusually long time (until January 1, 2020) to give developers time to migrate to Python 3.</li>
    </ul>
  </div>

  <div class="unit">
    <h3>Python 3.x (2008–Present): Modern Python</h3>
    <ul>
      <li><strong>3.0 (2008):</strong> Known as <strong>"Py3K"</strong>, this was a fundamental break from the past. It was <strong>not backward compatible</strong> with Python 2. It cleaned up many "warts" in the language:
        <ul>
          <li><code>print</code> became a function: <code>print()</code>.</li>
          <li>Text strings became <strong>Unicode</strong> by default.</li>
          <li>Integer division was refined (e.g., <code>3/2</code> equals <code>1.5</code> instead of <code>1</code>).</li>
        </ul>
      </li>
      <li><strong>3.11–3.13 (2022–2024):</strong> Recent updates have focused heavily on <strong>performance</strong>, making the language significantly faster and improving error messages for better developer experience.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. The Philosophy: The Zen of Python</h2>
  <p>In 1999, developer Tim Peters wrote <strong>"The Zen of Python"</strong> (PEP 20), which summarizes the core philosophy that has guided the language's history. Some of its most famous lines include:</p>
  <blockquote style="border-left: 3px solid var(--border-color); padding-left: 20px; color: var(--text-muted); font-style: italic; margin: 20px 0;">
    "Beautiful is better than ugly.<br>
    Explicit is better than implicit.<br>
    Simple is better than complex.<br>
    Readability counts."
  </blockquote>
</div>

<div class="syllabus-section">
  <h2>4. Current Status</h2>
  <p>Today, Python is maintained by the <strong>Python Software Foundation (PSF)</strong>. Guido van Rossum stepped down as the "Benevolent Dictator For Life" (BDFL) in 2018, and the language is now governed by a five-person <strong>Steering Council</strong>.</p>
  <p>As of 2026, Python remains a top-tier language, particularly dominant in <strong>Artificial Intelligence, Data Science, and Backend Web Development</strong>.</p>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/what-is-python/">← Previous: 1.1 What is Python?</a>
    </div>
    <div class="next-topic">
      <a href="/syllabus/bt101co/installing-python/">Next: 1.3 Downloading and Installing Python →</a>
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
blockquote {
  font-size: 1.1rem;
  line-height: 1.6;
}
</style>
