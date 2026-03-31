---
layout: default
title: 1.3 Downloading and Installing Python
course_code: BT101CO
permalink: /syllabus/bt101co/installing-python/
---

<div class="syllabus-header">
  <h1>{{ page.title }} <small>({{ page.course_code }})</small></h1>
</div>

<div class="syllabus-section">
  <p class="intro-note"><strong>Note:</strong> This guide covers the syllabus requirements for <em>1.3 Downloading and Installing Python</em> and <em>1.4 Running Python</em>, plus additional modern tools like IDEs to give you a head start.</p>
  <p>Setting up Python in 2026 is smoother than ever, thanks to improved installers and development tools. Below is the guide for your cross-platform journey.</p>
</div>

<div class="syllabus-section">
  <h2>1. Installing Python (The Core)</h2>
  
  <div class="unit">
    <h3>Windows</h3>
    <ol>
      <li><strong>Download:</strong> Go to <a href="https://www.python.org/downloads/windows/">python.org</a>.</li>
      <li><strong>Crucial Step:</strong> Run the <code>.exe</code> and <strong>check the box</strong> that says <strong>"Add Python to PATH"</strong>. If you miss this, your CLI won't recognize the <code>python</code> command.</li>
      <li><strong>Install:</strong> Select "Install Now."</li>
      <li><strong>Verify:</strong> Open PowerShell and type <code>python --version</code>.</li>
    </ol>
  </div>

  <div class="unit">
    <h3>macOS</h3>
    <p>While macOS comes with a version of Python, it’s usually outdated.</p>
    <ol>
      <li><strong>Homebrew (Recommended):</strong> Open Terminal and type:<br><code>brew install python</code></li>
      <li><strong>Official Installer:</strong> Alternatively, download the macOS 64-bit universal2 installer from python.org.</li>
      <li><strong>Verify:</strong> Type <code>python3 --version</code> in Terminal.</li>
    </ol>
  </div>

  <div class="unit">
    <h3>Linux (Ubuntu/Debian)</h3>
    <p>Python is usually pre-installed. To update or install:</p>
    <ol>
      <li><strong>Update:</strong> <code>sudo apt update</code></li>
      <li><strong>Install:</strong> <code>sudo apt install python3</code></li>
      <li><strong>Verify:</strong> Type <code>python3 --version</code>.</li>
    </ol>
  </div>
</div>

<div class="syllabus-section">
  <h2>2. The CLI (Command Line Interface)</h2>
  <p>The CLI is your direct line to Python.</p>
  <div class="unit">
    <ul>
      <li><strong>REPL:</strong> Type <code>python</code> (Windows) or <code>python3</code> (Mac/Linux) to enter the interactive shell. You'll see <code>>>></code>, where you can run code line-by-line.</li>
      <li><strong>Running Files:</strong> Navigate to your folder and type <code>python myscript.py</code>.</li>
      <li><strong>Pip:</strong> This is Python's package manager. Use it to install libraries: <code>pip install requests</code>.</li>
    </ul>
  </div>
</div>

<div class="syllabus-section">
  <h2>3. IDEs and VS Code</h2>
  <div class="unit">
    <h3>Visual Studio Code (The Standard)</h3>
    <ol>
      <li><strong>Install:</strong> Download from <a href="https://code.visualstudio.com/">code.visualstudio.com</a>.</li>
      <li><strong>Python Extension:</strong> Click the Extensions icon (square blocks) and search for <strong>"Python" by Microsoft</strong>.</li>
      <li><strong>Interpreter Selection:</strong> Press <code>Ctrl+Shift+P</code>, type "Python: Select Interpreter," and pick the version you just installed.</li>
      <li><strong>Extras:</strong> VS Code now features <strong>GitHub Copilot Native</strong>, allowing for real-time code generation and refactoring.</li>
    </ol>
  </div>
  <div class="unit">
    <h3>Future Note: Antigravity</h3>
    <p>For those looking for an "agent-first" experience, Google’s <strong>Antigravity</strong> platform (released recently) offers an environment where AI agents help plan and execute code autonomously, changing the role of a programmer to an Architect.</p>
  </div>
</div>

<div class="syllabus-section">
  <h2>Summary Table</h2>
  <table class="exam-table">
    <thead>
      <tr>
        <th>Feature</th>
        <th>Windows</th>
        <th>macOS</th>
        <th>Linux</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><strong>Primary Tool</strong></td>
        <td>Official <code>.exe</code></td>
        <td>Homebrew</td>
        <td><code>apt</code> or <code>dnf</code></td>
      </tr>
      <tr>
        <td><strong>CLI Command</strong></td>
        <td><code>python</code></td>
        <td><code>python3</code></td>
        <td><code>python3</code></td>
      </tr>
      <tr>
        <td><strong>Path Setup</strong></td>
        <td>Manual Checkbox</td>
        <td>Automatic (Brew)</td>
        <td>Automatic</td>
      </tr>
    </tbody>
  </table>
</div>

<div class="syllabus-section" style="margin-top: 50px;">
  <div class="topic-navigation">
    <div class="prev-topic">
      <a href="/syllabus/bt101co/history-of-python/">← Previous: 1.2 History of Python</a>
    </div>
    <div class="next-topic">
      <a href="/syllabus/bt101co/documentation/">Next: 1.5 Python Documentation →</a>
    </div>
  </div>
  <div style="text-align: center; margin-top: 30px;">
    <a href="/syllabus/bt101co/" class="back-link">Back to Course Syllabus</a>
  </div>
</div>

<style>
.intro-note {
  background: #fcfcfc;
  border: 1px solid var(--border-color);
  padding: 15px;
  border-radius: 6px;
  font-size: 0.95rem;
  margin-bottom: 25px;
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
