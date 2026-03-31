---
layout: default
title: "2.9 Game Playing"
course_code: BT104CO
permalink: /syllabus/bt104co/game-playing/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <h2>1. Formal Definition of a Game</h2>
  <div class="unit">
    <p>A game is formally defined as a search problem using these six components:</p>
    
    <div class="game-formalism-grid">
      <div class="f-card">
        <div class="f-symbol">$S_0$</div>
        <strong>Initial State:</strong> How the game starts (e.g., an empty board).
      </div>
      <div class="f-card">
        <div class="f-symbol">$Player(s)$</div>
        <strong>Turn-Taker:</strong> Defines which player has the move in state $s$.
      </div>
      <div class="f-card">
        <div class="f-symbol">$Actions(s)$</div>
        <strong>Legal Moves:</strong> Returns the set of valid actions in state $s$.
      </div>
      <div class="f-card">
        <div class="f-symbol">$Result(s, a)$</div>
        <strong>Transition:</strong> Defines the state resulting from move $a$ in state $s$.
      </div>
      <div class="f-card">
        <div class="f-symbol">$Terminal\_Test(s)$</div>
        <strong>End-Check:</strong> <em>True</em> when the game is over.
      </div>
      <div class="f-card highlight">
        <div class="f-symbol">$Utility(s, p)$</div>
        <strong>Outcome Score:</strong> The numeric value for player $p$ at the end.
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. The Minimax Algorithm</h2>
  <div class="unit">
    <p>The core strategy for games is the <strong>Minimax Search</strong>. In a two-player game, we name the players <strong>MAX</strong> (the AI) and <strong>MIN</strong> (the opponent).</p>
    
    <div class="minimax-logic">
      <div class="logic-side max">
        <h4>MAX Player</h4>
        <p>Tries to <strong>maximize</strong> its utility. Always wants the highest possible score.</p>
      </div>
      <div class="logic-side min">
        <h4>MIN Player</h4>
        <p>Tries to <strong>minimize</strong> MAX's utility. Always chooses the lowest score for the AI.</p>
      </div>
    </div>

    <div class="flow-steps">
      <div class="step">1. Generate the whole <strong>game tree</strong> down to terminal states.</div>
      <div class="step">2. Apply <strong>Utility Function</strong> to the terminal states.</div>
      <div class="step">3. <strong>Back up values:</strong> MIN nodes choose the minimum child; MAX nodes choose the maximum child.</div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Alpha-Beta Pruning (Optimization)</h2>
  <div class="unit">
    <p>Since the search tree grows exponentially ($b^d$), we use <strong>Alpha-Beta Pruning</strong> to ignore branches that cannot affect the final decision.</p>
    
    <div class="ab-grid">
      <div class="ab-val a">
        <div class="ab-label">Alpha ($\alpha$)</div>
        <p>The <strong>highest-value</strong> choice found so far for MAX.</p>
      </div>
      <div class="ab-val b">
        <div class="ab-label">Beta ($\beta$)</div>
        <p>The <strong>lowest-value</strong> choice found so far for MIN.</p>
      </div>
    </div>

    <div class="pruning-rule">
      <strong>Pruning Rule:</strong> If at any point <strong>$\alpha \ge \beta$</strong>, we stop searching that branch. A rational opponent would never allow the game to move into that branch.
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Real-Time Games (Heuristic Minimax)</h2>
  <div class="unit">
    <div class="heuristic-container">
      <div class="h-item">
        <strong>Cutoff Test:</strong> Stop searching at a certain depth (e.g., 5 moves ahead) rather than the end.
      </div>
      <div class="h-item">
        <strong>Evaluation Function ($Eval$):</strong> "Guess" how good a state is (e.g., material value in Chess: Queen=9, Pawn=1).
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Game Environment Dimensions</h2>
  <div class="unit">
    <table class="exam-table">
      <thead>
        <tr>
          <th>Property</th>
          <th>Typical Value</th>
          <th>Why?</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>Observability</strong></td>
          <td>Fully Observable</td>
          <td>Both players see the whole board.</td>
        </tr>
        <tr>
          <td><strong>Determinism</strong></td>
          <td>Deterministic</td>
          <td>No luck or "dice" (usually).</td>
        </tr>
        <tr>
          <td><strong>Agents</strong></td>
          <td>Multiagent</td>
          <td>At least two players involved.</td>
        </tr>
        <tr>
          <td><strong>Relation</strong></td>
          <td>Competitive</td>
          <td>One's gain is the other's loss.</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<div class="syllabus-section">
  <div class="exam-tip">
    <h4 style="color: #fff; margin-top: 0; margin-bottom: 0.5rem;">The "Zero-Sum" Game</h4>
    Games in this chapter are <strong>Zero-Sum</strong>. Total benefit adds up to zero. If I win ($+1$), you must lose ($-1$). This is why MIN's goal is exactly the mathematically opposite of MAX's goal.
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt104co/constraint-satisfaction/">← Previous: 2.8 Constraint Satisfaction</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt104co/search-strategies-intro/">Next: Unit 3 Search Strategies →</a>
    </div>
  </div>
  <div style="text-align: center; margin-top: 30px;">
    <a href="/syllabus/bt104co/" class="back-link">Back to Course Syllabus</a>
  </div>
</div>

<style>
.game-formalism-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 15px;
  margin-top: 1.5rem;
}
.f-card {
  padding: 1.25rem;
  background: #fff;
  border: 1px solid #e5e7eb;
  border-radius: 12px;
  font-size: 0.9rem;
  line-height: 1.4;
}
.f-symbol {
  font-family: serif;
  font-size: 1.25rem;
  font-weight: 900;
  color: #6366f1;
  margin-bottom: 8px;
}
.f-card.highlight {
  border-color: #10b981;
  background: #f0fdf4;
}

.minimax-logic {
  display: flex;
  gap: 20px;
  margin-top: 2rem;
}
.logic-side {
  flex: 1;
  padding: 1.5rem;
  border-radius: 16px;
  color: #fff;
}
.logic-side.max { background: #111827; }
.logic-side.min { background: #374151; }
.logic-side h4 { margin: 0 0 10px 0; font-size: 0.75rem; text-transform: uppercase; letter-spacing: 0.05em; }
.logic-side p { margin: 0; font-size: 0.95rem; }

.flow-steps {
  margin-top: 2rem;
  padding: 1.5rem;
  background: #f9fafb;
  border-radius: 12px;
}
.flow-steps .step { padding: 8px 0; border-bottom: 1px solid #f3f4f6; font-size: 0.95rem; }

.ab-grid {
  display: flex;
  gap: 20px;
  margin-top: 1.5rem;
}
.ab-val {
  flex: 1;
  padding: 1.5rem;
  background: #fff;
  border: 1px solid #e1e4e8;
  border-radius: 16px;
}
.ab-label { font-weight: 800; font-size: 0.95rem; margin-bottom: 8px; }
.ab-val.a .ab-label { color: #3b82f6; }
.ab-val.b .ab-label { color: #ef4444; }
.ab-val p { margin: 0; font-size: 0.85rem; color: #4b5563; }

.pruning-rule {
  margin-top: 1.5rem;
  padding: 1.5rem;
  background: #000;
  color: #fff;
  border-radius: 12px;
  text-align: center;
  font-size: 1.05rem;
}

.heuristic-container {
  display: flex;
  gap: 20px;
  margin-top: 1.5rem;
}
.h-item {
  flex: 1;
  padding: 1.5rem;
  background: #fdf2f2;
  border-radius: 12px;
  font-size: 0.9rem;
  color: #9b1c1c;
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
}
@media (max-width: 600px) {
  .minimax-logic, .ab-grid, .heuristic-container { flex-direction: column; }
}
</style>
