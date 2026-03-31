---
layout: default
title: "1.3 Foundations of AI and Related Fields"
course_code: BT104CO
permalink: /syllabus/bt104co/foundations-of-ai/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p class="intro-text" style="font-size: 1.1rem; color: var(--text-muted); margin-bottom: 30px;">
    Artificial Intelligence is not an isolated field. It is a multidisciplinary science that has evolved by drawing theories, tools, and methodologies from several foundational areas of human knowledge.
  </p>

  <div class="foundations-grid">
    <div class="foundation-card">
      <div class="foundation-header">
        <span class="foundation-year">428 B.C. – Present</span>
        <h3>1. Philosophy</h3>
      </div>
      <p>Provided the framework for "thinking about thinking." It explored formal rules for valid conclusions and the "mind-body" problem.</p>
      <ul class="contribution-list">
        <li><strong>Contribution:</strong> Rationalism (logic) and Empiricism.</li>
      </ul>
    </div>

    <div class="foundation-card">
      <div class="foundation-header">
        <span class="foundation-year">c. 800 – Present</span>
        <h3>2. Mathematics</h3>
      </div>
      <p>manipulate logical certainties and uncertain probabilities. Defined what can and cannot be computed (Decidability).</p>
      <ul class="contribution-list">
        <li><strong>Contribution:</strong> Algorithms, complexity theory, and Bayes' Theorem.</li>
      </ul>
    </div>

    <div class="foundation-card">
      <div class="foundation-header">
        <span class="foundation-year">1776 – Present</span>
        <h3>3. Economics</h3>
      </div>
      <p>Focuses on decision-making, Utility Theory (quantifying success), and Game Theory (rational agents in competition).</p>
      <ul class="contribution-list">
        <li><strong>Contribution:</strong> The concept of the <strong>Rational Agent</strong>.</li>
      </ul>
    </div>

    <div class="foundation-card">
      <div class="foundation-header">
        <span class="foundation-year">1861 – Present</span>
        <h3>4. Neuroscience</h3>
      </div>
      <p>The study of the physical substrate of intelligence—the brain and its billions of communicating neurons.</p>
      <ul class="contribution-list">
        <li><strong>Contribution:</strong> Inspiration for <strong>Artificial Neural Networks (ANNs)</strong>.</li>
      </ul>
    </div>

    <div class="foundation-card">
      <div class="foundation-header">
        <span class="foundation-year">1879 – Present</span>
        <h3>5. Psychology</h3>
      </div>
      <p>Investigates how humans perceive, remember, and reason. Views the brain as an information-processing device.</p>
      <ul class="contribution-list">
        <li><strong>Contribution:</strong> Basis for <strong>Cognitive Science</strong> and perception.</li>
      </ul>
    </div>

    <div class="foundation-card">
      <div class="foundation-header">
        <span class="foundation-year">1940 – Present</span>
        <h3>6. Computer Engineering</h3>
      </div>
      <p>Provides the physical hardware (electronic digital computers) needed for complex AI calculations.</p>
      <ul class="contribution-list">
        <li><strong>Contribution:</strong> Moore’s Law and the power for Deep Learning.</li>
      </ul>
    </div>

    <div class="foundation-card">
      <div class="foundation-header">
        <span class="foundation-year">1948 – Present</span>
        <h3>7. Control Theory</h3>
      </div>
      <p>Focuses on self-regulating systems and feedback loops (adjusting state based on goal deviation).</p>
      <ul class="contribution-list">
        <li><strong>Contribution:</strong> Foundation for <strong>Robotics</strong> and autonomous action.</li>
      </ul>
    </div>

    <div class="foundation-card">
      <div class="foundation-header">
        <span class="foundation-year">1957 – Present</span>
        <h3>8. Linguistics</h3>
      </div>
      <p>Understanding communication through grammar and logical structure. Knowledge and language are intertwined.</p>
      <ul class="contribution-list">
        <li><strong>Contribution:</strong> Birth of <strong>Natural Language Processing (NLP)</strong>.</li>
      </ul>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>Exam Prep: Summary of Contributions</h2>
  <div class="unit">
    <table class="exam-table">
      <thead>
        <tr>
          <th>Related Field</th>
          <th>Primary Contribution to AI</th>
        </tr>
      </thead>
      <tbody>
        <tr><td><strong>Philosophy</strong></td><td>Laws of thought, logic, and the "mind-body" problem.</td></tr>
        <tr><td><strong>Mathematics</strong></td><td>Algorithms, formal logic, and probability.</td></tr>
        <tr><td><strong>Economics</strong></td><td>Utility theory, decision-making, and game theory.</td></tr>
        <tr><td><strong>Neuroscience</strong></td><td>The biological model of the brain (neurons).</td></tr>
        <tr><td><strong>Psychology</strong></td><td>Understanding human perception and cognitive modeling.</td></tr>
        <tr><td><strong>Computer Eng.</strong></td><td>The physical hardware (speed/memory) to run AI.</td></tr>
        <tr><td><strong>Control Theory</strong></td><td>Homeostasis, feedback loops, and autonomous action.</td></tr>
        <tr><td><strong>Linguistics</strong></td><td>Syntax, semantics, and Natural Language Processing.</td></tr>
      </tbody>
    </table>
  </div>
</div>

<div class="syllabus-section">
  <div class="exam-tip">
    <h4 style="color: #fff; margin-top: 0; margin-bottom: 0.5rem;">Exam Tip</h4>
    While AI is implemented in Computer Science, it is a <strong>multidisciplinary</strong> field. It draws theories from mathematics, economics, psychology, and more.
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt104co/brief-history-ai/">← Previous: 1.2 Brief history of AI</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt104co/goals-challenges-ai/">Next: 1.4 Goals and Challenges →</a>
    </div>
  </div>
  <div style="text-align: center; margin-top: 30px;">
    <a href="/syllabus/bt104co/" class="back-link">Back to Course Syllabus</a>
  </div>
</div>

<style>
.foundations-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px;
  margin-top: 20px;
}
.foundation-card {
  background: var(--bg-secondary);
  border: 1px solid var(--border-color);
  padding: 20px;
  border-radius: 12px;
  transition: transform 0.2s ease;
}
.foundation-card:hover {
  transform: translateY(-4px);
  border-color: var(--text-main);
}
.foundation-header {
  margin-bottom: 15px;
}
.foundation-year {
  font-size: 0.75rem;
  font-weight: 700;
  color: var(--text-muted);
  text-transform: uppercase;
  letter-spacing: 0.05em;
}
.foundation-card h3 {
  margin: 5px 0 0 0;
  font-size: 1.2rem;
}
.foundation-card p {
  font-size: 0.9rem;
  line-height: 1.5;
  color: var(--text-main);
  margin-bottom: 15px;
}
.contribution-list {
  padding: 0;
  margin: 0;
  list-style: none;
  font-size: 0.85rem;
}
.exam-tip {
  background: #000;
  color: #fff;
  padding: 1.5rem;
  border-radius: 12px;
  margin-top: 2rem;
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
