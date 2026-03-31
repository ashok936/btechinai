---
layout: default
title: "1.2 Brief history of AI, Turing Test"
course_code: BT104CO
permalink: /syllabus/bt104co/brief-history-ai/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <h2>1. The Turing Test (1950)</h2>
  <div class="unit">
    <p>Proposed by <strong>Alan Turing</strong> in his paper <em>"Computing Machinery and Intelligence"</em>, the Turing Test was designed to provide an operational definition of intelligence. Instead of asking "Can machines think?", Turing suggested asking "Can machines behave like humans?".</p>

    <h3>A. The "Imitation Game"</h3>
    <p>A human interrogator communicates via text with two entities: a human and a computer. If the interrogator cannot reliably tell which is which after a series of questions, the computer is said to have passed the test.</p>

    <div class="formula-box">
      <strong style="display: block; margin-bottom: 10px;">Capabilities Required to Pass:</strong>
      <ul class="key-concepts-list">
        <li><strong>Natural Language Processing (NLP):</strong> To communicate successfully in a human language.</li>
        <li><strong>Knowledge Representation:</strong> To store what it knows or hears.</li>
        <li><strong>Automated Reasoning:</strong> To use stored information to answer questions and draw new conclusions.</li>
        <li><strong>Machine Learning:</strong> To adapt to new circumstances and detect patterns.</li>
      </ul>
    </div>
    
    <p><em>Note: The <strong>Total Turing Test</strong> also includes a video link to test perception and the ability to move objects (requiring Computer Vision and Robotics).</em></p>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Brief History of AI: Key Eras</h2>
  <div class="unit">
    <p>The history of AI is often viewed as a cycle of great expectations followed by periods of disappointment known as "AI Winters."</p>

    <div class="timeline-container">
      <div class="timeline-item">
        <div class="timeline-year">1943–1955</div>
        <div class="timeline-content">
          <h4>The Gestation Period</h4>
          <p>McCulloch and Pitts proposed the first model of <strong>artificial neurons</strong> (1943). Turing published the Turing Test paper (1950).</p>
        </div>
      </div>

      <div class="timeline-item">
        <div class="timeline-year">1956</div>
        <div class="timeline-content">
          <h4>The Birth of AI (Dartmouth Workshop)</h4>
          <p>John McCarthy coined the term "Artificial Intelligence". This officially established AI as a distinct field of research.</p>
        </div>
      </div>

      <div class="timeline-item">
        <div class="timeline-year">1952–1969</div>
        <div class="timeline-content">
          <h4>Early Enthusiasm & Great Expectations</h4>
          <p>Computers solving algebra problems and proving theorems. Newell and Simon created the <em>General Problem Solver (GPS)</em>.</p>
        </div>
      </div>

      <div class="timeline-item">
        <div class="timeline-year">1966–1973</div>
        <div class="timeline-content">
          <h4>A Dose of Reality (First AI Winter)</h4>
          <p>Realization that "solving the world" was harder than puzzles. Problems due to <strong>combinatorial explosion</strong> and lack of power.</p>
        </div>
      </div>

      <div class="timeline-item">
        <div class="timeline-year">1969–1988</div>
        <div class="timeline-content">
          <h4>Expert Systems</h4>
          <p>Shift to "domain-specific" AI. <strong>Expert Systems</strong> (like MYCIN) used "If-Then" rules to mimic human experts.</p>
        </div>
      </div>

      <div class="timeline-item">
        <div class="timeline-year">1986–Present</div>
        <div class="timeline-content">
          <h4>Return of Neural Networks</h4>
          <p>Reinvention of <strong>Backpropagation</strong> allowed multi-layer neural networks to learn (Connectionism).</p>
        </div>
      </div>

      <div class="timeline-item">
        <div class="timeline-year">2011–Present</div>
        <div class="timeline-content">
          <h4>The Big Data & Deep Learning Era</h4>
          <p>Massive datasets, powerful GPUs, and Deep Learning breakthrough (ImageNet, LLMs like GPT).</p>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Summary of Historical Transitions</h2>
  <div class="unit">
    <table class="exam-table">
      <thead>
        <tr>
          <th>Era</th>
          <th>Primary Focus</th>
          <th>Methodology</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>Foundational</strong></td>
          <td>Can machines calculate?</td>
          <td>Mathematical Logic / Neurons</td>
        </tr>
        <tr>
          <td><strong>Symbolic AI</strong></td>
          <td>Can machines reason?</td>
          <td>Search / Logic / Symbols</td>
        </tr>
        <tr>
          <td><strong>Knowledge-Based</strong></td>
          <td>What do machines need to know?</td>
          <td>Rules / Expert Systems</td>
        </tr>
        <tr>
          <td><strong>Modern AI</strong></td>
          <td>Can machines learn from data?</td>
          <td>Statistics / Neural Networks</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Key Exam Concepts</h2>
  <div class="unit">
    <div class="exam-tip">
      <h4 style="color: #fff; margin-top: 0; margin-bottom: 0.5rem;">Exam Tip</h4>
      Emphasize that the Turing Test is a test of <strong>behavior</strong>, not <strong>consciousness</strong>. The <strong>Dartmouth Conference (1956)</strong> is considered the official "birthday" of AI.
    </div>
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt104co/definitions-intelligence/">← Previous: 1.1 Definitions of Intelligence</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt104co/foundations-of-ai/">Next: 1.3 Foundations of AI →</a>
    </div>
  </div>
  <div style="text-align: center; margin-top: 30px;">
    <a href="/syllabus/bt104co/" class="back-link">Back to Course Syllabus</a>
  </div>
</div>

<style>
.formula-box {
  background: #f8f9fa;
  padding: 1.5rem;
  border-radius: 12px;
  margin: 1.5rem 0;
  border-left: 5px solid #000;
}
.key-concepts-list {
  padding-left: 1.5rem;
  list-style: square;
}
.key-concepts-list li {
  margin-bottom: 0.5rem;
}
.timeline-container {
  margin-top: 2rem;
  border-left: 2px solid #e5e7eb;
  padding-left: 2rem;
  position: relative;
}
.timeline-item {
  margin-bottom: 2.5rem;
  position: relative;
}
.timeline-item::before {
  content: "";
  position: absolute;
  left: -2.35rem;
  top: 0.25rem;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: #000;
  border: 4px solid #fff;
  box-shadow: 0 0 0 2px #000;
}
.timeline-year {
  font-weight: 800;
  font-size: 0.85rem;
  color: #6b7280;
  text-transform: uppercase;
  margin-bottom: 0.5rem;
}
.timeline-content h4 {
  margin-top: 0;
  margin-bottom: 0.5rem;
  font-size: 1.1rem;
}
.timeline-content p {
  margin: 0;
  font-size: 0.95rem;
  color: #374151;
  line-height: 1.6;
}
.exam-tip {
  background: #000;
  color: #fff;
  padding: 1.5rem;
  border-radius: 12px;
  margin-top: 2rem;
}
.exam-tip strong {
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
