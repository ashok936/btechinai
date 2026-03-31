---
layout: default
title: "2.1 Agents and Environments"
course_code: BT104CO
permalink: /syllabus/bt104co/agent-environment/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <h2>1. Defining the Agent</h2>
  <div class="unit">
    <p>An <strong>agent</strong> is anything that can be viewed as perceiving its <strong>environment</strong> through <strong>sensors</strong> and acting upon that environment through <strong>actuators</strong>.</p>
    
    <div class="mermaid">
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#e3f2fd', 'edgeLabelBackground':'#ffffff', 'tertiaryColor': '#ffffff'}}}%%
graph LR
    subgraph Environment ["The External World"]
        State["Current State"]
    end

    subgraph Agent ["The Intelligent System"]
        S["Sensors"] --> Program["Agent Program \n (Processing)"]
        Program --> A["Actuators"]
    end

    State -- "Percepts" --> S
    A -- "Actions" --> State
    
    %% Styling for clarity
    classDef hardware fill:#bbdefb,stroke:#1976d2,stroke-width:1px,rx:5,ry:5;
    classDef software fill:#c8e6c9,stroke:#388e3c,stroke-width:2px,rx:10,ry:10;
    classDef world fill:#fff9c4,stroke:#fbc02d,stroke-width:1px,stroke-dasharray: 5 5;
    
    class S,A hardware;
    class Program software;
    class State world;
    class Environment world;
    </div>

    <div class="math-card">
      <h4>The Mathematical Model</h4>
      <p>The behavior of an agent is described by the <strong>Agent Function</strong>, which maps any given percept sequence to an action:</p>
      <div class="equation">
        $$f: P^* \rightarrow A$$
      </div>
      <ul class="definitions-list">
        <li><strong>$P^*$</strong>: The percept sequence (everything the agent has perceived to date).</li>
        <li><strong>$A$</strong>: The action to be performed.</li>
      </ul>
      <div class="distinction-box">
        <strong>Important Distinction:</strong> The <em>Agent Function</em> is an abstract mathematical description; the <em>Agent Program</em> is the actual implementation (the code) that runs on the physical architecture.
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Sensors and Actuators</h2>
  <div class="unit">
    <p>To interact with the world, an agent must have "hardware" or "software interfaces" for input and output.</p>
    
    <div class="interaction-grid">
      <div class="interaction-card">
        <div class="card-icon">👁️</div>
        <h4>Sensors</h4>
        <p>The inputs the agent uses to perceive the environment.</p>
        <ul class="examples-list">
          <li><strong>Human:</strong> Eyes, ears, skin.</li>
          <li><strong>Robotic:</strong> Cameras, infrared, GPS.</li>
          <li><strong>Software:</strong> Key presses, network packets.</li>
        </ul>
      </div>
      
      <div class="interaction-card">
        <div class="card-icon">⚡</div>
        <h4>Actuators</h4>
        <p>The mechanisms through which the agent performs actions.</p>
        <ul class="examples-list">
          <li><strong>Human:</strong> Hands, legs, vocal cords.</li>
          <li><strong>Robotic:</strong> Wheels, motors, screens.</li>
          <li><strong>Software:</strong> File writing, data packets.</li>
        </ul>
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. The Concept of "Percepts"</h2>
  <div class="unit">
    <p>A <strong>percept</strong> is the agent’s perceptual inputs at any given instant. An agent’s choice of action can depend on its <strong>percept sequence</strong>—the entire history of everything the agent has perceived so far.</p>
    <div class="exam-note">
      <strong>Note for Exams:</strong> An agent cannot see the <em>future</em>, and it may only have <em>partial observability</em> of the current state, so it must rely on its history (percept sequence) to make the most rational choice.
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. The Environment</h2>
  <div class="unit">
    <p>The <strong>environment</strong> is the world in which the agent lives and operates. It is everything "outside" the agent. The nature of the environment directly dictates the design of the agent.</p>
    
    <div class="comparison-row">
      <div class="env-type">
        <h5>Friendly & Static</h5>
        <p>Like a crossword puzzle. Agent can be simple.</p>
      </div>
      <div class="env-type">
        <h5>Hostile & Dynamic</h5>
        <p>Like a battlefield. Agent must be sophisticated.</p>
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Agent Architecture</h2>
  <div class="unit">
    <div class="equation-box">
      <strong>Agent = Architecture + Program</strong>
    </div>

    <div class="mermaid">
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#e8f5e9', 'edgeLabelBackground':'#ffffff'}}}%%
graph TD
    A["The Complete Agent"] --> |runs on| Arch["Architecture \n (PC, Robot Body, Server)"]
    A --> |executes the| Program["Agent Program \n (The actual code)"]
    
    Program -.-> |implements| Function["Agent Function \n (Mathematical Map: P* -> A)"]
    
    %% Styling for clarity
    classDef agentPart fill:#e1f5fe,stroke:#01579b,stroke-width:2px;
    classDef mathPart fill:#f3e5f5,stroke:#4a148c,stroke-width:1px,stroke-dasharray: 3 3;
    
    class A,Arch,Program agentPart;
    class Function mathPart;
    </div>

    <ol class="arch-list">
      <li><strong>Architecture:</strong> The physical device (PC, robotic chassis, cloud server) that makes percepts available and executes actions.</li>
      <li><strong>Program:</strong> The software that implements the agent function.</li>
    </ol>
  </div>
</div>

<div class="syllabus-section">
  <h2>Summary of Agent Types</h2>
  <div class="unit">
    <table class="exam-table">
      <thead>
        <tr>
          <th>Agent Type</th>
          <th>Percepts</th>
          <th>Actions</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>Medical System</strong></td>
          <td>Symptoms, lab results</td>
          <td>Diagnosis, treatment plan</td>
        </tr>
        <tr>
          <td><strong>Satellite Controller</strong></td>
          <td>Altitude, signal strength</td>
          <td>Adjust thrusters, aim antenna</td>
        </tr>
        <tr>
          <td><strong>Email Filter</strong></td>
          <td>Words, sender, attachments</td>
          <td>Mark as Spam, Move to Inbox</td>
        </tr>
        <tr>
          <td><strong>Vacuum Cleaner</strong></td>
          <td>Dust levels, bump sensor</td>
          <td>Move, turn, suck up dirt</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<div class="syllabus-section">
  <div class="exam-tip">
    <h4 style="color: #fff; margin-top: 0; margin-bottom: 0.5rem;">Exam Tip</h4>
    Be prepared to define an agent using the $f: P^* \rightarrow A$ notation. Remember that an agent is <strong>autonomous</strong> if its behavior is determined by its own experience rather than just built-in knowledge.
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt104co/applications-of-ai/">← Previous: 1.5 Applications of AI</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt104co/agent-architecture/">Next: 2.2 Agent Architecture →</a>
    </div>
  </div>
  <div style="text-align: center; margin-top: 30px;">
    <a href="/syllabus/bt104co/" class="back-link">Back to Course Syllabus</a>
  </div>
</div>

<style>
.math-card {
  background: #f9fafb;
  padding: 2rem;
  border-radius: 16px;
  border: 1px solid #e5e7eb;
  margin: 1.5rem 0;
}
.mermaid-container {
  margin: 2rem 0;
  display: flex;
  justify-content: center;
}
.mermaid {
  display: flex;
  justify-content: center;
  margin: 2rem 0;
  background: #fff;
  padding: 2rem;
  border-radius: 16px;
  border: 1px solid #f3f4f6;
}
.equation {
  font-size: 1.5rem;
  text-align: center;
  margin: 1.5rem 0;
  padding: 1rem;
  background: #fff;
  border-radius: 8px;
}
.definitions-list {
  list-style: none;
  padding: 0;
  margin-bottom: 1.5rem;
}
.definitions-list li {
  margin-bottom: 0.5rem;
  padding-left: 1.5rem;
  position: relative;
}
.definitions-list li::before {
  content: "•";
  position: absolute;
  left: 0;
  color: #000;
}
.distinction-box {
  padding: 1rem;
  background: #fff;
  border-left: 4px solid #000;
  font-size: 0.9rem;
}
.interaction-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
  margin-top: 1.5rem;
}
.interaction-card {
  padding: 1.5rem;
  background: #fff;
  border: 1px solid #e5e7eb;
  border-radius: 16px;
}
.card-icon {
  font-size: 2rem;
  margin-bottom: 1rem;
}
.examples-list {
  padding-left: 1.2rem;
  font-size: 0.85rem;
  color: #4b5563;
}
.exam-note {
  background: #fff9e6;
  border-left: 4px solid #ffcc00;
  padding: 1rem;
  margin-top: 1rem;
  font-size: 0.9rem;
}
.comparison-row {
  display: flex;
  gap: 20px;
  margin-top: 1.5rem;
}
.env-type {
  flex: 1;
  padding: 1.2rem;
  background: #f3f4f6;
  border-radius: 12px;
}
.env-type h5 {
  margin-top: 0;
  margin-bottom: 0.5rem;
  font-size: 1rem;
}
.env-type p {
  margin: 0;
  font-size: 0.85rem;
  color: #4b5563;
}
.equation-box {
  background: #000;
  color: #fff;
  padding: 1.5rem;
  border-radius: 12px;
  text-align: center;
  font-size: 1.2rem;
  margin-bottom: 1.5rem;
}
.arch-list {
  padding-left: 1.5rem;
}
.arch-list li {
  margin-bottom: 1rem;
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

@media (max-width: 600px) {
  .interaction-grid, .comparison-row {
    grid-template-columns: 1fr;
    flex-direction: column;
  }
}
</style>
