---
layout: default
title: "2.8 Constraint Satisfaction Problems (CSP)"
course_code: BT104CO
permalink: /syllabus/bt104co/constraint-satisfaction/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <h2>1. What is a CSP?</h2>
  <div class="unit">
    <p>In the framework of Russell and Norvig, a <strong>Constraint Satisfaction Problem (CSP)</strong> solves problems by looking at the <em>internal structure</em> of a state (Factored representation), rather than treating it as an Atomic "black box."</p>
    
    <div class="xdc-grid">
      <div class="xdc-card x">
        <div class="xdc-label">X</div>
        <h4>Variables</h4>
        <p>The set of items that need to be assigned values (e.g., $\{X_1, X_2...\}$).</p>
      </div>
      <div class="xdc-card d">
        <div class="xdc-label">D</div>
        <h4>Domains</h4>
        <p>The set of all possible values for each variable (e.g., $\{Red, Blue...\}$).</p>
      </div>
      <div class="xdc-card c">
        <div class="xdc-label">C</div>
        <h4>Constraints</h4>
        <p>Mathematical rules specifying which value combinations are allowed.</p>
      </div>
    </div>
    
    <div class="note-box">
      <strong>Core Difference:</strong> While standard search looks for a <strong>path</strong>, a CSP looks for a <strong>legal configuration</strong> of variables.
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Types of Constraints</h2>
  <div class="unit">
    <div class="constraints-container">
      <div class="c-type">
        <strong>Unary Constraints:</strong> Restrict a single variable (e.g., $SA \neq \text{green}$).
      </div>
      <div class="c-type">
        <strong>Binary Constraints:</strong> Relate two variables (e.g., $SA \neq NSW$, common in Map Coloring).
      </div>
      <div class="c-type">
        <strong>Global Constraints:</strong> Involve three or more variables (e.g., $Alldifferent$ in Sudoku).
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Cryptarithmetic Problems: The Rookie Guide</h2>
  <div class="unit">
    <p>Solving Cryptarithmetic problems is like being a detective uncovering hidden digits. We use <strong>CSP principles</strong>: deduction, exhaustion, and "carry" variables.</p>
    
    <div class="rookie-guide">
      <div class="guide-header">The Rookie's "Golden Rules"</div>
      <div class="rules-row">
        <div class="rule-item"><strong>1. The Leftover 1:</strong> Carry over to a new column is <em>always 1</em>.</div>
        <div class="rule-item"><strong>2. Unique Digits:</strong> Each letter is $0-9$. No twins allowed.</div>
        <div class="rule-item"><strong>3. No Zero Starts:</strong> Leading letters (S, M, etc.) cannot be $0$.</div>
      </div>
    </div>

    <div class="walkthrough-box">
      <h4>Case Study Walkthrough: SEND + MORE = MONEY</h4>
      <div class="step-list">
        <div class="step"><strong>Step 1: Find the "Freebie":</strong> The sum of two 4-digits makes a 5-digit number. The leading <code>M</code> must be the carry. <strong>M = 1</strong>.</div>
        <div class="step"><strong>Step 2: Solve the neighbor:</strong> $S + M = MO$. Since $M=1$, then $S+1 = 10+O$. If $S=9$, then <strong>O = 0</strong>.</div>
        <div class="step"><strong>Step 3: Solve the bridge:</strong> In $N + R = E$, we find that <strong>R = 8</strong> (given carries from right).</div>
        <div class="step"><strong>Step 4: Final Deduction:</strong> After testing pairs for $D + E = Y + 10$, we find <strong>D=7, E=5, N=6, Y=2</strong>.</div>
      </div>
      <div class="step-result">Result: <strong>9567 + 1085 = 10652</strong></div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. 5 Classic Solved Problems</h2>
  <div class="unit">
    <div class="puzzles-grid">
      <!-- Puzzle 2 -->
      <div class="puzzle-card">
        <div class="puzzle-header">Two + Two = Four</div>
        <code>  TWO<br>+ TWO<br>-----<br> FOUR</code>
        <p><strong>Logic:</strong> $R$ is even ($2O$). $F=1$ (carry). If $T=7, O=4 \to R=8$. If $W=3 \to U=6$.</p>
        <div class="puzzle-ans">734 + 734 = 1468</div>
      </div>

      <!-- Puzzle 3 -->
      <div class="puzzle-card">
        <div class="puzzle-header">Base + Ball = Games</div>
        <code>  BASE<br>+ BALL<br>------<br> GAMES</code>
        <p><strong>Logic:</strong> $G=1$ (carry). $A=0$ (since $2A=A$). If $B=7$ (with carry) $\to G=1, A=0$.</p>
        <div class="puzzle-ans">7043 + 7055 = 14098</div>
      </div>

      <!-- Puzzle 4 -->
      <div class="puzzle-card">
        <div class="puzzle-header">Forty + Ten + Ten = Sixty</div>
        <code>  FORTY<br>    TEN<br>+   TEN<br>-------<br> SIXTY</code>
        <p><strong>Logic:</strong> $2N=10 \to N=5$ or $0$. Testing confirms $N=0, E=5, T=8$.</p>
        <div class="puzzle-ans">29786 + 850 + 850 = 31486</div>
      </div>

      <!-- Puzzle 5 -->
      <div class="puzzle-card">
        <div class="puzzle-header">Eat + That = Apple</div>
        <code>    EAT<br>+  THAT<br>-------<br> APPLE</code>
        <p><strong>Logic:</strong> $A=1$ (carry). $T=9$ (needed for carry). $P=0$ ($9+1=10$). $E=8$ ($9+9=18$).</p>
        <div class="puzzle-ans">819 + 9219 = 10038</div>
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Solving CSPs: Backtracking Search</h2>
  <div class="unit">
    <p>The standard algorithm is <strong>Backtracking Search</strong>—a Depth-First Search that chooses values for one variable at a time, "backtracking" immediately if a constraint is violated.</p>
    
    <div class="heuristics-grid">
      <div class="h-card">
        <div class="h-title">MRV Heuristic</div>
        <p><strong>Minimum Remaining Values:</strong> Pick the variable with the fewest "legal" values left. Also called the <em>Most Constrained Variable</em>.</p>
      </div>
      <div class="h-card">
        <div class="h-title">Degree Heuristic</div>
        <p>Choice based on the largest number of constraints on other unassigned variables. Acts as a tie-breaker for MRV.</p>
      </div>
      <div class="h-card">
        <div class="h-title">LCV Heuristic</div>
        <p><strong>Least Constraining Value:</strong> Choose the value that rules out the fewest choices for its neighbors.</p>
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>6. Quick Practice & Troubleshooting</h2>
  <div class="unit">
    <div class="practice-grid">
      <div class="practice-item">
        <strong>1. CP + IS = ART</strong><br>
        <small>Hint: $A=1$. Look at $C+I=A$.</small>
      </div>
      <div class="practice-item">
        <strong>2. AA + BB = CCB</strong><br>
        <small>Hint: $C=1, A=9$.</small>
      </div>
      <div class="practice-item">
        <strong>3. GO + TO = OUT</strong><br>
        <small>Hint: $O=1, T=2$.</small>
      </div>
    </div>

    <div class="troubleshoot-box">
      <h4>Rookie Troubleshooting Guide</h4>
      <ul>
        <li><strong>Stuck?</strong> Find the letter that appears most often—that's your "anchor."</li>
        <li><strong>Contradiction?</strong> If you find $E=5$ but $A$ is already $5$, your first guess (usually $S$ or $O$) was wrong. Backtrack!</li>
        <li><strong>Carry Mark:</strong> Always write a small "$1$" above your math columns. It changes everything!</li>
      </ul>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <div class="assignment-box">
    <h3>Unit 2 Assignment: CSP Master</h3>
    <p>Using the **Backtracking Search** logic and **MRV Heuristic**, solve the following 3 problems. Submit your step-by-step deductions.</p>
    <div class="assignment-tasks">
      <div class="task"><strong>Task 1:</strong> Formalize the "Map Coloring Problem" for 4 neighboring provinces using X, D, and C.</div>
      <div class="task"><strong>Task 2:</strong> Solve the cryptarithmetic puzzle <code>USA + USSR = PEACE</code>.</div>
      <div class="task"><strong>Task 3:</strong> Explain why the <strong>Degree Heuristic</strong> is used as a tie-breaker for <strong>MRV</strong>.</div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <div class="exam-tip">
    <h4 style="color: #fff; margin-top: 0; margin-bottom: 0.5rem;">Exam Tip</h4>
    In Cryptarithmetic, never forget the <strong>Carry Variables</strong> ($c_k$). Without carries, you cannot express the mathematical logic of the column-wise addition correctly in a CSP format.
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt104co/problem-solving-learning/">← Previous: 2.7 Problem-Solving Agents</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt104co/game-playing/">Next: 2.9 Game Playing →</a>
    </div>
  </div>
  <div style="text-align: center; margin-top: 30px;">
    <a href="/syllabus/bt104co/" class="back-link">Back to Course Syllabus</a>
  </div>
</div>

<style>
.xdc-grid {
  display: flex;
  gap: 20px;
  margin-top: 2rem;
}
.xdc-card {
  flex: 1;
  padding: 1.5rem;
  background: #fff;
  border: 1px solid #e1e4e8;
  border-radius: 16px;
  text-align: center;
}
.xdc-label {
  font-size: 2.5rem;
  font-weight: 900;
  margin-bottom: 10px;
  color: #000;
  font-family: serif;
}
.xdc-card h4 { margin: 0 0 10px 0; font-size: 1rem; }
.xdc-card p { font-size: 0.85rem; color: #4b5563; margin: 0; line-height: 1.4; }

.constraints-container {
  display: flex;
  flex-direction: column;
  gap: 12px;
  margin-top: 1.5rem;
}
.c-type {
  padding: 1rem 1.5rem;
  background: #f9fafb;
  border-radius: 10px;
  font-size: 0.95rem;
  border-left: 4px solid #000;
}

.heuristics-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 20px;
  margin-top: 2rem;
}
.h-card {
  padding: 1.5rem;
  background: #fff;
  border: 1px solid #f3f4f6;
  border-radius: 20px;
  box-shadow: 0 4px 6px -1px rgba(0,0,0,0.05);
}
.h-title {
  font-weight: 800;
  font-size: 0.8rem;
  text-transform: uppercase;
  color: #6366f1;
  margin-bottom: 10px;
}
.h-card p { font-size: 0.85rem; color: #374151; margin: 0; line-height: 1.5; }

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

.note-box {
  margin-top: 2rem;
  padding: 1.25rem;
  background: #f5f3ff;
  border-radius: 12px;
  font-size: 0.9rem;
  color: #4338ca;
}
.exam-tip {
  background: #000;
  color: #fff;
  padding: 1.5rem;
  border-radius: 12px;
  margin-top: 2rem;
}
.rookie-guide {
  background: #000;
  color: #fff;
  padding: 2rem;
  border-radius: 20px;
  margin: 2rem 0;
}
.guide-header {
  font-weight: 800;
  text-transform: uppercase;
  font-size: 0.75rem;
  letter-spacing: 0.1em;
  color: #60a5fa;
  margin-bottom: 1.5rem;
}
.rules-row {
  display: flex;
  gap: 20px;
}
.rule-item {
  flex: 1;
  font-size: 0.9rem;
  line-height: 1.5;
}

.walkthrough-box {
  background: #f9fafb;
  padding: 2rem;
  border-radius: 20px;
  border: 1px solid #e5e7eb;
}
.step-list {
  margin-top: 1.5rem;
}
.step {
  padding: 10px 0;
  border-bottom: 1px dashed #e5e7eb;
  font-size: 0.9rem;
}
.step-result {
  margin-top: 1.5rem;
  font-weight: 800;
  color: #059669;
}

.puzzles-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 25px;
  margin-top: 2rem;
}
.puzzle-card {
  padding: 1.5rem;
  background: #fff;
  border: 1px solid #e1e4e8;
  border-radius: 16px;
}
.puzzle-header {
  font-weight: 800;
  font-size: 0.8rem;
  text-transform: uppercase;
  margin-bottom: 15px;
  color: #000;
}
.puzzle-card code {
  display: block;
  background: #f3f4f6;
  padding: 1rem;
  border-radius: 8px;
  margin-bottom: 1rem;
  font-size: 1.1rem;
}
.puzzle-card p {
  font-size: 0.8rem;
  color: #4b5563;
  margin-bottom: 10px;
}
.puzzle-ans {
  font-weight: 700;
  font-size: 0.9rem;
  color: #3b82f6;
}

.practice-grid {
  display: flex;
  gap: 15px;
  margin: 2rem 0;
}
.practice-item {
  flex: 1;
  padding: 1rem;
  background: #fff;
  border: 1px solid #e5e7eb;
  border-radius: 10px;
  font-size: 0.85rem;
}
.troubleshoot-box {
  padding: 1.5rem;
  background: #fffcf0;
  border-radius: 12px;
  border: 1px solid #fef3c7;
}

.assignment-box {
  background: #000;
  color: #fff;
  padding: 2.5rem;
  border-radius: 24px;
  margin-top: 3rem;
}
.assignment-tasks {
  margin-top: 1.5rem;
}
.task {
  padding: 12px 15px;
  background: rgba(255,255,255,0.05);
  border-radius: 10px;
  margin-bottom: 10px;
  font-size: 0.9rem;
}

.back-link {
  font-size: 0.9rem;
  font-weight: 600;
  text-decoration: none;
  color: var(--text-muted);
  border-bottom: 1px solid var(--border-color);
  padding-bottom: 4px;
}
@media (max-width: 768px) {
  .rules-row, .practice-grid { flex-direction: column; }
}
</style>
