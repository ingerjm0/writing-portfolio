# Developer Documentation

Developer documentation meets the developer where they are, providing language-specific guidance, API references, and code samples to illustrate an API usage. Whether its developing a developer's quick start guide, a detailed API reference, example code snippets, or walk-through tutorials, I've enjoyed working with programmers in many different languages.

Click below to view samples of developer documentation that I've worked on in my career:

<table style="float:auto; border:none;">
  <tr>
    <td>
      <figure>
        <a href="#sample-1---high-fidelity-online-docs"><img src="api-ref.png" width="250px" />
          <figcaption style="font-style:italic; text-align:center;">API Reference generated with JSDoc</figcaption></a>
      </figure>
      </td>
    <td>
      <figure>
        <a href="#sample-3---javascript-quick-start"><img src="quick-start.png" width="250px" />
        <figcaption style="font-style:italic; text-align:center;">JavaScript Quick Start</figcaption></a>
      </figure>
    </td>
  </tr>
  <tr>
    <td>
      <figure>
        <a href="#sample-3---javascript-quick-start"><img src="quick-start.png" width="250px" />
        <figcaption style="font-style:italic; text-align:center;">JavaScript Quick Start</figcaption></a>
      </figure>
      </td>
    <td>
      <figure>
        <a href="#sample-4---getting-started-guide-xml"><img src="xml-script.png" width="250px" />
        <figcaption style="font-style:italic; text-align:center;">Getting Started Guide for XML</figcaption></a>
      </figure>
    </td>
  </tr>
</table>

## Sample 1 - High Fidelity API Reference 

**Tools Used:** JavaScript, JSDoc, GitHub Pages, Markdown, HTML, CSS

Prior to joining High Fidelity, the API reference guide was using JSDoc to generate the API documentation; however, the content was extracted from the output files and merged with Markdown template files uisng a custom JavaScript. The custom script required constant maintenance, and the process of creating files, merging them, then re-creating them was a definitive source of inefficiency. 

After ensuring that I understood the existing architecture, I recommended and proposed a plan to migrate entirely to JSDoc for documentation generation and formatting, and use GitHub Pages to host the generated pages. This removed the dependency on multiple tools working together, and increased the control we had over branding, design, and implementation. 

The High Fidelity JavaScript API lets content creators and developers create new experiences and transform virtual worlds within the High Fidelity metaverse. 

[View the API reference here](api/index.html). 

<hr style="margin-left:auto; margin-right:auto; width:75%;" />

## Sample 3 - JavaScript Quick Start

**Tools Used:** JavaScript, HTML, CSS

This quick start was developed to help new scripters get acquainted with JavaScript for the first time, specifically when scripting with High Fidelity. It answers the questions: 

* What is JavaScript?
* How do I use JavaScript with High Fidelity?
* What are some things I can do with scripting?
* Where can I learn more about scripting?

### Sample Chapters

* [Getting Started with JavaScript](scripting.html)
* [Write Your Own Scripts](write-scripts.html)

<hr style="margin-left:auto; margin-right:auto; width:75%;" />

## Sample 4 - Getting Started Guide (XML)

**Tools Used:** MadCap Flare, Perforce, XML, HTML, CSS

This quick start guides walks IT professionals through integrating BarTender software ([https://www.seagullscientific.com](seagullscientific.com)) with other applications with BarTender XML Script. Specifically, the BTXML schema provides a way to pass print job data from an external interface directly to BarTender. An XML response message, which contains data that can be used to verify the completion of the job, is automatically created each time a script is received.

Throughout the years, this content has been adopted into many deliverable formats: an introduction to an online help system, a technical white paper, and a BTXML reference guide. 

### Sample Chapters

* [Setting Up BTXML to Run with Your Application](get-started.html)
* [Using the XML Response](response.html)
