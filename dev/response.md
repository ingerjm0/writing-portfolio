# Getting Started Guide (XML) - Sample Chapter 2

[Return to Getting Started Guide (XML)](overview.html)

---

## Using the XML Response

In some cases, an XML response is created after the script runs. An example of this is when you pass BTXML script to BarTender by using ActiveX Automation. An XML response gives you valuable information about the print job, the printer that was used to complete the job, the BarTender settings during the print job, and complete details about the printed items. This response can be integrated with a custom application. An XML response is returned when BTXML script is run by using the following methods:

* ActiveX Automation
* Print Server API
* Integration Builder

You can use the information that is contained in the response to:

* Troubleshoot problems that were encountered while print jobs were processed.
* Record the status of print jobs.
* Create a record that you can use to validate the content of documents and individual printed items.
* Create a summary of the entire print job.

The default response that is returned contains information about the user who sent the BTXML request, the printer that was used to process the request, the status of the print job, and any messages that were created. The following example shows the response that is returned when no attributes are used or when the 'ReturnPrintData' attribute is set to true and the 'ReturnSummary' and 'ReturnLabelData' attributes are set to false.

~~~ xml
<?xml version="1.0" encoding="utf-16"?>
<Response Version="2.0" Name="09232006_103601_Job1" ID="123" AppName="BarTender" AppVersion="9.00" AppVersionId="900" AppVersionMajor="9" AppVersionMinor="00" AppVersionBuild="2345" AppInstancePid="12345" AppInstanceGUID="(5EFC7975-14BC-11CF-9B2B-00AA00573819)">
    <User>Administrator</User>
    <Server>MyServer</Server>
    <Command Name="Job1">
        <Print GUID="{C87068F8-4972-41F1-A6E8-724381703764}" JobName="MCIJob" ID="1234" JobLastStatus="Sent" JobCompleted="true">
            <JobStatus Completed="true">
                <TimeJobStart>02:24:34</TimeJobStart>
                <TimeJobQueued>02:24:34</TimeJobQueued>
                <TimeJobSent>02:24:34</TimeJobSent>
                <LastStatus>Sent</LastStatus>
                <Description>Finished sending print job to printer.</Description>
            </JobStatus>
            <Message ID="1606" GUID="{8A8E8550-C822-4e84-8713-212793DFD6E1}" Severity="Information" Category="Miscellaneous" Response="OK">
                <Text>BarTender successfully sent the print job to the spooler.
                    Job Name: MyJobName
                    BarTender Document: Document1.btw
                    Printer: Datamax H-4212 7.1.4 </Text>
            </Message>
        </Print>
    </Command>
</Response>
~~~

You can set the response to include additional information by setting the attributes of various commands. Read on to learn more about how to customize the data returned in the XML response.

### Returning Print Data

The 'ReturnPrintData' attribute displays the summary data and the template information, depending on how the 'ReturnSummaryData' and 'ReturnLabelData' attributes are set. When you set the `<Print>` command's 'ReturnPrintData' attribute to true and do not include any other attribute, the response includes the print job details, a summary of the print job, and the individual item information. When you set either the 'ReturnSummaryData' or 'ReturnLabelData' attributes to false, their information is removed from the response.

### Returning Summary Data 

When you set the 'ReturnSummary' attribute of the `<Print>` command to true, or do not include the attribute at all, a response is returned that includes the 'ReturnPrintData' attribute information and a summary of the entire print job. The summary information includes document and printer information, general page and layout information, and information about how BarTender was configured when it processed the print job. When you set 'ReturnSummary' to false, a response is returned, but it does not include a detailed summary of the print job.

### Returning Template Data 

When you set the 'ReturnLabelData' attribute to true or do not include the attribute at all, a response is returned that includes the print job information (see <strong>Returning Print Data</strong> above), as well as a detailed definition that includes page, template, object, and data source information that can be used to validate and reprint the print job. 

### Returning Checksum Data

To return checksum data in the response, you must set the 'ReturnChecksum' attribute to true. The checksum attribute returns checksums that represent various parts of the print job and objects that are included on the document that is being printed.

History Explorer and Reprint Console use these checksum values to verify the content of the documents that are being reprinted by comparing the checksums of the new document with the old one. If the checksum values match, you can be sure that the document that you print exactly matches the old one.

### Returning an Image of a Label

The 'ReturnImageInReponse' attribute of the `<ExportPrintPreviewToImage>` command returns a response that contains an image of the exported template as a string in Base64 format. 

