---
layout: default
title: "1.1 Definitions of Intelligence and AI"
course_code: BT104CO
permalink: /syllabus/bt104co/definitions-intelligence/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <h2>1. What is Intelligence?</h2>
  <div class="unit">
    <p>In the context of AI, intelligence is not defined as a single spark of consciousness, but as a <strong>computational process</strong>.</p>
    
    <h3>The Rational Definition</h3>
    <p>Intelligence is the study of <strong>Rational Agency</strong>. A system is intelligent if it perceives its environment and takes actions that maximize its chances of success, given its goals and the available information.</p>
    
    <div class="formula-box">
      <strong>Key Formula for Intelligence:</strong><br>
      <code>Intelligence = Perception + Reasoning + Action</code>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Defining Artificial Intelligence (AI)</h2>
  <div class="unit">
    <p>Russell and Norvig categorize AI definitions into four historical approaches, organized by whether they focus on <strong>thought processes</strong> vs. <strong>behavior</strong>, and <strong>human-like</strong> performance vs. <strong>rational</strong> performance.</p>

    <div class="ai-approaches">
      <div class="approach-card">
        <h4>A. Thinking Humanly (Cognitive Modeling)</h4>
        <p><strong>Focus:</strong> Internal "mind" and decision-making.<br>
        <strong>Goal:</strong> To build machines that solve problems like humans.<br>
        <strong>Validation:</strong> Requires experimental evidence from psychology/neuroscience.</p>
      </div>
      <div class="approach-card">
        <h4>B. Acting Humanly (Turing Test)</h4>
        <p><strong>Focus:</strong> External behavior and output.<br>
        <strong>Goal:</strong> To perform functions requiring intelligence when done by people.<br>
        <strong>Validation:</strong> The <strong>Turing Test</strong> benchmark.</p>
      </div>
      <div class="approach-card">
        <h4>C. Thinking Rationally (Laws of Thought)</h4>
        <p><strong>Focus:</strong> Formal Logic (Syllogisms).<br>
        <strong>Goal:</strong> To use logical patterns to reach "right" conclusions.<br>
        <strong>Problem:</strong> Hard to turn "fuzzy" real-world knowledge into rigid logic.</p>
      </div>
      <div class="approach-card">
        <h4>D. Acting Rationally (Rational Agent)</h4>
        <p><strong>Focus:</strong> Goal achievement and behavior.<br>
        <strong>Goal:</strong> Operating to achieve the best outcome (or best expected outcome).<br>
        <strong>Modern Standard:</strong> This is the most widely accepted definition in CS.</p>
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. AI vs. Natural Intelligence (NI)</h2>
  <div class="unit">
    <p>While both involve processing information to solve problems, their substrates and characteristics differ significantly.</p>
    <table class="exam-table">
      <thead>
        <tr>
          <th>Feature</th>
          <th>Artificial Intelligence (AI)</th>
          <th>Natural Intelligence (NI)</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>Substrate</strong></td>
          <td>Silicon chips, digital circuits</td>
          <td>Carbon-based, biological neurons</td>
        </tr>
        <tr>
          <td><strong>Speed</strong></td>
          <td>Extremely fast (nanoseconds)</td>
          <td>Relatively slow (milliseconds)</td>
        </tr>
        <tr>
          <td><strong>Learning</strong></td>
          <td>Massive datasets; "copyable"</td>
          <td>Continuous; individual-unique</td>
        </tr>
        <tr>
          <td><strong>Consistency</strong></td>
          <td>High; does not get "tired"</td>
          <td>Subject to emotions and fatigue</td>
        </tr>
        <tr>
          <td><strong>Efficiency</strong></td>
          <td>High consumption (GPU clusters)</td>
          <td>Extremely efficient (~20 Watts)</td>
        </tr>
        <tr>
          <td><strong>Durability</strong></td>
          <td>Permanent (Weights can be stored)</td>
          <td>Perishable (Dies with organism)</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Key Exam Concepts</h2>
  <div class="unit">
    <ul class="key-concepts-list">
      <li><strong>Rationality vs. Omniscience:</strong> AI focuses on Rationality (doing the best with what you know), not Omniscience (knowing everything).</li>
      <li><strong>The Goal of AI:</strong> To find the <strong>optimal</strong> or <strong>satisficing</strong> (sufficient) solution using computational means.</li>
      <li><strong>Turing Test Requirements:</strong> Natural Language Processing, Knowledge Representation, Automated Reasoning, and Machine Learning.</li>
    </ul>
    
    <div class="exam-tip">
      <h4 style="color: #fff; margin-top: 0; margin-bottom: 0.5rem;">Exam Tip</h4>
      Mention the <strong>Rational Agent</strong> approach as the modern standard, while acknowledging the <strong>Turing Test</strong> as the historical benchmark.
    </div>
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <!-- No previous topic for 1.1 -->
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt104co/brief-history-ai/">Next: 1.2 Brief history of AI →</a>
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
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
}
.formula-box code {
  font-size: 1.1rem;
  color: #000;
  font-weight: 600;
}
.ai-approaches {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 1.5rem;
  margin-top: 1.5rem;
}
.approach-card {
  border: 1px solid #e5e7eb;
  padding: 1.5rem;
  border-radius: 12px;
  background: #fff;
  transition: transform 0.2s ease, border-color 0.2s ease;
}
.approach-card:hover {
  transform: translateY(-2px);
  border-color: #000;
}
.approach-card h4 {
  margin-top: 0;
  margin-bottom: 0.75rem;
  font-size: 1rem;
  color: #000;
}
.approach-card p {
  font-size: 0.9rem;
  line-height: 1.5;
  margin: 0;
  color: #4b5563;
}
.key-concepts-list {
  margin-top: 1.5rem;
}
.key-concepts-list li {
  margin-bottom: 1rem;
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
