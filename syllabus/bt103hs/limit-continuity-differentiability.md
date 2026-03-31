---
layout: default
title: "1.1 Limit, Continuity and Differentiability"
course_code: BT103HS
permalink: /syllabus/bt103hs/limit-continuity-differentiability/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <h2>1. General Concept of Limit</h2>
  <div class="unit">
    <p>A limit is the value that a function "approaches" as the input approaches some value. Limits are essential to calculus and are used to define continuity, derivatives, and integrals.</p>
    <p>We write: <code>lim<sub>x&rarr;a</sub> f(x) = L</code></p>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Continuity</h2>
  <div class="unit">
    <p>A function <code>f(x)</code> is continuous at a point <code>x = a</code> if the following three conditions are met:</p>
    <ol>
      <li><code>f(a)</code> is defined.</li>
      <li><code>lim<sub>x&rarr;a</sub> f(x)</code> exists.</li>
      <li><code>lim<sub>x&rarr;a</sub> f(x) = f(a)</code>.</li>
    </ol>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Differentiability</h2>
  <div class="unit">
    <p>A function is differentiable at <code>x = a</code> if its derivative exists at that point. Geometrically, this means the graph of the function has a non-vertical tangent line at <code>(a, f(a))</code>.</p>
    <p>All differentiable functions are continuous, but not all continuous functions are differentiable (e.g., <code>f(x) = |x|</code> at <code>x = 0</code>).</p>
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <!-- No previous topic -->
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt103hs/tangent-normal/">Next: 1.2 Tangent and Normal →</a>
    </div>
  </div>
  <div style="text-align: center; margin-top: 30px;">
    <a href="/syllabus/bt103hs/" class="back-link">Back to Course Syllabus</a>
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
