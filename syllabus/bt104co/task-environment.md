---
layout: default
title: "2.3 The Properties of Task Environments"
course_code: BT104CO
permalink: /syllabus/bt104co/task-environment/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <h2>1. Understanding the Task Environment</h2>
  <div class="unit">
    <p>In the framework of Russell and Norvig, the design of an agent is strictly dictated by the <strong>Task Environment</strong>. To design a rational agent, we must first categorize the environment using six key dimensions.</p>
    
    <div class="dimensions-grid">
      <!-- 1. Observability -->
      <div class="dimension-card">
        <div class="dim-num">01</div>
        <h4>Fully vs. Partially Observable</h4>
        <p><strong>Fully:</strong> Sensors detect all relevant aspects (e.g., Chess).</p>
        <p><strong>Partially:</strong> Missing info due to noise or limited range (e.g., Poker).</p>
      </div>

      <!-- 2. Agents -->
      <div class="dimension-card">
        <div class="dim-num">02</div>
        <h4>Single Agent vs. Multiagent</h4>
        <p><strong>Single:</strong> Acting alone (e.g., Crossword).</p>
        <p><strong>Multiagent:</strong> Other agents are present. Can be <em>Competitive</em> (Chess) or <em>Cooperative</em> (Traffic).</p>
      </div>

      <!-- 3. Determinism -->
      <div class="dimension-card">
        <div class="dim-num">03</div>
        <h4>Deterministic vs. Stochastic</h4>
        <p><strong>Deterministic:</strong> Next state is completely certain (e.g., Sudoku).</p>
        <p><strong>Stochastic:</strong> Uncertainty or randomness involved (e.g., Taxi driving).</p>
        <div class="note-box"><strong>Strategic:</strong> Deterministic except for other agents.</div>
      </div>

      <!-- 4. Episodes -->
      <div class="dimension-card">
        <div class="dim-num">04</div>
        <h4>Episodic vs. Sequential</h4>
        <p><strong>Episodic:</strong> Actions are independent "episodes" (e.g., Image Analysis).</p>
        <p><strong>Sequential:</strong> Decisions have long-term consequences (e.g., Driving).</p>
      </div>

      <!-- 5. Dynamics -->
      <div class="dimension-card">
        <div class="dim-num">05</div>
        <h4>Static vs. Dynamic</h4>
        <p><strong>Static:</strong> World doesn't change while thinking (e.g., Crossword).</p>
        <p><strong>Dynamic:</strong> World keeps moving during deliberation (e.g., Taxi).</p>
        <div class="note-box"><strong>Semidynamic:</strong> Only performance score changes (e.g., Timed Chess).</div>
      </div>

      <!-- 6. Continuity -->
      <div class="dimension-card">
        <div class="dim-num">06</div>
        <h4>Discrete vs. Continuous</h4>
        <p><strong>Discrete:</strong> Limited, distinct number of states (e.g., Chess).</p>
        <p><strong>Continuous:</strong> Smoothly varying speed, angles, coords (e.g., Self-driving cars).</p>
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Summary Table of Task Environments</h2>
  <div class="unit">
    <table class="exam-table">
      <thead>
        <tr>
          <th>Environment</th>
          <th>Observable</th>
          <th>Agents</th>
          <th>Deterministic</th>
          <th>Episodic</th>
          <th>Static</th>
          <th>Discrete</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>Chess</strong></td>
          <td>Fully</td>
          <td>Multi</td>
          <td>Strategic</td>
          <td>Sequential</td>
          <td>Static</td>
          <td>Discrete</td>
        </tr>
        <tr>
          <td><strong>Taxi Driving</strong></td>
          <td>Partial</td>
          <td>Multi</td>
          <td>Stochastic</td>
          <td>Sequential</td>
          <td>Dynamic</td>
          <td>Continuous</td>
        </tr>
        <tr>
          <td><strong>Medical Diagnosis</strong></td>
          <td>Partial</td>
          <td>Single</td>
          <td>Stochastic</td>
          <td>Sequential</td>
          <td>Dynamic</td>
          <td>Continuous</td>
        </tr>
        <tr>
          <td><strong>Image Analysis</strong></td>
          <td>Fully</td>
          <td>Single</td>
          <td>Deterministic</td>
          <td>Episodic</td>
          <td>Semi</td>
          <td>Continuous</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Why This Matters for AI Design</h2>
  <div class="unit">
    <div class="comparison-row">
      <div class="comparison-card easy">
        <div class="comp-tag">The Easy Path</div>
        <h4>"Toy Worlds"</h4>
        <p><em>Fully Observable, Deterministic, Static, Discrete.</em></p>
        <p>Simple search algorithms and "Simple Reflex" architectures can solve these perfectly.</p>
      </div>
      <div class="comparison-card hard">
        <div class="comp-tag">The Challenge</div>
        <h4>The Real World</h4>
        <p><em>Partially Observable, Stochastic, Dynamic, Continuous.</em></p>
        <p>Requires sophisticated "Model-Based" or "Utility-Based" agents that handle uncertainty.</p>
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <div class="exam-tip">
    <h4 style="color: #fff; margin-top: 0; margin-bottom: 0.5rem;">Exam Tip</h4>
    If asked to describe an environment (like a "Vacuum Cleaner"), use these <strong>six terms</strong> as your technical headings to provide a complete answer.
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt104co/agent-architecture/">← Previous: 2.2 Agent Architecture and Types</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt104co/peas/">Next: 2.4 PEAS Framework →</a>
    </div>
  </div>
  <div style="text-align: center; margin-top: 30px;">
    <a href="/syllabus/bt104co/" class="back-link">Back to Course Syllabus</a>
  </div>
</div>

<style>
.dimensions-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 25px;
  margin-top: 2rem;
}
.dimension-card {
  padding: 1.5rem;
  background: #fff;
  border: 1px solid #e5e7eb;
  border-radius: 16px;
  position: relative;
  transition: all 0.3s ease;
}
.dimension-card:hover {
  transform: translateY(-5px);
  border-color: #000;
  box-shadow: 0 10px 25px -5px rgba(0,0,0,0.05);
}
.dim-num {
  font-size: 2rem;
  font-weight: 900;
  color: #f3f4f6;
  position: absolute;
  top: 1rem;
  right: 1rem;
  font-family: serif;
}
.dimension-card h4 {
  margin: 0 0 1rem 0;
  font-size: 1.1rem;
  padding-right: 2rem;
}
.dimension-card p {
  margin: 0 0 8px 0;
  font-size: 0.9rem;
  color: #4b5563;
}
.note-box {
  margin-top: 12px;
  padding: 8px 12px;
  background: #f9fafb;
  border-radius: 8px;
  font-size: 0.8rem;
  border-left: 3px solid #000;
}

.comparison-row {
  display: flex;
  gap: 25px;
  margin-top: 1.5rem;
}
.comparison-card {
  flex: 1;
  padding: 24px;
  border-radius: 20px;
  border: 1px solid #e5e7eb;
}
.comparison-card.easy { background: #f0fdf4; border-color: #dcfce7; }
.comparison-card.hard { background: #fffcf0; border-color: #fef3c7; }

.comp-tag {
  display: inline-block;
  font-size: 0.65rem;
  font-weight: 800;
  text-transform: uppercase;
  padding: 4px 10px;
  background: #fff;
  border-radius: 20px;
  margin-bottom: 12px;
  border: 1px solid rgba(0,0,0,0.05);
}

.comparison-card h4 { margin: 0 0 10px 0; }
.comparison-card p {
  font-size: 0.9rem;
  line-height: 1.5;
  color: #374151;
  margin-bottom: 0px;
}

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

@media (max-width: 768px) {
  .comparison-row {
    flex-direction: column;
  }
}
</style>
