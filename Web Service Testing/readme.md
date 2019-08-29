### Web Services Testing

#### Objectives

This chapter discusses web services in general and looks at
TestComplete support for testing web services. You\'ll learn how to
import a web service and call a web service function directly in a
test. You\'ll use Web Services Checkpoint and XML Checkpoint to verify
results between test runs.

#### Overview of Web Services

Web Services provide a standardized SOAP based mechanism for calling
functions across a network of computers where the remote computer
executes the specified routine and returns the results. From the
calling computer a request is made using the SOAP protocol and the web
service provided will execute the function specified and return the
result.

![](./media/image276.jpeg){width="3.0108311461067365in"
height="1.5365616797900263in"}

SOAP stands for Simple Object Access Protocol and is a standardized
format for calling functions on remote computers.

In order to work with Web Services, you must have access to a WSDL
(Web Services Description Language) document that describes the
available functions, their parameters and results. By importing the
WSDL document into TestComplete, Web Services calls can be made using
the Web Services checkpoint.

You can use Web Services to supply data used in a test or you can test
a Web Service itself. Web Services can be used directly from Keyword
Tests or Script and the results used as just another data source.

#### Web Service Example*

First, let\'s take a look at a sample web service that contains a
number of math related functions. The web service is located at this
URL:

[http:*//training.falafel.com/testcompletews/*](http://training.falafel.com/testcompletews/)

Using a web browser to hit the above URL, you can see a listing of the
available functions provided by the web service. A link to the WSDL
document (the link that reads \"Service Description\" in the
screenshot below) describes the structure of each request and
response. If you click on the \"Service Description\" link you will
see the WSDL XML document that fully describes the web service.

![](./media/image277.png){width="5.906447944006999in" height="2.9325in"}

Not all web services frameworks provide a page like the one above that
allows a user to examine each function call individually. In many
cases you will only have a WSDL link pointing to the XML document
describing the available functions and data types.

#### Importing a Web Service

> Before calling web service functions we need to import its WSDL
> document using the **Web Services Project Item.** This project item is
> only included in the Enterprise version of TestComplete. Here are the
> steps to import a Web Service:

57. From the Project Explorer right click the project node and select
    **Add \| New Item..**. and then the Web Services Project Item:

![](./media/image278.png){width="4.345608048993876in" height="3.6875in"}

> **Figure 196 \--Adding the Web Services Project Item**

58. Right click the Web Services node and select **Add \| New Item\...**
    This will display the Create Project Item dialog.

59. Specify the name for the Web Service to be imported.

![](./media/image279.png){width="4.332505468066492in"
height="2.041874453193351in"}

> **Figure 197 \-- Creating the Web Service Wrapper**

60. On the Web Services editor in the Workspace click the **Select**
    button to import a Web Service:

![](./media/image280.png){width="4.422877296587926in"
height="2.7708333333333335in"}

> **Figure 198 \--Web Services Editor**

61. Specify the URL of the WSDL document
    \"**<http://training.falafel.com/webservice/>
    service1.asmx?WSDL**\".

62. Click the **Get Services** button to import the Web Service, then
    click OK to finish the import process.

![](./media/image281.png){width="5.206571522309711in"
height="2.84375in"}

> **Figure 199 \-- Im porting the Web Service**
>
> You should now see the WSDL imported into TestComplete and be able to
> review the objects and methods provided by the web service within the
> editor.

![](./media/image282.png){width="5.950994094488189in"
height="4.134374453193351in"}

> **Figure 200 \-- The Im ported Web Service**
>
> []{#Lab:_Using_a_Web_Service_From_a_Keyword_ .anchor}**Lab: Using a
> Web Service From a Keyword Test**
>
> To use the results from a keyword test you can use the Last Operation
> Result, if the web service returns a value. The example below runs the
> web service imported in the previous example and logs the return
> value.

1.  From the Test Actions category of Operations, drag the **Call Object
    Method** Operation into the Keyword Test editor.

2.  In the **Call Object Method** dialog, type \"WebServices\", then a
    period \".\". The list of Web Services in your project should
    display in the drop-down list. Select the web service you imported
    and then click the **Finish** button to create the web service call
    and close the dialog.

![](./media/image283.png){width="5.55871719160105in"
height="3.3958333333333335in"}

> **Figure 201 \--Calling the WebService**

3.  In this example we\'re using the \"Add\" web service, a method that
    takes two parameters. Double-click the **Value** column to bring up
    the **Operation Parameters**.

![](./media/image284.png){width="4.975261373578303in"
height="0.5308333333333334in"}

> **Figure 202 \--Invoking Parameters Dialog**

4.  In the Operation Parameters dialog, enter values for each parameter
    in the list, then click the Finish button to retain the values and
    close the dialog.

![](./media/image285.png){width="4.6688320209973755in"
height="2.1145833333333335in"}

> **Figure 203 \--Setting Param eter Values**

5.  Drag a **Log Message** Operation from the Logging category to the
    Keyword Test. This will display the **Log Message** wizard.

6.  In the Log Message wizard, leave the **Message** blank and click the
    **Next** button to proceed to the **Operation Parameters** page of
    the wizard.

7.  In the **Operation Parameters** page of the wizard, click the
    ellipses button for the

> **AdditionalInformation** property. This will display the **Edit
> Parameter** dialog.

8.  In the **Edit Parameter** dialog, drop down the **Mode** list and
    select **Last Operation** Result. Click the **OK** button to close
    the dialog, then click the **Finish** button to close the wizard.

![](./media/image286.png){width="4.375099518810149in"
height="2.1770833333333335in"}

> **Setting Log Message Parameters**

9.  At this point, the Keyword Test should look something like the
    screenshot below.

![](./media/image287.png){width="6.264760498687664in"
height="0.5961450131233595in"}

> **Figure 204 \--Keyword Test with Web Service**

10. Run the test. The message should show the result of the web service
    call.

![](./media/image288.png){width="1.5396380139982502in"
height="1.1859372265966754in"}

> **The Logged Web Service Result**
>
> []{#Web_Services_Checkpoints .anchor}**Web Services Checkpoints**
>
> Not only can we call the web service directly and use the results
> however we\'d like in the test, we can also test the web service
> itself to see that it returns expected results. You can perform all of
> the operations needed to call a web service method and check the
> results yourself, or you can use the **Create Web Service Checkpoint
> Wizard** to walk you through the process. Performing the operations by
> hand is more flexible, but the wizard helps you create checkpoints
> faster and more conveniently.
>
> The wizard helps you:
>
> Create an **XMLCheckpoint** project item that stores a baseline copy
> of a web service's response.
>
> Generate script code or Keyword Test steps that calls the web service
> method and checks the result.
>
> You can invoke the wizard when recording a test or at design time. To
> display the wizard when recording a test, select **Create Web Service
> Checkpoint** from the Recording toolbar. You can create Web Service
> Checkpoints for keyword tests and in code. Drag the Web Service
> Checkpoint Operation into the Keyword Test editor.

![](./media/image289.png){width="3.637673884514436in"
height="2.9895833333333335in"}

> **Figure 205 \--Keyword Tests Checkpoints**
>
> \...or create Web Service Checkpoints using the Code Editor toolbar.

![](./media/image290.png){width="3.137584208223972in"
height="2.6041666666666665in"}

> **Figure 206 \--Code Editor Checkpoints**
>
> []{#Web_Services_Test_Log_Results .anchor}**Web Services Test Log
> Results**
>
> When using the XML Checkpoint, the TestComplete Test Log provides
> additional support for examining which XML nodes differ. When we
> execute our Web, Services test we get a clean test log without errors.
> If we modify our test to generate an error, we can look at the
> resulting test log and see specifically where the difference in the
> XML is located.
>
> To simulate an error, we\'re going to modify the **y** parameter in
> our call to the web service and re-execute our test.

1.  Double click the **Value** column on the first step of our Keyword
    Test. Change the y parameter value to \"21\" on the Call Object
    Method dialog and click the **Finish** button:

![](./media/image291.png){width="4.509179790026247in"
height="2.000624453193351in"}

> **Figure 207 \--Changing the \"Y\" Value**

2.  Click the **Run** button on the Keyword Test Editor to re-execute
    the test.

3.  On the **Test Log** window click the **Details** link.

![](./media/image292.png){width="4.966160323709536in"
height="1.3921872265966755in"}

> **Figure 208 \--Test Log for Web Service**
>
> The XML Checkpoint details show us the **Expected XML Data** vs. the
> **Actual XML Data**
>
> reported between the documents.

![](./media/image293.jpeg){width="5.858810148731409in"
height="3.4125in"}

[]{#Lab:_Using_the_Web_Services_Checkpoint_F .anchor}**\
**

> **Lab: Using the Web Services Checkpoint From a Keyword Test**
>
> In this lab, we\'ll take a look at calling a web service function,
> specifying the expected results and then verifying those results:

1.  On our Web Services Project, right click the **KeywordTests** node
    in the Project Explorer and select **Add \| New Item\...** to create
    a new web services Keyword Test. This will display the Create
    Project item dialog.

![](./media/image294.png){width="4.41576990376203in"
height="2.0109372265966754in"}

> **Figure 209 \--Creating New Keyword Test**

2.  From the **Checkpoints** section of the **Operations** palette drag
    & drop the **Web Services Checkpoint**.

![](./media/image295.png){width="2.602512029746282in"
height="2.3203116797900263in"}

> **Figure 210 \--Drop Web Services Checkpoint**

3.  On the **Create Web Service Checkpoint** dialog select our imported
    web service and click **Next**.

![](./media/image296.png){width="6.251077209098862in"
height="2.3793744531933507in"}

> **Figure 211 \--Selecting the Im ported Web Service**

4.  Select the **Add** function and click **Next** to specify the x and
    y parameters.

![](./media/image297.png){width="4.159982502187226in" height="3.0625in"}

> **Figure 212 \--Select the Add Function**

5.  Enter 10 and 20 for the **x** and **y** values respectively then
    click the **Next** button.

![](./media/image298.png){width="6.240153105861768in"
height="2.2814577865266843in"}

> **Figure 213 \--Entering X and Y Values**

6.  Expand the XML tree (left side of the dialog) so you can see the
    \"\#text\" node which is the expected result of the \"Add\" function
    call. Click the **Finish** button. Note that you can change the
    Value for the AddResult if you need to.

> ![](./media/image299.png){width="6.186564960629921in"
> height="5.15375in"}
>
> **Figure 214 \--Setting the Expected Result**
>
> The Web Services Checkpoint uses an XML Checkpoint to validate the
> resulting XML from the web service. On the above dialog you are given
> an option to use an existing XML Checkpoint or create a new one.
>
> The resulting Keyword Test contains two steps including:

1.  A call to the Web Services function passing the specified
    parameters.

2.  A call to an XML Checkpoint used to verify the resulting XML.

![](./media/image300.png){width="5.919174321959755in"
height="0.8411450131233595in"}

> **Figure 215 \--Web Services Function Call and XML Checkpoint**
>
> []{#XML_Checkpoint .anchor}**XML Checkpoint**
>
> Web Services communicate via XML therefore the TestComplete XML
> Checkpoint is perfectly suited to the task of verifying calls to these
> functions. However, this Checkpoint can also be used for XML files or
> URLs that return XML. In this topic will take a look at adding an XML
> Checkpoint to our existing Web Services test that validates the
> contents of a file. For example, let\'s say we have an XML file named
> \"Contacts.XML\" that looks like this:

![](./media/image301.png){width="4.968770778652669in"
height="4.958333333333333in"}

> **Figure 216 \--Contacts.xml**

#### Creating an XML Checkpoint Using a File

1.  Add an **XML Checkpoint** from either the Recording toolbar, as a
    Keyword Test Operation or from the Code Editor toolbar.

2.  On the XML Checkpoint dialog, use the default \"Create new item in
    stores\", enter \"\<your local path\>\\Contacts.xml\" as the \"File
    name\" under **XML Source** and click the **Finish** button.

> ![](./media/image302.png){width="5.6897856517935255in"
> height="3.2793744531933506in"}
>
> **Figure 217 \--Creating the XML Checkpoint**
>
> We can optionally use an existing XML Stores item and/or specify a URL
> to fetch the XML document used during the comparison.

3.  Now that we\'ve added the XML Checkpoint to our test, let\'s take a
    look at the XML store item and review our options for comparison.
    Expand the **Advanced \| Stores \| XML** nodes for the project from
    the Project Explorer and double click the new \"XmlCheckpoint1\"
    node

![](./media/image303.png){width="6.1515605861767275in"
height="3.183333333333333in"}

> **Figure 218 \--XML Checkpoint Editor**

#### XML Checkpoint Options

> The editor for **XML Checkpoints** has several options to customize
> the type of comparison performed during the checkpoint execution.
> These options are designed to ignore certain parts of XML documents,
> extending the capabilities of the checkpoint in situations where the
> documents might not be identical. These options include:

##### Ignore node order Ignore attributes

##### Ignore namespace declarations Ignore prefixes

> **Compare in subtree mode** \-- for comparing an XML fragment
>
> **Extended logging** \-- optionally report information on unchanged
> nodes
>
> []{#_bookmark241 .anchor}**Summary**
>
> In this chapter, we defined web services and examined TestComplete
> support for testing these systems. We looked at:
>
> Importing a web service WSDL document into TestComplete. Using a Web
> Service directly in a test.
>
> Using the Web Services Checkpoint.
>
> Calling a web service function and specifying the XML result.
> Verifying the results of XML documents using the XML Checkpoint.