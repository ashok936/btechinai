---
layout: default
title: "1.5 Applications of AI"
course_code: BT104CO
permalink: /syllabus/bt104co/applications-of-ai/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <h2>1. Major Domains of Application</h2>
  <div class="unit">
    <p>AI has transitioned from lab experiments to ubiquitous technology, powering systems that solve real-world problems through rational action.</p>

    <div class="applications-grid">
      <div class="app-card">
        <div class="app-tag">Automotive</div>
        <h4>A. Robotic Vehicles</h4>
        <p>The most visible application of the <strong>Rational Agent</strong> model. Involves high-speed sensor fusion and real-time path planning.</p>
        <ul class="app-list">
          <li><strong>Examples:</strong> Self-driving cars (Tesla, Waymo), Mars Rovers.</li>
        </ul>
      </div>

      <div class="app-card">
        <div class="app-tag">Communication</div>
        <h4>B. NLP & Speech</h4>
        <p>Interacting with machines using human language by understanding syntax, semantics, and context.</p>
        <ul class="app-list">
          <li><strong>Examples:</strong> Virtual assistants (Siri, Alexa), LLMs (ChatGPT).</li>
        </ul>
      </div>

      <div class="app-card">
        <div class="app-tag">Strategy</div>
        <h4>C. Games & Planning</h4>
        <p>Searching massive state spaces and using <strong>Heuristics</strong> to evaluate optimal board positions.</p>
        <ul class="app-list">
          <li><strong>Examples:</strong> Deep Blue (Chess), AlphaGo (Go).</li>
        </ul>
      </div>

      <div class="app-card">
        <div class="app-tag">Healthcare</div>
        <h4>D. Medicine</h4>
        <p>AI acting as an expert assistant for pattern recognition and high-precision classification in diagnosis.</p>
        <ul class="app-list">
          <li><strong>Examples:</strong> Tumor detection (MRIs), AlphaFold (Proteins).</li>
        </ul>
      </div>

      <div class="app-card">
        <div class="app-tag">Enterprise</div>
        <h4>E. Finance & E-commerce</h4>
        <p>Using probabilistic reasoning and anomaly detection to predict human behavior and market trends.</p>
        <ul class="app-list">
          <li><strong>Examples:</strong> Fraud detection, Recommendation engines.</li>
        </ul>
      </div>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. Classification by Function</h2>
  <div class="unit">
    <p>In the context of exams, applications can be classified by the <strong>type of cognitive task</strong> they perform:</p>
    <table class="exam-table">
      <thead>
        <tr>
          <th>Category</th>
          <th>Description</th>
          <th>Example</th>
        </tr>
      </thead>
      <tbody>
        <tr><td><strong>Perception</strong></td><td>Interpreting binary sensory data.</td><td>Facial recognition, OCR.</td></tr>
        <tr><td><strong>Reasoning</strong></td><td>Drawing logical conclusions.</td><td>Legal research, diagnostic systems.</td></tr>
        <tr><td><strong>Planning</strong></td><td>Sequencing actions to reach a goal.</td><td>Supply chain optimization.</td></tr>
        <tr><td><strong>Learning</strong></td><td>Improving based on experience.</td><td>Spam filters, personalized ads.</td></tr>
      </tbody>
    </table>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. The "AI Effect" (A Key Concept)</h2>
  <div class="unit">
    <div class="ai-effect-box">
      <h4>The Paradox of Success</h4>
      <p>Russell and Norvig note that <strong>"as soon as an AI technique becomes common enough, it is no longer called AI."</strong> This is known as the <em>AI Effect</em>. Optical Character Recognition (OCR) was once considered miraculous AI; today it is standard computation. "AI" often defines whatever hasn't been done yet.</p>
    </div>
  </div>
</div>

<div class="syllabus-section">
  <h2>4. Historical Milestones (Exam Prep)</h2>
  <div class="milestones-row">
    <div class="milestone-pill"><strong>AlphaGo (2016):</strong> Defeated World Champion Lee Sedol.</div>
    <div class="milestone-pill"><strong>Watson (2011):</strong> Won Jeopardy! against humans.</div>
    <div class="milestone-pill"><strong>Deep Blue (1997):</strong> Defeated Kasparov in Chess.</div>
  </div>
</div>

<div class="syllabus-section">
  <div class="exam-tip">
    <h4 style="color: #fff; margin-top: 0; margin-bottom: 0.5rem;">Exam Tip</h4>
    When writing about applications, connect them to the <strong>PEAS</strong> framework. For a self-driving car, mention its <strong>Sensors</strong> (Cameras) and <strong>Actuators</strong> (Steering/Brakes).
  </div>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt104co/goals-challenges-ai/">← Previous: 1.4 Goals and Challenges</a>
    </div>
    <div class="next-topic">
       <a href="/syllabus/bt104co/agent-environment/">Next: 2.1 Agent & Environment →</a>
    </div>
  </div>
  <div style="text-align: center; margin-top: 30px;">
    <a href="/syllabus/bt104co/" class="back-link">Back to Course Syllabus</a>
  </div>
</div>

<style>
.applications-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px;
  margin-top: 25px;
}
.app-card {
  padding: 24px;
  background: #fff;
  border: 1px solid #e5e7eb;
  border-radius: 16px;
  transition: all 0.3s ease;
}
.app-card:hover {
  transform: translateY(-5px);
  border-color: #000;
  box-shadow: 0 10px 25px -5px rgba(0,0,0,0.05);
}
.app-tag {
  display: inline-block;
  font-size: 0.65rem;
  font-weight: 800;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  padding: 4px 10px;
  background: #f3f4f6;
  border-radius: 20px;
  margin-bottom: 15px;
  color: #4b5563;
}
.app-card h4 {
  margin: 0 0 10px 0;
  font-size: 1.1rem;
}
.app-card p {
  font-size: 0.9rem;
  line-height: 1.5;
  color: #374151;
  margin-bottom: 12px;
}
.app-list {
  padding: 0;
  margin: 0;
  list-style: none;
  font-size: 0.85rem;
  color: #6b7280;
}
.ai-effect-box {
  padding: 30px;
  background: #f9fafb;
  border-radius: 20px;
  border-left: 5px solid #000;
}
.ai-effect-box h4 {
  margin-top: 0;
  margin-bottom: 10px;
}
.ai-effect-box p {
  margin: 0;
  line-height: 1.6;
  color: #4b5563;
}
.milestones-row {
  display: flex;
  flex-wrap: wrap;
  gap: 15px;
  margin-top: 15px;
}
.milestone-pill {
  padding: 12px 20px;
  background: #fff;
  border: 1px solid #f3f4f6;
  border-radius: 100px;
  font-size: 0.9rem;
  color: #374151;
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
