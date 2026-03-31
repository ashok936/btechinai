---
layout: default
title: "2.5 Defining Problems as State Space Search"
course_code: BT104CO
permalink: /syllabus/bt104co/state-space-search/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <h2>1. What is a State Space?</h2>
  <div class="unit">
    <p>In Russell and Norvig's framework, a goal-based agent must first formalize its goal into a "problem" that can be solved using search algorithms.</p>
    
    <div class="definition-box">
      <div class="def-item">
        <strong>State:</strong> A configuration of the agent and its environment at a specific moment.
      </div>
      <div class="def-item">
        <strong>State Space:</strong> The set of <strong>all possible states</strong> reachable from the initial state by any sequence of actions.
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. The 5 Components of a Formal Problem</h2>
  <div class="unit">
    <p>To define a problem for an AI, you must specify these five elements:</p>
    
    <div class="components-grid">
      <!-- 1. Initial State -->
      <div class="comp-card">
        <div class="comp-num">I</div>
        <h4>Initial State</h4>
        <p>The state the agent starts in (e.g., initial piece arrangement in Chess).</p>
      </div>

      <!-- 2. Actions -->
      <div class="comp-card">
        <div class="comp-num">II</div>
        <h4>Actions</h4>
        <p>Possible actions available. $Actions(s)$ returns all legal moves from state $s$.</p>
      </div>

      <!-- 3. Transition Model -->
      <div class="comp-card">
        <div class="comp-num">III</div>
        <h4>Transition Model</h4>
        <p>What each action does. $Result(s, a)$ returns the state resulting from action $a$ in state $s$.</p>
      </div>

      <!-- 4. Goal Test -->
      <div class="comp-card">
        <div class="comp-num">IV</div>
        <h4>Goal Test</h4>
        <p>Condition determining if a state is a <strong>Goal State</strong> (e.g., checkmate).</p>
      </div>

      <!-- 5. Path Cost -->
      <div class="comp-card">
        <div class="comp-num">V</div>
        <h4>Path Cost</h4>
        <p>Assigns a numeric cost to each path. Agents seek the <strong>lowest cost</strong> (e.g., distance, time).</p>
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Real-World vs. Toy Problems</h2>
  <div class="unit">
    <div class="problem-types">
      <div class="problem-type toy">
        <h4>Toy Problems</h4>
        <p>Precise descriptions used to exercise search methods.</p>
        <ul>
          <li>8-puzzle / Sudoku</li>
          <li>Vacuum-world</li>
          <li>The 8-queens problem</li>
        </ul>
      </div>
      <div class="problem-type real">
        <h4>Real-World Problems</h4>
        <p>Complex, "noisy" problems that solutions are actually needed for.</p>
        <ul>
          <li>Airline travel planning</li>
          <li>VLSI layout design</li>
          <li>Robot navigation</li>
        </ul>
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Key Concepts in Search</h2>
  <div class="unit">
    <div class="concepts-container">
      <div class="concept-item">
        <strong>A. State Space Graph:</strong> A visualization where <strong>nodes</strong> are states and <strong>edges</strong> are actions.
      </div>
      <div class="concept-item">
        <strong>B. Solution:</strong> An action sequence leading from Initial to Goal state.
      </div>
      <div class="concept-item">
        <strong>C. Optimal Solution:</strong> The path with the <strong>lowest path cost</strong> among all solutions.
      </div>
      <div class="concept-item">
        <strong>D. Abstraction:</strong> Removing irrelevant details (e.g., tile color) to keep only necessary data.
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Example: Formalizing the 8-Puzzle</h2>
  <div class="unit">
    <table class="exam-table">
      <thead>
        <tr>
          <th>Component</th>
          <th>8-Puzzle Description</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>Initial State</strong></td>
          <td>Any specific configuration of tiles on the $3 \times 3$ board.</td>
        </tr>
        <tr>
          <td><strong>Actions</strong></td>
          <td>Move the "blank" space {Left, Right, Up, Down}.</td>
        </tr>
        <tr>
          <td><strong>Transition Model</strong></td>
          <td>The new board configuration after sliding a tile.</td>
        </tr>
        <tr>
          <td><strong>Goal Test</strong></td>
          <td>Does the board match the target state (e.g., $1, 2, 3...$)?</td>
        </tr>
        <tr>
          <td><strong>Path Cost</strong></td>
          <td>Each move costs 1. Path cost is the total number of moves.</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<div class="syllabus-section">
  <div class="exam-tip">
    <h4 style="color: #fff; margin-top: 0; margin-bottom: 0.5rem;">Exam Tip</h4>
    If asked to <strong>"formalize"</strong> a problem (like the Water Jug or Missionaries & Cannibals), strictly list these <strong>five components</strong>. This structure ensures full marks and technical accuracy.
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt104co/peas/">← Previous: 2.4 PEAS Framework</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt104co/problem-types/">Next: 2.6 Problem Types →</a>
    </div>
  </div>
  <div style="text-align: center; margin-top: 30px;">
    <a href="/syllabus/bt104co/" class="back-link">Back to Course Syllabus</a>
  </div>
</div>

<style>
.definition-box {
  background: #f9fafb;
  padding: 1.5rem;
  border-radius: 12px;
  border: 1px solid #e5e7eb;
}
.def-item {
  margin-bottom: 10px;
  font-size: 0.95rem;
}
.def-item:last-child { margin-bottom: 0; }

.components-grid {
  display: flex;
  flex-direction: column;
  gap: 15px;
  margin-top: 1.5rem;
}
.comp-card {
  display: flex;
  align-items: flex-start;
  gap: 20px;
  padding: 1.2rem;
  background: #fff;
  border: 1px solid #e1e4e8;
  border-radius: 12px;
}
.comp-num {
  background: #000;
  color: #fff;
  width: 32px;
  height: 32px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 700;
  font-size: 0.8rem;
  flex-shrink: 0;
}
.comp-card h4 {
  margin: 0 0 5px 0;
  font-size: 1rem;
}
.comp-card p {
  margin: 0;
  font-size: 0.85rem;
  color: #4b5563;
}

.problem-types {
  display: flex;
  gap: 20px;
  margin-top: 1.5rem;
}
.problem-type {
  flex: 1;
  padding: 1.5rem;
  border-radius: 16px;
  border: 1px solid #e5e7eb;
}
.problem-type.toy { background: #f8f9fa; }
.problem-type.real { background: #fff; }
.problem-type h4 { margin-top: 0; }
.problem-type ul {
  padding-left: 1.2rem;
  margin-bottom: 0;
  font-size: 0.85rem;
  color: #4b5563;
}

.concepts-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 15px;
  margin-top: 1.5rem;
}
.concept-item {
  padding: 1rem;
  border-bottom: 1px solid #f3f4f6;
  font-size: 0.9rem;
}

.exam-table {
  width: 100%;
  border-collapse: collapse;
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
</style>
