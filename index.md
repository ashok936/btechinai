---
layout: default
---

<div class="wrapper">
  <div class="curriculum-container">
    <div class="semester-tabs">
      <button class="tab-btn active" onclick="openSemester(event, 'sem1')">1st Sem</button>
      <button class="tab-btn" onclick="openSemester(event, 'sem2')">2nd Sem</button>
      <button class="tab-btn" onclick="openSemester(event, 'sem3')">3rd Sem</button>
      <button class="tab-btn" onclick="openSemester(event, 'sem4')">4th Sem</button>
      <button class="tab-btn" onclick="openSemester(event, 'sem5')">5th Sem</button>
      <button class="tab-btn" onclick="openSemester(event, 'sem6')">6th Sem</button>
      <button class="tab-btn" onclick="openSemester(event, 'sem7')">7th Sem</button>
      <button class="tab-btn" onclick="openSemester(event, 'sem8')">8th Sem</button>
    </div>

    <div class="semester-panels">
      <!-- Semester 1 -->
      <div id="sem1" class="semester-panel active">
        <div class="semester-header">
          <h3>Semester I <span class="credits-badge">18 Total Credits</span></h3>
        </div>
        <div class="subject-list">
          <div class="subject-item">
            <div class="subject-info">
              <h4><a href="{{ "/syllabus/bt101co/" | relative_url }}">Introduction to Programming</a></h4>
              <span class="subject-credits">3 Credits</span>
            </div>
            <p class="subject-desc">Fundamental programming concepts and problem-solving techniques using modern programming languages.</p>
            <div class="subject-links">
              <a href="{{ "/syllabus/bt101co/" | relative_url }}">Syllabus</a>
              <a href="{{ "/syllabus/bt101co/#old-questions" | relative_url }}">Old Questions</a>
            </div>
          </div>
          <div class="subject-item">
            <div class="subject-info">
              <h4><a href="{{ "/syllabus/bt102co/" | relative_url }}">Digital Logic</a></h4>
              <span class="subject-credits">3 Credits</span>
            </div>
            <p class="subject-desc">Foundational principles of digital system design, Boolean algebra, logic gates, and sequential circuits.</p>
            <div class="subject-links">
              <a href="{{ "/syllabus/bt102co/" | relative_url }}">Syllabus</a>
              <a href="{{ "/syllabus/bt102co/#old-questions" | relative_url }}">Old Questions</a>
            </div>
          </div>
          <div class="subject-item">
            <div class="subject-info">
              <h4><a href="{{ "/syllabus/bt103hs/" | relative_url }}">Calculus</a></h4>
              <span class="subject-credits">3 Credits</span>
            </div>
            <p class="subject-desc">Comprehensive study of differential and integral calculus with applications in engineering.</p>
            <div class="subject-links">
              <a href="{{ "/syllabus/bt103hs/" | relative_url }}">Syllabus</a>
              <a href="{{ "/syllabus/bt103hs/#old-questions" | relative_url }}">Old Questions</a>
            </div>
          </div>
          <div class="subject-item">
            <div class="subject-info">
              <h4><a href="{{ "/syllabus/bt104co/" | relative_url }}">Introduction to Artificial Intelligence</a></h4>
              <span class="subject-credits">3 Credits</span>
            </div>
            <p class="subject-desc">Conceptual understanding of AI systems, agents, search strategies, and knowledge representation.</p>
            <div class="subject-links">
              <a href="{{ "/syllabus/bt104co/" | relative_url }}">Syllabus</a>
              <a href="{{ "/syllabus/bt104co/#old-questions" | relative_url }}">Old Questions</a>
            </div>
          </div>
          <div class="subject-item">
            <div class="subject-info">
              <h4><a href="{{ "/syllabus/bt105hs/" | relative_url }}">Technical Report Writing & Presentation</a></h4>
              <span class="subject-credits">3 Credits</span>
            </div>
            <p class="subject-desc">Developing linguistic competence, English language skills for technical communication, and effective presentation techniques.</p>
            <div class="subject-links">
              <a href="{{ "/syllabus/bt105hs/" | relative_url }}">Syllabus</a>
              <a href="{{ "/syllabus/bt105hs/#old-questions" | relative_url }}">Old Questions</a>
            </div>
          </div>
          <div class="subject-item">
            <div class="subject-info">
              <h4><a href="{{ "/syllabus/bt106hs/" | relative_url }}">Sociology and Professional Ethics</a></h4>
              <span class="subject-credits">3 Credits</span>
            </div>
            <p class="subject-desc">Exploration of social dynamics, cultural change, ethical issues in IT, and emotional intelligence.</p>
            <div class="subject-links">
              <a href="{{ "/syllabus/bt106hs/" | relative_url }}">Syllabus</a>
              <a href="{{ "/syllabus/bt106hs/#old-questions" | relative_url }}">Old Questions</a>
            </div>
          </div>
        </div>
      </div>

      <!-- Semester 2 -->
      <div id="sem2" class="semester-panel">
        <div class="semester-header">
          <h3>Semester II <span class="credits-badge">14 Total Credits</span></h3>
        </div>
        <div class="subject-list">
          <div class="subject-item">
            <div class="subject-info">
              <h4>Object Oriented Programming</h4>
              <span class="subject-credits">3 Credits</span>
            </div>
            <div class="subject-links">
              <a href="#">Syllabus</a>
              <a href="#">Old Questions</a>
            </div>
          </div>
          <div class="subject-item">
            <div class="subject-info">
              <h4>Artificial Intelligence & Intelligent Systems</h4>
              <span class="subject-credits">3 Credits</span>
            </div>
            <div class="subject-links">
              <a href="#">Syllabus</a>
              <a href="#">Old Questions</a>
            </div>
          </div>
          <div class="subject-item">
            <div class="subject-info">
              <h4>Microprocessor & Assembly Language</h4>
              <span class="subject-credits">3 Credits</span>
            </div>
            <div class="subject-links">
              <a href="#">Syllabus</a>
              <a href="#">Old Questions</a>
            </div>
          </div>
          <div class="subject-item">
            <div class="subject-info">
              <h4>Linear Algebra & Statistics</h4>
              <span class="subject-credits">3 Credits</span>
            </div>
            <div class="subject-links">
              <a href="#">Syllabus</a>
              <a href="#">Old Questions</a>
            </div>
          </div>
          <div class="subject-item">
            <div class="subject-info">
              <h4>Project I</h4>
              <span class="subject-credits">2 Credits</span>
            </div>
            <div class="subject-links">
              <a href="#">Syllabus</a>
              <a href="#">Old Questions</a>
            </div>
          </div>
        </div>
      </div>

      <!-- Placeholders for Sem 3-8 -->
      {% for i in (3..8) %}
        <div id="sem{{i}}" class="semester-panel">
          <div class="semester-header">
            <h3>Semester {{ i }} <span class="credits-badge">TBD</span></h3>
          </div>
          <p>Curriculum data for Semester {{ i }} will be updated soon.</p>
        </div>
      {% endfor %}
    </div>
  </div>

  <script>
    function openSemester(evt, semId) {
      if (!evt || !semId) return;
      var i, panels, tablinks;
      panels = document.getElementsByClassName("semester-panel");
      for (i = 0; i < panels.length; i++) {
        panels[i].className = panels[i].className.replace(" active", "");
      }
      tablinks = document.getElementsByClassName("tab-btn");
      for (i = 0; i < tablinks.length; i++) {
        tablinks[i].className = tablinks[i].className.replace(" active", "");
      }
      var targetPanel = document.getElementById(semId);
      if (targetPanel) targetPanel.className += " active";
      if (evt.currentTarget) evt.currentTarget.className += " active";
    }
  </script>
</div>
