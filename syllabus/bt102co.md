---
layout: default
title: Digital Logic
course_code: BT102CO
permalink: /syllabus/bt102co/
nav_exclude: true
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <h2>Course Objective</h2>
  <p>The main objective of this course is to familiarize students with the concepts of design and analysis of digital systems and introduce the principles of digital computer organization and design.</p>
</div>

<div class="syllabus-section">
  <h2>Course Contents</h2>
  
  <div class="unit">
    <h3>Unit 1: Number Systems <span class="unit-hours">[5 Hrs]</span></h3>
    <ul>
      <li><a href="/syllabus/bt102co/introduction-analog-digital/">1.1 Introduction: Comparison between analog and digital system</a></li>
      <li><a href="/syllabus/bt102co/number-system-conversion/">1.2 Number system and conversion (Binary, Octal, and Hexadecimal)</a></li>
      <li><a href="/syllabus/bt102co/binary-arithmetic/">1.3 Signed and unsigned numbers, fraction conversion and binary arithmetic</a></li>
      <li><a href="/syllabus/bt102co/binary-codes/">1.4 Representation of Binary coded decimal, gray code, alphanumeric code and error detection and correction codes</a></li>
    </ul>
  </div>

  <div class="unit">
    <h3>Unit 2: Boolean Algebra and Logic Gates <span class="unit-hours">[6 Hrs]</span></h3>
    <ul>
      <li><a href="/syllabus/bt102co/boolean-algebra-theory/">2.1 Introduction to Boolean algebra: Basic theory and properties</a></li>
      <li><a href="/syllabus/bt102co/boolean-functions/">2.2 Boolean functions</a></li>
      <li><a href="/syllabus/bt102co/logic-gates/">2.3 Logic gates and operations</a></li>
    </ul>
  </div>

  <div class="unit">
    <h3>Unit 3: Simplification of Boolean Functions <span class="unit-hours">[6 Hrs]</span></h3>
    <ul>
      <li><a href="/syllabus/bt102co/k-map-simplification/">3.1 K-Map (Two and three variable maps)</a></li>
      <li><a href="/syllabus/bt102co/pos-sop-forms/">3.2 Product of sums, sum of products</a></li>
      <li><a href="/syllabus/bt102co/nand-nor-implementation/">3.3 Simplification of NAND and NOR implementation</a></li>
    </ul>
  </div>

  <div class="unit">
    <h3>Unit 4: Combinational Logic I <span class="unit-hours">[8 Hrs]</span></h3>
    <ul>
      <li><a href="/syllabus/bt102co/adders-subtractors/">4.1 Design procedure of Adders and Subtractors</a></li>
      <li><a href="/syllabus/bt102co/code-conversion/">4.2 Code conversion, Analysis procedure</a></li>
      <li><a href="/syllabus/bt102co/multilevel-nand-nor/">4.3 Multilevel NAND and NOR gates</a></li>
    </ul>
  </div>

  <div class="unit">
    <h3>Unit 5: Combinational Logic II <span class="unit-hours">[8 Hrs]</span></h3>
    <ul>
      <li><a href="/syllabus/bt102co/parallel-decimal-adder/">5.1 Binary parallel adder and Decimal adder</a></li>
      <li><a href="/syllabus/bt102co/magnitude-comparator/">5.2 Magnitude comparator</a></li>
      <li><a href="/syllabus/bt102co/decoders-multiplexers/">5.3 Decoders and Multiplexers</a></li>
      <li><a href="/syllabus/bt102co/rom-pla/">5.4 Read only memory and Programmable logic array (PLA)</a></li>
    </ul>
  </div>

  <div class="unit">
    <h3>Unit 6: Sequential Logic <span class="unit-hours">[6 Hrs]</span></h3>
    <ul>
      <li><a href="/syllabus/bt102co/sequential-vs-combinational/">6.1 Difference between sequential and combinational circuit</a></li>
      <li><a href="/syllabus/bt102co/flip-flops/">6.2 Introduction and Design procedure of RS, JK, T, D and master-slave flip flops</a></li>
      <li><a href="/syllabus/bt102co/sequential-design/">6.3 Design with state equation and state reduction table</a></li>
    </ul>
  </div>

  <div class="unit">
    <h3>Unit 7: Registers and Counters <span class="unit-hours">[6 Hrs]</span></h3>
    <ul>
      <li><a href="/syllabus/bt102co/registers/">7.1 Left and right shift registers (SISO, SIPO, PISO, PIPO)</a></li>
      <li><a href="/syllabus/bt102co/counters/">7.2 Asynchronous and Synchronous counters (Up/Down, Decade, Ring)</a></li>
      <li><a href="/syllabus/bt102co/counter-applications/">7.3 Application of counters</a></li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>Examination Scheme</h2>
  <table class="exam-table">
    <thead>
      <tr>
        <th colspan="3">Teaching Schedule</th>
        <th colspan="4">Examination Scheme</th>
        <th rowspan="2">Total</th>
      </tr>
      <tr>
        <th>TH</th>
        <th>TU</th>
        <th>PR</th>
        <th colspan="2">Internal</th>
        <th colspan="2">Final</th>
      </tr>
      <tr>
        <th></th>
        <th></th>
        <th></th>
        <th>TH</th>
        <th>PR</th>
        <th>TH</th>
        <th>PR</th>
        <th></th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>3</td>
        <td>1</td>
        <td>2</td>
        <td>20</td>
        <td>20</td>
        <td>60</td>
        <td>-</td>
        <td>100</td>
      </tr>
    </tbody>
  </table>
</div>

<div class="syllabus-section">
  <h2>Laboratory Work</h2>
  <ol>
    <li>Familiarization with logic gates</li>
    <li>De Morgan’s law</li>
    <li>Multiplexer and de-multiplexer</li>
    <li>Encoder and decoder</li>
    <li>Half adder and half subtractor</li>
    <li>Full adder and full subtractor</li>
    <li>RS, JK, T, D and master slave flip flops</li>
    <li>Shift registers, Sequential logic</li>
    <li>Ripple counters and synchronous counters</li>
    <li>Simulation using suitable software</li>
  </ol>
</div>

<div class="syllabus-section">
  <h2>Reference Books</h2>
  <ol>
    <li>Floyd T. L & Jain R. P, “Digital Fundamentals”, 8th edition</li>
    <li>Morris Mano, “Logic & Computer Design Fundamentals”, Pearson education</li>
    <li>William I, Fletcher, “An Engineering Approach to Digital Design”, Prentice Hall of India, New Delhi, 1990</li>
    <li>A.P. Malvino & Jerald A. Brown, “Digital Computer Electronics”, 1995</li>
    <li>D. D. Hodegs & H.G. Jackson, “Analysis & Design of Digital Integrated Circuits”, McGraw Hill, New York, 1983</li>
  </ol>
</div>
