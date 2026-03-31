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
          <h3>Semester I <span class="credits-badge">16 Total Credits</span></h3>
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
              <a href="#">Old Questions</a>
            </div>
          </div>
          <div class="subject-item">
            <div class="subject-info">
              <h4>Digital Logic</h4>
              <span class="subject-credits">3 Credits</span>
            </div>
            <div class="subject-links">
              <a href="#">Syllabus</a>
              <a href="#">Old Questions</a>
            </div>
          </div>
          <div class="subject-item">
            <div class="subject-info">
              <h4>Calculus</h4>
              <span class="subject-credits">3 Credits</span>
            </div>
            <div class="subject-links">
              <a href="#">Syllabus</a>
              <a href="#">Old Questions</a>
            </div>
          </div>
          <div class="subject-item">
            <div class="subject-info">
              <h4>Introduction to Artificial Intelligence</h4>
              <span class="subject-credits">3 Credits</span>
            </div>
            <div class="subject-links">
              <a href="#">Syllabus</a>
              <a href="#">Old Questions</a>
            </div>
          </div>
          <div class="subject-item">
            <div class="subject-info">
              <h4>Technical Report Writing & Presentation</h4>
              <span class="subject-credits">2 Credits</span>
            </div>
            <div class="subject-links">
              <a href="#">Syllabus</a>
              <a href="#">Old Questions</a>
            </div>
          </div>
          <div class="subject-item">
            <div class="subject-info">
              <h4>Society & Professional Ethics</h4>
              <span class="subject-credits">2 Credits</span>
            </div>
            <div class="subject-links">
              <a href="#">Syllabus</a>
              <a href="#">Old Questions</a>
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
