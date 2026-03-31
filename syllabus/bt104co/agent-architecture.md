---
layout: default
title: "2.2 Agent Architecture"
course_code: BT104CO
permalink: /syllabus/bt104co/agent-architecture/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <h2>1. The Agent Equation</h2>
  <div class="unit">
    <p>In the framework of Russell and Norvig, the internal structure of an AI is defined as the <strong>Agent Architecture</strong>. It is the relationship between physical hardware and controlling software.</p>
    
    <div class="equation-box">
      <strong>Agent = Architecture + Program</strong>
    </div>

    <div class="arch-description">
      <ul>
        <li><strong>Architecture:</strong> The physical device or computing platform (e.g., PC, robotic chassis, cloud server).</li>
        <li><strong>Program:</strong> The computer code that implements the <strong>Agent Function</strong> (mapping percepts to actions).</li>
      </ul>
      <p>The Architecture makes percepts from sensors available to the Program, runs the logic, and feeds the chosen actions to the Actuators.</p>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Basic Architecture Diagram</h2>
  <div class="unit">
    <p>The architecture serves as the "bridge" between the software logic and the physical world.</p>
    <div class="mermaid">
graph TD
    subgraph Agent ["The Agent"]
        direction TB
        Program["Agent Program \n Logic/Software"]
        Arch["Architecture \n Hardware/PC/Robot"]
    end
    
    Env["Environment"] -- "Percepts" --> Sensors
    Sensors -- "Data" --> Arch
    Arch -- "Input" --> Program
    Program -- "Decision" --> Arch
    Arch -- "Commands" --> Actuators
    Actuators -- "Actions" --> Env

    style Program fill:#c8e6c9,stroke:#388e3c
    style Arch fill:#bbdefb,stroke:#1976d2
    style Env fill:#fff9c4,stroke:#fbc02d
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. Four Basic Types of Agent Architectures</h2>
  <div class="unit">
    <p>Agent programs are categorized based on how the architecture processes information. As we move down this list, the "internal mind" becomes more complex.</p>
    
    <div class="architecture-types">
      <!-- Simple Reflex Agent -->
      <div class="arch-section">
        <h3>A. Simple Reflex Agent</h3>
        <p>Acts based only on the current percept, using pre-defined condition-action rules.</p>
        <div class="arch-details">
          <ul>
            <li><strong>Logic:</strong> "If <strong>[Condition]</strong>, then <strong>[Action]</strong>."</li>
            <li><strong>Best For:</strong> Fully observable environments.</li>
            <li><strong>Examples:</strong>
              <ul>
                <li><strong>Medical System:</strong> If "high fever", prescribe paracetamol.</li>
                <li><strong>Thermostat:</strong> If "temp < 20°C", turn on heater.</li>
                <li><strong>Automated Camera:</strong> If "lighting is dark", activate flash.</li>
              </ul>
            </li>
          </ul>
        </div>
        <div class="mermaid">
graph LR
    subgraph Env ["Environment"]
        World["Current State"]
    end

    subgraph Agent ["Simple Reflex Agent"]
        direction TB
        Sensors --> Rules["Condition-Action Rules"]
        Rules --> Actuators
    end

    World -- "Percepts" --> Sensors
    Actuators -- "Actions" --> World

    style Rules fill:#f9f9f9,stroke:#333
    style Sensors fill:#fff,stroke:#333
    style Actuators fill:#fff,stroke:#333
    style Env fill:#eeeeee,stroke:#999
        </div>
      </div>

      <!-- Model-Based Reflex Agent -->
      <div class="arch-section">
        <h3>B. Model-Based Reflex Agent</h3>
        <p>Maintains an internal state that depends on the percept history to handle partially observable environments.</p>
        <div class="arch-details">
          <ul>
            <li><strong>Logic:</strong> "What is the world like now? (Even the parts I can't see)."</li>
            <li><strong>Best For:</strong> Environments requiring "memory" of the past.</li>
            <li><strong>Examples:</strong>
              <ul>
                <li><strong>Self-Driving Car:</strong> Remembers a cyclist in the blind spot from 2 seconds ago.</li>
                <li><strong>Dishwasher:</strong> Knows it's in the "rinse cycle" even if current sensor readings match the "wash cycle".</li>
              </ul>
            </li>
          </ul>
        </div>
        <div class="mermaid">
graph LR
    subgraph Env ["Environment"]
        World["Current State"]
    end

    subgraph Agent ["Model-Based Reflex Agent"]
        direction TB
        Sensors --> CurState["What the world \n is like now"]
        
        Evolution["How the world \n evolves"] --> CurState
        ActionsDo["What my \n actions do"] --> CurState
        
        CurState --> Rules["Condition-Action Rules"]
        Rules --> Actuators
    end

    World -- "Percepts" --> Sensors
    Actuators -- "Actions" --> World

    style CurState fill:#f9f9f9,stroke:#333
    style Evolution fill:#fff,stroke:#333,stroke-dasharray: 5 5
    style ActionsDo fill:#fff,stroke:#333,stroke-dasharray: 5 5
        </div>
      </div>

      <!-- Goal-Based Agent -->
      <div class="arch-section">
        <h3>C. Goal-Based Agent</h3>
        <p>Uses goals to guide its actions, choosing those that lead to a desired state via search and planning.</p>
        <div class="arch-details">
          <ul>
            <li><strong>Logic:</strong> "What will happen if I do Action X, and will it get me closer to my Goal?"</li>
            <li><strong>Best For:</strong> Complex tasks where the right action depends on the destination.</li>
            <li><strong>Examples:</strong>
              <ul>
                <li><strong>GPS/Maps:</strong> Evaluates thousands of turns to find the sequence ending at the goal.</li>
                <li><strong>Robotic Arm:</strong> Plans joint trajectories to reach a specific coordinate ("place bolt").</li>
              </ul>
            </li>
          </ul>
        </div>
        <div class="mermaid">
graph LR
    subgraph Env ["Environment"]
        World["Current State"]
    end

    subgraph Agent ["Goal-Based Agent"]
        direction TB
        Sensors --> CurState["What the world \n is like now"]
        CurState --> Predict["What it will be like \n if I do action A"]
        Goals["Goals"] --> Predict
        Predict --> Choice["What action I \n should do now"]
        Choice --> Actuators
    end

    World -- "Percepts" --> Sensors
    Actuators -- "Actions" --> World

    style Goals fill:#e3f2fd,stroke:#1976d2
    style Choice fill:#f9f9f9,stroke:#333
        </div>
      </div>

      <!-- Utility-Based Agent -->
      <div class="arch-section">
        <h3>D. Utility-Based Agent</h3>
        <p>Chooses actions to maximize a utility function ("happiness" or "success") when there are multiple paths or trade-offs.</p>
        <div class="arch-details">
          <ul>
            <li><strong>Logic:</strong> "How happy will I be in this state? Is this path better?"</li>
            <li><strong>Best For:</strong> Environments with conflicting requirements (e.g., speed vs. safety).</li>
            <li><strong>Examples:</strong>
              <ul>
                <li><strong>Automated Taxi:</strong> Chooses the fastest, cheapest, and most comfortable route among many.</li>
                <li><strong>Trading Bot:</strong> Balances potential gain against risk of loss.</li>
              </ul>
            </li>
          </ul>
        </div>
        <div class="mermaid">
graph LR
    subgraph Env ["Environment"]
        World["Current State"]
    end

    subgraph Agent ["Utility-Based Agent"]
        direction TB
        Sensors --> CurState["What the world \n is like now"]
        CurState --> Predict["What it will be like \n if I do action A"]
        Predict --> Utility["How happy will \n I be in such a state"]
        Utility --> Choice["What action I \n should do now"]
        Choice --> Actuators
    end

    World -- "Percepts" --> Sensors
    Actuators -- "Actions" --> World

    style Utility fill:#f3e5f5,stroke:#4a148c
        </div>
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. The Learning Agent Architecture</h2>
  <div class="unit">
    <p>Any of the above architectures can be turned into a <strong>Learning Agent</strong>, allowing the AI to improve over time.</p>
    
    <div class="learning-container">
      <div class="mermaid">
graph LR
    subgraph Env ["Environment"]
        World["Current State"]
    end

    subgraph Agent ["Learning Agent"]
        direction TB
        Sensors --> Critic["Critic"]
        Critic --> Learning["Learning \n Element"]
        Learning --> Performance["Performance \n Element"]
        Performance --> Actuators
        
        Standard["Performance Standard"] --> Critic
        Learning --> Changes["Knowledge/Modifications"]
        Changes --> Performance
        Learning --> Generator["Problem \n Generator"]
        Generator --> Performance
    end

    World -- "Percepts" --> Sensors
    Actuators -- "Actions" --> World

    style Learning fill:#e8f5e9,stroke:#2e7d32
    style Critic fill:#fff3e0,stroke:#ef6c00
    style Generator fill:#f3e5f5,stroke:#7b1fa2
    style Standard fill:#f5f5f5,stroke:#9e9e9e,stroke-dasharray: 5 5
      </div>

      <div class="learning-details">
        <div class="learning-row">
          <div class="learning-item">
            <strong>1. Performance Element:</strong> This is the "old" agent (Reflex, Goal, etc.) that decides on actions.
          </div>
          <div class="learning-item">
            <strong>2. Learning Element:</strong> Responsible for making improvements based on feedback.
          </div>
        </div>
        <div class="learning-row">
          <div class="learning-item">
            <strong>3. Critic:</strong> Observes the world and evaluates the agent based on a fixed <strong>Performance Standard</strong>.
          </div>
          <div class="learning-item">
            <strong>4. Problem Generator:</strong> Suggests exploratory actions that will lead to new, informative experiences.
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>5. Summary Comparison</h2>
  <div class="unit">
    <table class="exam-table">
      <thead>
        <tr>
          <th>Agent Type</th>
          <th>Main Feature</th>
          <th>Core Question</th>
          <th>Analogs</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>Simple Reflex</strong></td>
          <td>Condition-Action Rules</td>
          <td>What do I see now?</td>
          <td>Light switch</td>
        </tr>
        <tr>
          <td><strong>Model-Based</strong></td>
          <td>Internal State</td>
          <td>What is the hidden state?</td>
          <td>Driver in fog</td>
        </tr>
        <tr>
          <td><strong>Goal-Based</strong></td>
          <td>Future Planning</td>
          <td>Will this get me there?</td>
          <td>Chess player</td>
        </tr>
        <tr>
          <td><strong>Utility-Based</strong></td>
          <td>Preferences</td>
          <td>How good is this path?</td>
          <td>Travel agent</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<div class="syllabus-section">
  <div class="exam-tip">
    <h4 style="color: #fff; margin-top: 0; margin-bottom: 0.5rem;">Note on Learning Agents</h4>
    Any of these four can be a <strong>Learning Agent</strong>. A "Learning Utility-Based Agent" starts with a basic utility function and learns to prefer different paths based on feedback (e.g., discoverying a road is bumpy and lowering its comfort utility).
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt104co/agent-environment/">← Previous: 2.1 Agents and Environments</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt104co/task-environment/">Next: 2.3 Task Environments →</a>
    </div>
  </div>
  <div style="text-align: center; margin-top: 30px;">
    <a href="/syllabus/bt104co/" class="back-link">Back to Course Syllabus</a>
  </div>
</div>

<style>
.equation-box {
  background: #000;
  color: #fff;
  padding: 1.5rem;
  border-radius: 12px;
  text-align: center;
  font-size: 1.2rem;
  margin-bottom: 1.5rem;
}
.arch-description ul {
  padding-left: 1.2rem;
  margin-bottom: 1rem;
}
.arch-description li {
  margin-bottom: 0.5rem;
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
.architecture-types {
  display: flex;
  flex-direction: column;
  gap: 40px;
  margin-top: 2rem;
}
.arch-section {
  padding: 2rem;
  background: #fff;
  border: 1px solid #e5e7eb;
  border-radius: 20px;
}
.arch-section h3 {
  margin-top: 0;
  margin-bottom: 10px;
}
.arch-section p {
  color: #4b5563;
  font-size: 0.95rem;
  margin-bottom: 20px;
  line-height: 1.5;
}
.arch-details ul {
  padding-left: 1.2rem;
  margin-bottom: 25px;
  font-size: 0.9rem;
  color: #374151;
}
.arch-details li {
  margin-bottom: 8px;
}
.mermaid {
  display: flex;
  justify-content: center;
  background: #fff;
  padding: 1.5rem;
  border-radius: 12px;
  border: 1px solid #f3f4f6;
  margin-top: 1rem;
}

.learning-container {
  background: #f9fafb;
  padding: 2rem;
  border-radius: 20px;
  margin-top: 1.5rem;
}
.learning-details {
  margin-top: 2rem;
}
.learning-row {
  display: flex;
  gap: 20px;
  margin-bottom: 15px;
}
.learning-item {
  flex: 1;
  background: #fff;
  padding: 1.2rem;
  border-radius: 12px;
  border: 1px solid #e5e7eb;
  font-size: 0.9rem;
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
  .learning-row {
    flex-direction: column;
  }
}
</style>
