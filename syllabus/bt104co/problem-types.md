---
layout: default
title: "2.6 Types of Problems"
course_code: BT104CO
permalink: /syllabus/bt104co/problem-types/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <h2>1. Categorizing Problems by Environment Knowledge</h2>
  <div class="unit">
    <p>In the framework of Russell and Norvig, the nature of the agent’s knowledge about its environment determines the <strong>type of problem</strong> it must solve. Not all problems are solved by simply searching a map.</p>
    
    <div class="problem-types-grid">
      <!-- 1. Single-State -->
      <div class="problem-card single">
        <div class="problem-icon">①</div>
        <h4>Single-State Problems</h4>
        <p><strong>Status:</strong> Deterministic & Fully Observable.</p>
        <p>The agent knows exactly which state it is in, and every action has a predictable result.</p>
        <div class="problem-example"><strong>Example:</strong> Sudoku or a known maze map.</div>
      </div>

      <!-- 2. Multiple-State -->
      <div class="problem-card multiple">
        <div class="problem-icon">②</div>
        <h4>Multiple-State (Sensorless)</h4>
        <p><strong>Status:</strong> Known & Non-observable.</p>
        <p>Also called <strong>Conformant Problems</strong>. The agent must find a sequence that works for all possible starts.</p>
        <div class="problem-example"><strong>Example:</strong> A "blind" vacuum cleaner.</div>
      </div>

      <!-- 3. Contingency -->
      <div class="problem-card contingency">
        <div class="problem-icon">③</div>
        <h4>Contingency Problems</h4>
        <p><strong>Status:</strong> Nondeterministic / Partially Observable.</p>
        <p>The agent must calculate a <strong>strategy</strong> (tree of actions) rather than a single sequence.</p>
        <div class="problem-example"><strong>Example:</strong> Driving in traffic (interleaved search/execution).</div>
      </div>

      <!-- 4. Exploration -->
      <div class="problem-card exploration">
        <div class="problem-icon">④</div>
        <h4>Exploration Problems</h4>
        <p><strong>Status:</strong> Unknown State Space.</p>
        <p>The agent has no transition model or map. It must experiment and learn while acting.</p>
        <div class="problem-example"><strong>Example:</strong> A robot mapping a new building.</div>
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. The Concept of "Belief States"</h2>
  <div class="unit">
    <div class="belief-state-box">
      <div class="belief-icon">🧠</div>
      <div class="belief-content">
        <h4>Defining Belief States</h4>
        <p>For Multiple-State and Contingency problems, the agent doesn't deal with a single physical state. Instead, it deals with a <strong>Belief State</strong>—the set of all physical states that the agent believes it <em>might</em> be in, based on its history of actions and percepts.</p>
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Problem Type Comparison</h2>
  <div class="unit">
    <table class="exam-table">
      <thead>
        <tr>
          <th>Problem Type</th>
          <th>Knowledge</th>
          <th>Sensor Status</th>
          <th>Solution Type</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>Single-State</strong></td>
          <td>Known / Det.</td>
          <td>Fully Observable</td>
          <td>A sequence of actions</td>
        </tr>
        <tr>
          <td><strong>Multiple-State</strong></td>
          <td>Known / Det.</td>
          <td><b>Sensorless</b></td>
          <td>A sequence for all starts</td>
        </tr>
        <tr>
          <td><strong>Contingency</strong></td>
          <td>Uncertain / Stoch.</td>
          <td>Partially Observable</td>
          <td>A "Tree" or "Policy"</td>
        </tr>
        <tr>
          <td><strong>Exploration</strong></td>
          <td><b>Unknown</b></td>
          <td>Varies</td>
          <td>Learning while acting</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Why This Matters</h2>
  <div class="unit">
    <p>Most "classic" AI algorithms assume a <strong>Single-State Problem</strong>. However, real-world AI (like a robot on Mars) almost always faces <strong>Contingency</strong> or <strong>Exploration</strong> problems, where it must react to the percepts it receives during execution.</p>
  </div>
</div>

<div class="syllabus-section">
  <div class="exam-tip">
    <h4 style="color: #fff; margin-top: 0; margin-bottom: 0.5rem;">Exam Tip</h4>
    If asked about <strong>"Sensorless"</strong> problems, always use the term <strong>Belief State</strong>. It is the specific technical term used to describe how an agent represents uncertainty about its location.
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt104co/state-space-search/">← Previous: 2.5 State Space Search</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt104co/problem-solving-learning/">Next: 2.7 Problem-Solving Agents →</a>
    </div>
  </div>
  <div style="text-align: center; margin-top: 30px;">
    <a href="/syllabus/bt104co/" class="back-link">Back to Course Syllabus</a>
  </div>
</div>

<style>
.problem-types-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px;
  margin-top: 2rem;
}
.problem-card {
  padding: 1.5rem;
  background: #fff;
  border: 1px solid #e1e4e8;
  border-radius: 16px;
  transition: all 0.3s ease;
}
.problem-card:hover {
  transform: translateY(-5px);
  border-color: #000;
  box-shadow: 0 10px 25px -5px rgba(0,0,0,0.05);
}
.problem-icon {
  font-size: 1.25rem;
  font-weight: 800;
  margin-bottom: 10px;
  color: #000;
}
.problem-card h4 {
  margin: 0 0 10px 0;
  font-size: 1.05rem;
}
.problem-card p {
  margin: 0 0 8px 0;
  font-size: 0.85rem;
  color: #4b5563;
  line-height: 1.4;
}
.problem-example {
  margin-top: 12px;
  padding: 8px 12px;
  background: #f9fafb;
  border-radius: 8px;
  font-size: 0.8rem;
  font-style: italic;
  color: #374151;
}

.belief-state-box {
  display: flex;
  gap: 20px;
  padding: 2rem;
  background: #000;
  color: #fff;
  border-radius: 20px;
  margin-top: 2rem;
  align-items: center;
}
.belief-icon { font-size: 2.5rem; }
.belief-content h4 { margin: 0 0 8px 0; color: #60a5fa; }
.belief-content p { margin: 0; font-size: 0.95rem; line-height: 1.5; color: #e5e7eb; }

.exam-table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 1rem;
  font-size: 0.9rem;
}
.exam-table th {
  text-align: left;
  background: #f3f4f6;
  padding: 12px;
  border-bottom: 2px solid #000;
  color: #000;
  text-transform: uppercase;
  font-size: 0.75rem;
  letter-spacing: 0.05em;
}
.exam-table td {
  padding: 12px;
  border-bottom: 1px solid #e5e7eb;
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
