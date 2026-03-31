---
layout: default
title: "2.4 The PEAS Framework"
course_code: BT104CO
permalink: /syllabus/bt104co/peas/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <h2>1. What is PEAS?</h2>
  <div class="unit">
    <p>In the framework of Russell and Norvig, <strong>PEAS</strong> is the first step in designing any AI. Before writing code, you must specify the task environment using these four headings.</p>
    
    <div class="peas-grid">
      <div class="peas-card p">
        <div class="peas-letter">P</div>
        <h4>Performance</h4>
        <p>The objective criteria for success. What the agent is trying to maximize (the "goal" or "reward").</p>
      </div>
      <div class="peas-card e">
        <div class="peas-letter">E</div>
        <h4>Environment</h4>
        <p>The external world or setting where the agent operates (roads, patient, image database).</p>
      </div>
      <div class="peas-card a">
        <div class="peas-letter">A</div>
        <h4>Actuators</h4>
        <p>The "tools" the agent uses to perform actions and change its environment (steering, display, tags).</p>
      </div>
      <div class="peas-card s">
        <div class="peas-letter">S</div>
        <h4>Sensors</h4>
        <p>The inputs the agent uses to perceive the environment and gather data (cameras, keyboard, LIDAR).</p>
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. PEAS Examples (Case Studies)</h2>
  <div class="unit">
    <p>To master PEAS for an exam, you should be able to break down any AI system into these four categories.</p>
    
    <!-- Taxi Driver -->
    <div class="example-case">
      <h3>Case A: Automated Taxi Driver</h3>
      <table class="exam-table">
        <tr><th>Category</th><th>Description</th></tr>
        <tr><td><strong>Performance</strong></td><td>Safety, speed, legal driving, passenger comfort, profit.</td></tr>
        <tr><td><strong>Environment</strong></td><td>Roads, other traffic, pedestrians, weather, customers.</td></tr>
        <tr><td><strong>Actuators</strong></td><td>Steering wheel, accelerator, brake, signal, horn, display.</td></tr>
        <tr><td><strong>Sensors</strong></td><td>Cameras, LIDAR, GPS, speedometer, engine sensors.</td></tr>
      </table>
    </div>

    <!-- Medical Diagnosis -->
    <div class="example-case">
      <h3>Case B: Medical Diagnosis System</h3>
      <table class="exam-table">
        <tr><th>Category</th><th>Description</th></tr>
        <tr><td><strong>Performance</strong></td><td>Healthy patient, minimized costs, avoiding malpractice.</td></tr>
        <tr><td><strong>Environment</strong></td><td>Patient, hospital staff, medical database.</td></tr>
        <tr><td><strong>Actuators</strong></td><td>Display of questions, tests, diagnoses, treatments.</td></tr>
        <tr><td><strong>Sensors</strong></td><td>Keyboard/Touchscreen (symptoms, lab results, history).</td></tr>
      </table>
    </div>

    <!-- Satellite Image Analysis -->
    <div class="example-case">
      <h3>Case C: Satellite Image Analysis</h3>
      <table class="exam-table">
        <tr><th>Category</th><th>Description</th></tr>
        <tr><td><strong>Performance</strong></td><td>Categorization accuracy, speed, minimized false positives.</td></tr>
        <tr><td><strong>Environment</strong></td><td>Downlink from satellite, image database, weather.</td></tr>
        <tr><td><strong>Actuators</strong></td><td>Tagging images, sending alerts, re-ordering database.</td></tr>
        <tr><td><strong>Sensors</strong></td><td>High-resolution cameras, infrared sensors.</td></tr>
      </table>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. The Relationship Between PEAS and Rationality</h2>
  <div class="unit">
    <p>A <strong>Rational Agent</strong> is defined relative to its PEAS. An action is rational if it follows this logic:</p>
    <div class="rational-logic">
      <div class="logic-step">1. Maximize the <strong>Performance</strong> measure...</div>
      <div class="logic-step">2. Given the history of <strong>Sensors</strong> (percepts)...</div>
      <div class="logic-step">3. Within the specified <strong>Environment</strong>...</div>
      <div class="logic-step">4. Using the available <strong>Actuators</strong>.</div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <div class="exam-tip">
    <h4 style="color: #fff; margin-top: 0; margin-bottom: 0.5rem;">The "Vacuum Cleaner" Gotcha</h4>
    <strong>Performance Measure Selection:</strong> If you give a vacuum cleaner a measure of "amount of dust collected," it might suck up dust, spit it out, and suck it up again to "maximize" its score. This is irrational. A better measure is <strong>"Cleanliness of the floor."</strong>
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt104co/task-environment/">← Previous: 2.3 Task Environments</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt104co/state-space-search/">Next: 2.5 State Space Search →</a>
    </div>
  </div>
  <div style="text-align: center; margin-top: 30px;">
    <a href="/syllabus/bt104co/" class="back-link">Back to Course Syllabus</a>
  </div>
</div>

<style>
.peas-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 20px;
  margin-top: 2rem;
}
.peas-card {
  padding: 1.5rem;
  background: #fff;
  border: 1px solid #e5e7eb;
  border-radius: 16px;
  transition: all 0.3s ease;
}
.peas-card:hover {
  transform: translateY(-5px);
  border-color: #000;
  box-shadow: 0 10px 25px -5px rgba(0,0,0,0.05);
}
.peas-letter {
  font-size: 3rem;
  font-weight: 900;
  margin-bottom: 10px;
}
.peas-card.p .peas-letter { color: #3b82f6; }
.peas-card.e .peas-letter { color: #10b981; }
.peas-card.a .peas-letter { color: #f59e0b; }
.peas-card.s .peas-letter { color: #ef4444; }

.peas-card h4 { margin: 0 0 8px 0; }
.peas-card p {
  font-size: 0.85rem;
  color: #4b5563;
  line-height: 1.5;
  margin: 0;
}

.example-case {
  margin-top: 3rem;
}
.example-case h3 {
  font-size: 1.25rem;
  margin-bottom: 15px;
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

.rational-logic {
  background: #000;
  color: #fff;
  padding: 2rem;
  border-radius: 20px;
  margin-top: 1.5rem;
}
.logic-step {
  font-size: 1.1rem;
  margin-bottom: 15px;
  font-weight: 500;
}
.logic-step strong { color: #60a5fa; }

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
