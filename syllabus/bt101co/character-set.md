---
layout: default
title: 2.1 Python Character Set
course_code: BT101CO
permalink: /syllabus/bt101co/character-set/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p>To understand any language, we must first look at the basic building blocks that form it. In Python, the <strong>Character Set</strong> is the collection of valid characters that the interpreter can recognize and process.</p>
</div>

<div class="syllabus-section">
  <h2>The Basic Building Blocks</h2>
  <p>Python's character set consists of letters, digits, and various special symbols. These are categorized as follows:</p>

  <div class="unit">
    <h3>1. Letters</h3>
    <p>Python supports both uppercase and lowercase letters of the English alphabet.</p>
    <ul>
      <li><strong>Uppercase:</strong> <code>A</code> to <code>Z</code></li>
      <li><strong>Lowercase:</strong> <code>a</code> to <code>z</code></li>
    </ul>
    <p><em>Note:</em> Python is <strong>case-sensitive</strong>, meaning <code>Variable</code> and <code>variable</code> are treated as two entirely different entities.</p>
  </div>

  <div class="unit">
    <h3>2. Digits</h3>
    <p>Python recognizes all decimal digits used to form numbers.</p>
    <ul>
      <li><strong>Digits:</strong> <code>0</code> to <code>9</code></li>
    </ul>
  </div>

  <div class="unit">
    <h3>3. Special Symbols</h3>
    <p>These characters have specific functional meanings in Python syntax, such as defining structures, performing math, or assigning values.</p>
    <ul>
      <li><strong>Arithmetic:</strong> <code>+</code>, <code>-</code>, <code>*</code>, <code>/</code>, <code>%</code>, <code>**</code>, <code>//</code></li>
      <li><strong>Assignment/Comparison:</strong> <code>=</code>, <code>==</code>, <code><</code>, <code>></code>, <code>!=</code></li>
      <li><strong>Grouping/Brackets:</strong> <code>( )</code>, <code>[ ]</code>, <code>{ }</code></li>
      <li><strong>Punctuation:</strong> <code>,</code>, <code>:</code>, <code>.</code>, <code>'</code>, <code>"</code>, <code>#</code>, <code>\</code></li>
    </ul>
  </div>

  <div class="unit">
    <h3>4. White Spaces and Other Characters</h3>
    <p>These are often "invisible" but are critical for the structure and readability of the code.</p>
    <ul>
      <li><strong>Blank Space:</strong> Used to separate tokens.</li>
      <li><strong>Tabs:</strong> Used for <strong>indentation</strong> (a core requirement in Python for defining code blocks).</li>
      <li><strong>Newline:</strong> Signals the end of a statement.</li>
      <li><strong>Carriage Return:</strong> Often grouped with newline handling.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>Why the Character Set Matters</h2>
  <div class="unit">
    <p>According to Kamthane and Kamthane, the character set is the <strong>"Basic Building Block"</strong> of the language. From these characters, the programmer forms <strong>Tokens</strong> (Keywords, Identifiers, Literals, etc.).</p>
    
    <p>For example, the character <code>+</code> is part of the character set, but when placed between two numbers, it becomes an <strong>Operator Token</strong>. Similarly, the letters <code>p</code>, <code>r</code>, <code>i</code>, <code>n</code>, <code>t</code> are part of the character set, but when combined, they form a <strong>Keyword/Function Identifier</strong>.</p>
  </div>

  <blockquote style="border-left: 3px solid var(--border-color); padding-left: 20px; color: var(--text-muted); font-style: italic; margin: 20px 0;">
    <strong>Important Concept:</strong> While Python traditionally uses the ASCII character set, modern Python (3.x) is <strong>Unicode-based</strong>, meaning it can technically recognize characters from various world languages, though the Kamthane text focuses on the standard programming set for fundamental problem-solving.
  </blockquote>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/comparing-python/">← Previous: 1.6 Comparing Python</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt101co/core-data-types/">Next: 2.2 Core Data Types →</a>
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
