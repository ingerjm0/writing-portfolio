# Developer Documentation

Developer documentation meets the developer where they are, providing language-specific guidance, API references, and code samples to illustrate an API usage. Whether its developing a developer's quick start guide, a detailed API reference, example code snippets, or walk-through tutorials, I've enjoyed working with programmers in many different languages.

# Samples of Developer Documentation

<div style="width:100%; background:aliceblue; padding:25px;">

<h2>High Fidelity API Reference</h2>

<p>
  <figure style="float:right;">
    <a href="api/index.html"><img src="api-ref.png" width="400px" />
      <figcaption style="font-style:italic; text-align:center;">API Reference generated with JSDoc</figcaption></a>
  </figure>
  <strong>Tools Used:</strong> JavaScript, JSDoc, GitHub Pages, Markdown, HTML, CSS</p>

<p>Prior to joining High Fidelity, the API reference guide was using JSDoc to generate the API documentation; however, the content was extracted from the output files and merged with Markdown template files uisng a custom JavaScript. The custom script required constant maintenance, and the process of creating files, merging them, then re-creating them was a definitive source of inefficiency. </p>

<p>After ensuring that I understood the existing architecture, I recommended and proposed a plan to migrate entirely to JSDoc for documentation generation and formatting, and use GitHub Pages to host the generated pages. This removed the dependency on multiple tools working together, and increased the control we had over branding, design, and implementation. </p>

<p>View the API reference here: <a href="api/index.html">https://ingerjm0.github.io/writing-portfolio/dev/api/index.html</a>.</p>

</div>

<div style="width:100%; background:lightgray; padding:25px;">

<h2>JavaScript Quick Start</h2>

<p>
  <figure style="float:right;">
    <img src="quick-start.png" width="400px" />
      <figcaption style="font-style:italic; text-align:center;">JavaScript Quick Start Guide</figcaption>
  </figure>
  <strong>Tools Used:</strong> JavaScript, HTML, CSS</p>

<p>This quick start was developed to help new scripters get acquainted with JavaScript for the first time, specifically when scripting with High Fidelity. It answers the questions: </p>

<ul>
  <li>What is JavaScript?</li>
  <li>How do I use JavaScript with High Fidelity?</li>
  <li>What are some things I can do with scripting?</li>
  <li>Where can I learn more about scripting?</li>
</ul>

<h3>Sample Chapters</h3>

<ul>
  <li><a href="scripting.html">Getting Started with JavaScript</a></li>
  <li><a href="write-scripts.html">Write Your Own Scripts</a></li>
</ul>

</div>

<div style="width:100%; background:aliceblue; padding:25px;">

<h2>Getting Started Guide (XML)</h2>

<p>
  <figure style="float:right;">
    <img src="xml-script.png" width="400px" />
      <figcaption style="font-style:italic; text-align:center;">Getting Started Guide for XML</figcaption>
  </figure>
  <strong>Tools Used:</strong> MadCap Flare, Perforce, XML, HTML, CSS</p>

<p>This quick start guides walks IT professionals through integrating <a href="https://www.seagullscientific.com">BarTender software</a> with other applications with BarTender XML Script. Specifically, the BTXML schema provides a way to pass print job data from an external interface directly to BarTender. An XML response message, which contains data that can be used to verify the completion of the job, is automatically created each time a script is received.</p>

<p>Throughout the years, this content has been adopted into many deliverable formats: an introduction to an online help system, a technical white paper, and a BTXML reference guide. </p>

<p>I'd love to be able to share the entire project with you, but unfortunately, it is not in the public domain. Please contact me for any questions; I'd be happy to discuss in detail my role in this project!</p>

</div>

<div style="width:100%; background:lightgray; padding:25px;">

<h2>Tutorial: Create a Portal with High Fidelity</h2>

<p>
  <figure style="float:right;">
    <img src="portal-tutorial.png" width="400px" />
      <figcaption style="font-style:italic; text-align:center;">Tutorial: Create a Portal</figcaption>
  </figure>
  <strong>Tools Used:</strong> High Fidelity, JavaScript, JSDoc, Markdown, GitHub Pages</p>

<p>For this project, I developed a tutorial that instructed our users how to achieve advanced functionality with High Fidelity's open source platform using scripting. Specifically, this tutorial walks someone through the creation of an object, then scripts its behavior to transport an avatar to another location in the metaverse. </p>
<p>The entire goal of this project (and its accompanying tutorials) is to educate users on the immense functionality that the JavaScript API provides. Here, I break down an advanced feature to its simplest parts so that creators with basic scripting knowledge can learn from the samples and develop their own functionality through scripting.</p>
</div>
