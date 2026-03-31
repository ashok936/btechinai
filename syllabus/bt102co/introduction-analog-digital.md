---
layout: default
title: "1.1 Analog vs Digital Systems"
course_code: BT102CO
permalink: /syllabus/bt102co/introduction-analog-digital/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <h2>1. Introduction</h2>
  <div class="unit">
    <p>A system is a set of elements or components that are organized for a common purpose. In electronics, systems are generally divided into two categories: <strong>Analog</strong> and <strong>Digital</strong>.</p>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Analog vs. Digital</h2>
  <div class="unit">
    <p>An <strong>analog system</strong> uses continuous signals to represent information, while a <strong>digital system</strong> uses discrete values (typically 0 and 1).</p>
    <table class="exam-table">
      <thead>
        <tr>
          <th>Feature</th>
          <th>Analog System</th>
          <th>Digital System</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>Signal Type</strong></td>
          <td>Continuous</td>
          <td>Discrete (Binary)</td>
        </tr>
        <tr>
          <td><strong>Precision</strong></td>
          <td>Affected by noise</td>
          <td>High precision, noise resistant</td>
        </tr>
        <tr>
          <td><strong>Storage</strong></td>
          <td>Difficult to store (tapes)</td>
          <td>Easy to store (HDD, Flash)</td>
        </tr>
        <tr>
          <td><strong>Complexity</strong></td>
          <td>Simpler for small tasks</td>
          <td>Flexible and programmable</td>
        </tr>
        <tr>
          <td><strong>Example</strong></td>
          <td>Mercury Thermometer</td>
          <td>Digital Clock</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Advantages of Digital Systems</h2>
  <div class="unit">
    <ul>
      <li>High speed and high reliability.</li>
      <li>Ease of design and information storage.</li>
      <li>Programmability and flexibility.</li>
      <li>Less affected by noise and environmental changes.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <!-- No previous topic -->
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt102co/number-system-conversion/">Next: 1.2 Number System & Conversion →</a>
    </div>
  </div>
  <div style="text-align: center; margin-top: 30px;">
    <a href="/syllabus/bt102co/" class="back-link">Back to Course Syllabus</a>
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
</style>
