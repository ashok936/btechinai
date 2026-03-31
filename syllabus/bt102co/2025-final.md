---
layout: default
title: Digital Logic - Old Question 2025
course_code: BT102CO
permalink: /syllabus/bt102co/questions/2025/
nav_exclude: true
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
  <a href="/syllabus/bt102co/" class="back-link">← Back to Syllabus</a>
</div>

<div class="question-paper">
  <div class="paper-header">
    <p><strong>Purbanchal University</strong></p>
    <p><strong>2025</strong></p>
    <p><strong>Bachelor of Technology in Artificial Intelligence/First Semester/Final</strong></p>
    <div class="marks-info">
      <span>Time: 03:00 hrs.</span>
      <span>Full Marks: 60/Pass Marks: 24</span>
    </div>
    <p><strong>BT102CO: Digital Logic</strong></p>
  </div>

  <hr>

  <p><em>Candidates are required to give their answers in their own words as far as practicable.</em></p>
  <p><em>Figure in the margin indicate full marks.</em></p>

  <hr>

  <div class="group">
    <h3>Group A</h3>
    <div class="group-info">
      <span>Answer TWO questions.</span>
      <span>2 × 12 = 24</span>
    </div>

    <div class="question">
      <p><strong>1.</strong> What is a counter? Explain different types of counter. Discuss synchronous counter with a timing diagram. <span class="marks">[2+4+6]</span></p>
    </div>

    <div class="question">
      <p><strong>2.</strong> Explain the role of multilevel NAND and NOR gates in implementing combinational logic circuits and provide a detailed analysis of the circuit's operation. <span class="marks">[12]</span></p>
    </div>

    <div class="question">
      <p><strong>3. (a)</strong> What is a K-map? Explain the don't care condition in K-map with an example. <span class="marks">[6]</span></p>
      <p><strong>3. (b)</strong> Simplify the following using K-map: <span class="marks">[6]</span></p>
      <ul>
        <li>$F(A, B, C, D) = \Sigma(0, 2, 4, 7, 10, 12)$</li>
        <li>$d(A, B, C, D) = \Sigma(1, 3, 5, 6, 8)$</li>
      </ul>
    </div>
  </div>

  <hr>

  <div class="group">
    <h3>Group B</h3>
    <div class="group-info">
      <span>Answer SIX questions.</span>
      <span>6 × 6 = 36</span>
    </div>

    <div class="question">
      <p><strong>4.</strong> Explain the difference between analog and digital signals. Give real-world examples of each. Why are digital signals preferred in modern electronics? <span class="marks">[6]</span></p>
    </div>

    <div class="question">
      <p><strong>5.</strong> Perform the following: <span class="marks">[2+2+2]</span></p>
      <ul>
        <li><strong>(a)</strong> Subtract $(873)_{10}$ from $(3462)_{10}$ using the 10's complement method.</li>
        <li><strong>(b)</strong> $(2312)_{4} = (?)_{3}$</li>
        <li><strong>(c)</strong> $(32689)_{10} = (?)_{2}$</li>
      </ul>
    </div>

    <div class="question">
      <p><strong>6.</strong> What is a combinational logic circuit? Explain a 4:1 multiplexer with a neat diagram. <span class="marks">[6]</span></p>
    </div>

    <div class="question">
      <p><strong>7.</strong> Analyze the given logic circuit. Determine the output expression and simplify it (if possible). Construct the truth table for the circuit. <span class="marks">[6]</span></p>
      
      <div class="mermaid">
      graph LR
          subgraph Inputs
          A[A]
          B[B]
          C[C]
          D[D]
          end

          A --- NOR((NOR))
          B --- NOR

          C --- NOT((NOT))

          C --- OR((OR))
          D --- OR

          NOR --- AND{AND}
          NOT --- AND
          OR --- AND

          AND --- OUT[Output]
      </div>
    </div>

    <div class="question">
      <p><strong>8.</strong> Design a sequential circuit using T flip-flops to implement a 3-bit counter that counts in the sequence $000 \rightarrow 001 \rightarrow 010 \rightarrow 100$ (repeating). Include the state diagram and state equations in your design. <span class="marks">[6]</span></p>
    </div>

    <div class="question">
      <p><strong>9.</strong> What is a Programmable Logic Array (PLA), and how does it differ from a ROM? Explain different types of ROMs. <span class="marks">[6]</span></p>
    </div>

    <div class="question">
      <p><strong>10.</strong> What is a flip-flop? Explain JK-flip-flop with an example. <span class="marks">[6]</span></p>
    </div>
  </div>
</div>

<style>
.back-link {
  display: inline-block;
  margin-top: 10px;
  text-decoration: none;
  font-size: 0.9rem;
  color: var(--text-muted);
}
.back-link:hover {
  color: var(--text-main);
}
</style>
