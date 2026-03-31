---
layout: default
title: "2.7 Problem-Solving and Learning Agents"
course_code: BT104CO
permalink: /syllabus/bt104co/problem-solving-learning/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <h2>1. The Problem-Solving Agent</h2>
  <div class="unit">
    <p>A <strong>Problem-Solving Agent</strong> is a type of <strong>Goal-Based Agent</strong>. It decides what to do by finding sequences of actions that lead to desirable states.</p>
    
    <div class="process-flow">
      <div class="flow-item">
        <span class="flow-num">1</span>
        <strong>Goal Formulation:</strong> Decides which state is "desirable" (e.g., reaching Kathmandu).
      </div>
      <div class="flow-arrow">↓</div>
      <div class="flow-item">
        <span class="flow-num">2</span>
        <strong>Problem Formulation:</strong> Decides which actions and states to consider given the goal.
      </div>
      <div class="flow-arrow">↓</div>
      <div class="flow-item">
        <span class="flow-num">3</span>
        <strong>Search:</strong> Simulates action sequences in its "head" to find a path to the goal.
      </div>
      <div class="flow-arrow">↓</div>
      <div class="flow-item highlight">
        <span class="flow-num">4</span>
        <strong>Execution:</strong> Once a solution is found, the agent performs the actions one by one.
      </div>
    </div>
    
    <div class="note-box">
      <strong>Crucial Note:</strong> Problem-solving agents usually operate in <strong>"Open-loop"</strong> systems—they ignore their sensors while executing, assuming the world is deterministic.
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Problem Formulation (The 5-Tuple)</h2>
  <div class="unit">
    <p>To turn a vague desire into a computable problem, we must formally define these five components:</p>
    <div class="tuple-list">
      <div class="tuple-item"><span>1</span> <strong>Initial State:</strong> Where the agent starts (e.g., <em>In(Lalitpur)</em>).</div>
      <div class="tuple-item"><span>2</span> <strong>Actions:</strong> The set of possible moves available in a state $s$.</div>
      <div class="tuple-item"><span>3</span> <strong>Transition Model:</strong> The result of an action, expressed as $Result(s, a)$.</div>
      <div class="tuple-item"><span>4</span> <strong>Goal Test:</strong> A function checking if the current state matches the target.</div>
      <div class="tuple-item"><span>5</span> <strong>Path Cost:</strong> A numeric cost (distance, time, fuel) assigned to a path.</div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. The Learning Agent</h2>
  <div class="unit">
    <p>While standard agents rely on pre-programmed knowledge, a <strong>Learning Agent</strong> adapts in unknown environments.</p>
    
    <div class="learning-grid">
      <div class="learning-comp">
        <h4>Learning Element</h4>
        <p>Responsible for making improvements to the agent's logic based on feedback.</p>
      </div>
      <div class="learning-comp">
        <h4>Performance Element</h4>
        <p>This is the actual "agent" that selects actions based on percepts.</p>
      </div>
      <div class="learning-comp">
        <h4>The Critic</h4>
        <p>Compares results against a fixed <strong>performance standard</strong> to judge success.</p>
      </div>
      <div class="learning-comp highlight">
        <h4>Problem Generator</h4>
        <p>Suggests "exploratory" actions to help the agent learn more about the world.</p>
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Agent Comparison Summary</h2>
  <div class="unit">
    <table class="exam-table">
      <thead>
        <tr>
          <th>Agent Type</th>
          <th>Knowledge Source</th>
          <th>Decision Basis</th>
          <th>Uncertainty?</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>Problem-Solving</strong></td>
          <td>Pre-defined Model</td>
          <td>Search/Planning</td>
          <td>No (Deterministic)</td>
        </tr>
        <tr>
          <td><strong>Simple Reflex</strong></td>
          <td>Hard-coded Rules</td>
          <td>Current Percept</td>
          <td>Poorly</td>
        </tr>
        <tr>
          <td><strong>Learning Agent</strong></td>
          <td>Experience</td>
          <td>Feedback/Critic</td>
          <td>Yes (Adapts)</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Knowledge Representation Levels</h2>
  <div class="unit">
    <div class="representation-grid">
      <div class="rep-card">
        <div class="rep-title">Atomic</div>
        <p>State is a single unit/node with no internal parts (e.g., map node).</p>
      </div>
      <div class="rep-card">
        <div class="rep-title">Factored</div>
        <p>State is split into variables (e.g., GPS coordinates + Fuel level).</p>
      </div>
      <div class="rep-card">
        <div class="rep-title">Structured</div>
        <p>State includes relations (e.g., "The key is <em>inside</em> the box").</p>
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <div class="exam-tip">
    <h4 style="color: #fff; margin-top: 0; margin-bottom: 0.5rem;">Exam Tip</h4>
    Focus on the <strong>Problem Generator</strong>. It's the most unique part—it encourages "exploration" so the agent doesn't just repeat safe actions forever but finds better solutions over time.
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt104co/problem-types/">← Previous: 2.6 Problem Types</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt104co/constraint-satisfaction/">Next: 2.8 Constraint Satisfaction →</a>
    </div>
  </div>
  <div style="text-align: center; margin-top: 30px;">
    <a href="/syllabus/bt104co/" class="back-link">Back to Course Syllabus</a>
  </div>
</div>

<style>
.process-flow {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
  margin-top: 2rem;
}
.flow-item {
  width: 100%;
  max-width: 500px;
  padding: 1.25rem;
  background: #fff;
  border: 1px solid #e5e7eb;
  border-radius: 12px;
  display: flex;
  align-items: center;
  gap: 15px;
  font-size: 0.95rem;
}
.flow-num {
  width: 24px;
  height: 24px;
  background: #000;
  color: #fff;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 700;
  font-size: 0.75rem;
  flex-shrink: 0;
}
.flow-arrow {
  color: #9ca3af;
  font-size: 1.25rem;
}
.flow-item.highlight {
  border-color: #10b981;
  background: #f0fdf4;
}

.tuple-list {
  display: flex;
  flex-direction: column;
  gap: 10px;
  margin-top: 1rem;
}
.tuple-item {
  font-size: 0.95rem;
  color: #374151;
}
.tuple-item span {
  display: inline-block;
  font-weight: 800;
  color: #9ca3af;
  margin-right: 8px;
}

.learning-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 20px;
  margin-top: 2rem;
}
.learning-comp {
  padding: 1.5rem;
  background: #fff;
  border: 1px solid #e5e7eb;
  border-radius: 16px;
}
.learning-comp h4 { margin: 0 0 10px 0; font-size: 1rem; color: #111827; }
.learning-comp p { font-size: 0.85rem; color: #4b5563; margin: 0; }
.learning-comp.highlight { border-color: #6366f1; background: #f5f3ff; }

.representation-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 15px;
  margin-top: 1.5rem;
}
.rep-card {
  padding: 1.25rem;
  background: #f9fafb;
  border-radius: 12px;
}
.rep-title {
  font-weight: 800;
  font-size: 0.75rem;
  text-transform: uppercase;
  margin-bottom: 8px;
  color: #6366f1;
}
.rep-card p {
  font-size: 0.85rem;
  color: #374151;
  margin: 0;
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
.note-box {
  margin-top: 2rem;
  padding: 1rem 1.5rem;
  background: #fffcf0;
  border-left: 4px solid #fcd34d;
  font-size: 0.9rem;
  color: #92400e;
  border-radius: 0 12px 12px 0;
}
</style>
