# Getting Started Guide (XML) - Sample Chapter 1

[Return to Getting Started Guide (XML)](overview.html)

---

## Automation with BTXML Script

BarTender XML (BTXML) script is a pre-written Extensible Markup Language (XML) schema that was created specifically to work together with BarTender. (XML is a markup language that defines a set of rules for encoding documents in a format that is both human-readable and machine-readable.) You can use BTXML script to control and automate BarTender and print jobs, and you can send BTXML script to your external software applications to run BarTender and print jobs. Third-party programmers can use it to integrate BarTender into their applications.

In some cases, an XML response is created after the script is run. For example, when you use BTXML script to print a document, you receive an XML response that gives you valuable information about the print job, the items that were printed, the printer that was used to complete the job, and the BarTender settings that were used during the print job. You can integrate this response with a custom application.

Most enterprise resource planning (ERP) software packages already have built-in standard functions for generating XML. This is one reason why using XML is so convenient for instructing applications to send commands to BarTender. One potential challenge, however, is that the default XML that is generated by this software may not be compatible with the BTXML format that BarTender uses. As an alternative to generating custom XML from your ERP application, you can generate your XML in its default format and then convert it to BXTML by using Integration Builder.

### Methods of Running BTXML Script

You can create BTXML script as a script or as a file and then send it to BarTender by using any of the following methods:

<table>
    <thead><tr>
        <th>Method</th>
        <th>Description</th>
    </tr></thead>
    <tbody><tr>
        <td><p>Integration Builder</p></td>
        <td>Integration Builder is a BarTender companion application that you can use to integrate BarTender with other software or other sources of data and to automate processes in BarTender. By using Integration Builder, you can create an integration that contains a Print BTXML Script action that you can configure to pass your BTXML script to BarTender to print one or more documents.</td>
    </tr>
    <tr>
        <td><p>BarTender .NET SDK</p></td>
        <td><p>The BarTender .NET SDK interfaces with any .NET language and supports task-based concurrent label printing for high-demand environments such as web servers. It includes the following application programming interfaces (APIs) that support BTXML script:</p>
            <ul>
                <li><strong>Print API</strong>: Run BTXML with the Print API using the <code>Engine.XMLScript</code> method. This method passes either a BTXML script string or the path and file name of a file that contains BTXML Script.</li>
                <li><strong>Print Server API</strong>: With the Print Server API, you can use instances of the <code>XMLScriptTask</code> class to run BTXML script. The XMLScriptTask task is then submitted to the task queue by either the <code>QueueTaskAndWait</code> method or the <code>QueueTask</code> method. The BTXML script can be used in either file or string mode. In file mode, the path to a BTXML script file is given, and the file is read at print time to automate BarTender. In string mode, the BTXML script itself is placed in the task and then used to perform automation.</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td><p>ActiveX Automation</p></td>
        <td>BarTender exposes the functionality of ActiveX Automation as a set of software objects. By using a programming or scripting language, such as Visual Basic or C#, you can use ActiveX Automation to pass BTXML scripts to BarTender by using the Application object XMLScript method.</td>
    </tr>
    <tr>
        <td><p>Command Line Interface</p></td>
        <td><p>You can configure BarTender functions to be performed automatically when BarTender starts by passing BTXML script via the command line interface. The BTXML script must be passed as a string or a file, and the /XMLScript parameter must be the last argument on the command line. The following example shows the correct syntax for passing a BTXML script string to BarTender for processing:</p>
            <pre>/XMLScript = "btxml_script_file"</pre>
        </td>
    </tr></tbody>
</table>

### The BTXML Script Message Format

BTXML script uses an XML-style format to communicate with BarTender to process print jobs. BarTender processes the code and then performs the task that the code defines.

All BTXML commands that are sent to BarTender must have the following format: 

~~~ xml
<?xml version="1.0" encoding="utf-8"?>
<XMLScript Version="2.0">
    <Command>
        ...
    </Command>
</XMLScript>
~~~

The `<Command>` tag defines the command request, and uses the following syntax:

~~~ 
<Command [Name=Command Name] [RepeatCount=Number]> ... </Command> 
~~~

The ellipsis is then replaced with the tags that the command contains, such as print, read from database, or serialize.





    