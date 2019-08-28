**Table of Contents**

[Overview of TestComplete](./Overview%20of%20TestComplete/Readme.md)
--------------------------------------------------------

[Keyword Testing](./Keyword%20Testing/readme.md)
--------------------------------------

[Project Organization](./Project%20Organization/readme.md)
------------------------------------------------

[Test Log](./Test%20Log/readme.md)
---------------------------------

[Stores and Checkpoints](./Stores%20and%20Checkpoints/readme.md)
----------------------------------------------------------------

[Name Mapping](./Name%20Mapping/readme.md)
-----------------------------------------

[TestComplete Debugging](./Debugging/readme.md)
--------------------------------------------------

[Event Handling](./Event%20Handling)
-------------------------------------

[Data Driven Testing](#Data_Driven_Testing)
-----------------------------------------------

##### [Objectives](#Data_Driven_Testing)

##### [Materials](#_bookmark181)

##### [The DB Table Object](#_bookmark181)

##### [Creating a Data Driven Test](#Creating_a_Data_Driven_Test)

##### [Database Table Checkpoint](#Database_Table_Checkpoint)

##### [Summary](#_bookmark193)

[Web Testing](#Web_Testing)
-------------------------------

##### [Objectives](#Web_Testing)

##### [Materials](#_bookmark195)

##### [Web Application Testing Issues](#Web_Application_Testing_Issues)

##### [Understanding The TestComplete View of Web](#Understanding_The_TestComplete_View_of_W)

##### [Applications](#Understanding_The_TestComplete_View_of_W)

##### [Web Tree Models](#Web_Tree_Models)

##### [Web Stores & Checkpoints](#Web_Stores_&_Checkpoints)

##### [Summary](#_bookmark207)

[Mobile](#Mobile)
---------------------

##### [Objectives](#Mobile)

##### [Materials](#_bookmark209)

##### [Mobile Testing Strategies](#_bookmark209)

##### [Mobile Web](#Mobile_Web)

##### [Android](#Android)

##### [Summary](#Xamarin_Open_Apps_Testing)

[Web Services Testing](#Web_Services_Testing)
-------------------------------------------------

##### [Objectives](#Web_Services_Testing)

##### [Materials](#_bookmark230)

##### [Overview of Web Services](#_bookmark230)

##### [Web Service Example](#Web_Service_Example)

##### [Importing a Web Service](#Importing_a_Web_Service)

##### [Lab: Using a Web Service From a Keyw ord Test](#Lab:_Using_a_Web_Service_From_a_Keyword_)

##### [Web Services Checkpoints](#Web_Services_Checkpoints)

##### [Web Services Test Log Results](#Web_Services_Test_Log_Results)

##### [Lab: Using the Web Services Checkpoint From a Keyword Test](#Lab:_Using_the_Web_Services_Checkpoint_F)

##### [XML Checkpoint](#XML_Checkpoint)

##### [Summary](#_bookmark241)

[Distributed Testing](#_bookmark242)
----------------------------------------

##### [Objectives](#_bookmark242)

##### [Materials](#about-the-network-suite)

##### [About the Netw ork Suite](#about-the-network-suite)

##### [Setting up a Distributed Test](#setting-up-a-distributed-test)

##### [Executing Distributed Tests](#executing-distributed-tests)

##### [Lab: Simple Distributed Test](#lab-simple-distributed-test)

##### [Summary](#summary)

[Manual Testing](#manual-testing-2)
---------------------------------------
##### [Objectives](#manual-testing-2)

##### [Materials](#_bookmark267)

##### [About Manual Testing](#_bookmark268)

##### [Creating Manual Tests](#creating-manual-tests)

##### [Manual Test Interaction With Automated Tests](#manual-test-interaction-with-automated-tests)

##### [Exporting a Manual Test](#exporting-a-manual-test)

##### [Importing a Manual Test](#importing-a-manual-test)

##### [Legacy Migration](#legacy-migration)

##### [Summary](#summary-1)

[Low Level Procedures](#low-level-procedures-2)
---------------------------------------------------
##### [Objectives](#low-level-procedures-2)

##### [Materials](#about-low-level-procedures)

##### [About Low Level Procedures](#about-low-level-procedures)

##### [Recording Low Level Procedures](#recording-low-level-procedures)

##### [Calling Low Level Procedures from Keyword Tests](#calling-low-level-procedures-from-keyword-tests)

##### [Summary](#summary-2)

[User Forms](#user-forms-2)
--------------------------------
##### [Objectives](#user-forms-2)

##### [Materials](#Materials)

##### [Using the Designer](#_bookmark297)

##### [Calling User Forms in a Keyword Test](#Calling_User_Forms_in_a_Keyword_Test)

##### [Summary](#_bookmark303)

[Best Practices](#Best_Practices)
-------------------------------------

##### [Objectives](#Best_Practices)

##### [Communicating Test Results](#Communicating_Test_Results)

##### [Plan your testing, but not that kind of planning](#Plan_your_testing,_but_not_that_kind_of_)

##### [Organizing your TestComplete Projects](#Organizing_your_TestComplete_Projects)

##### [Use a Source Control Repository](#Use_a_Source_Control_Repository)

##### [Your Most Important Test](#Your_Most_Important_Test)

##### [General](#General)

##### [Web Page](#Web_Page)

##### [Summary](#Summary)

[Appendix A - Cheat Sheet](#Appendix_A_-_Cheat_Sheet)
------------------------------------------------------------

##### [Keyboard Shortcuts](#Appendix_A_-_Cheat_Sheet)

##### [Keyboard Handling in Recorder](#Keyboard_Handling_in_Recorder)

##### [Configuring Global Shortcuts](#Configuring_Global_Shortcuts)

##### [Configuring Keyboard Emulation](#Configuring_Keyboard_Emulation)

[Appendix B - Types of Testing](#Appendix_B_-_Types_of_Testing)
-------------------------------------------------------------------

##### [Types of Testing](#Types_of_Testing)















### Data Driven Testing

10. []{#Data_Driven_Testing .anchor}**Data Driven Testing**

> **Objectives**
>
> This chapter demonstrates how you can drive tests from data stored in
> a database, spreadsheet or text document. You\'ll learn about the DB
> Table object used to automatically feed data to your test and how to
> leverage the DBTable checkpoint to verify database contents.
>
> []{#_bookmark181 .anchor}**The DB Table Object**
>
> TestComplete provides a built-in data driven testing object type
> called **DB Table** that provides a straight forward and consistent
> mechanism for working with a wide variety of data sources. DB Tables
> can provide connection to Excel spreadsheets, comma delimited CSV
> files and database tables such as Oracle or MS SQL.

#### Creating a DB Table Variable

> To create a DB Table variable:

41. Navigate to the **Variables** tab of for the project. Right-click
    the **Temporary Variables**

> area and select **New Item\...** from the context menu.

42. Provide a name for the table, drop down the Type list and select
    **DB Table**. Click the ellipses in the **Default Value** column.
    This will bring up **Edit DB Table Variable Value** dialog.

![](./media/image186.png){width="5.028421916010498in"
height="0.8971872265966754in"}

> **Figure 160 \--Defining the Table**

43. In the **Edit DB Table Variable Value** dialog, select one of the
    data source types from the list. In the screenshot below the **CSV
    file** type is selected. Click the **Next** button to continue.

![](./media/image187.png){width="5.9469061679790025in" height="3.125in"}

> **Figure 161 \--Selecting the Data Source Type**

44. In this page specify a CSV file, an Excel file or a database table,
    depending on the data source type you specified in the preceding
    step. In this example we specify the path to a CSV file called
    \"orders.txt\". Click the **Create File** button to invoke Notepad.

![](./media/image188.png){width="5.50991469816273in"
height="2.8229166666666665in"}

> **Figure 162 \--Selecting a CSV File**

45. In Notepad, enter a comma-delimited list of information as shown in
    the screenshot below. The first row of information will be used as
    headings. Once you have entered the data, save and close Notepad.
    Click the **Next** button to continue.

![](./media/image189.png){width="4.676351706036745in" height="1.8975in"}

46. The CSV Format Parameters page of the wizard shows a preview of the
    data and allows you to tweak parameters including the delimiters,
    treat several consecutive delimiters as a single entity, and to use
    the first row for column names. You can leave the default settings
    and click the **Finish** button.

![](./media/image190.png){width="4.533639545056868in" height="3.6875in"}

47. When the wizard is finished you will have a new **Default Value**
    column entry. This entry will vary depending on the path you\'ve
    taken through the wizard. Examples of results for several file type
    choices are shown in the screenshot below. Notice that in all three
    cases, the name \"Orders\" stays the same and the type is DB Table.
    Later, if you need to change the data source, assuming the data
    source contains the same named columns, you can swap in a new data
    source without changing your test.

![](./media/image191.png){width="5.020610236220472in"
height="1.7634372265966753in"}

#### Accessing DB Table Values

> You can assign the values from any column in the DB Table. Here\'s a
> quick example of assigning the \"Customer\" edit box from the
> \"Customer\" column in a DB Table.
>
> In the example, we assume that the sample \"Orders\" application with
> the \"New Order\" dialog is already open and the text boxes there are
> already mapped. The \"Orders\" DB Table variable should already be
> configured.

1.  Drag an On-Screen Action Operation to the Keyword Test Editor.

![](./media/image192.png){width="3.214634733158355in"
height="1.8665616797900262in"}

> **Figure 163 \--Creating an On-Screen Action**

2.  In the On-Screen Action wizard, select the mapped \"Customer\"
    object.

![](./media/image193.png){width="3.583225065616798in"
height="1.4540616797900263in"}

> **Figure 164 \--Selecting an Object**

3.  In the \"Specify Method or Property\" page of the On-Screen Action
    wizard, select the

> **SetText** method.

![](./media/image194.png){width="5.4898392388451445in"
height="1.6396872265966753in"}

> **Figure 165 \--Selecting the SetText Method**

4.  In the \"Operation Parameters\" page of the wizard, click the
    ellipses for the text value to display the Edit Parameter dialog. In
    the Edit Parameter dialog, set the **Mode** to \"Variable\", drop
    down the **Value** list and move the mouse to the \"Orders\"
    variable. Click the **Column** button when it appears to display the
    Table Indexes dialog.

![](./media/image195.png){width="5.534167760279965in"
height="4.322916666666667in"}

> **Figure 166 \--Selecting the DB Table Variable**
>
> The DBTable variable can be created in a project suite, the project or
> in the variables for a keyword test.

5.  In the Table Indexes dialog, drop down the Column list and select
    Customer. Click **OK**, **OK** again and the **Finish** button to
    close the wizard.

![](./media/image196.png){width="4.955260279965004in"
height="2.90625in"}

> **Figure 167 \--Selecting the DB Table Colum n**

6.  The completed On-Screen action shows the \"Customer\" object text
    being assigned the \"Orders\" DB Table \"Customer\" column value.

![](./media/image197.png){width="5.331420603674541in"
height="0.7631244531933509in"}

> **Figure 168 \--The Completed SetText Operation**
>
> []{#Creating_a_Data_Driven_Test .anchor}**Creating a Data Driven
> Test**
>
> A productive way to construct data driven Keyword Tests is to identify
> areas within your application where repetitious data entry is required
> such as adding customer records or creating orders. These scenarios
> are generally good targets for performing data driven testing. In this
> section we\'ll construct a data driven Keyword Test that illustrates
> just such a scenario using the \"Orders\" sample application. In this
> example we\'ll illustrate using the DB Table to read data from a comma
> separated file (CSV). To start, we\'ll record a basic data entry
> scenario of inserting a new customer order.

#### Recording the Test

1.  Select **File \| New \| Project\...** and click **OK** on the Create
    Project dialog.

2.  Launch the \"Orders\" sample application.

3.  Right-click the \"Orders\" process in the Object Browser and select
    **Add to TestedApps** from the context menu. You may need to click
    the **Refresh** option if you don\'t see the \"Orders\" process in
    the Object Browser.

![](./media/image198.png){width="4.490891294838145in"
height="3.9895833333333335in"}

> **Figure 169 \--Adding to TestedApps**

4.  Close the \"Orders\" application. We\'ll launch it during the
    recording using the

> **TestedApps** button.

5.  Click the **Record** button on the toolbar button.

6.  Using the **TestedApps** button launch the Orders application.

7.  Select **Orders \| New Order\...**

8.  Fill in Customer, Street, City, State and Zip.

9.  Click **OK.**

10. Click the **Stop** button on the recording toolbar to end the
    recording.

#### Data Driven Loops

> The **Data Driven Loop** Operation makes it possible to iterate over
> data for some set of Test Steps. The Operation will loop once for each
> record in the data source. The data for columns in the data source
> will be available to your Keyword Test and can be assigned to items in
> the test. The walk through below uses the recorded \"Orders\" test
> where the new order is created, populated and added to the table.
> These test steps will become a part of a data driven loop.

1.  Select the \"Orders\" node that contains the creation of a new order
    and entering of fields in the order.

2.  Right-click the Keyword Test Editor and select **Make Data
    Loop\...** from the context menu. This will display the
    **Data-Driven Loop** dialog.

![](./media/image199.png){width="4.6980096237970255in"
height="4.65625in"}

> **Figure 170 \--Making a Data Loop**

3.  In the **Select Table Variable** page of the wizard, select the
    **Create new variable** radio button and enter \"Orders\" as the
    variable name. Click the **Next** button to continue.

![](./media/image200.png){width="5.542230971128609in" height="2.6875in"}

> **Figure 171 \--Selecting the DB Table Variable**

4.  In the **Specify Table type** page of the wizard, select the \"CSV
    file\" option. Click the **Next**

> button to continue.

![](./media/image201.png){width="5.673924978127734in"
height="3.34375in"}

> **Figure 172 \--Setting the Data Source Type**

5.  In the **Select CSV File** page of the wizard, click the ellipses
    button, locate and open the \"orders.txt\" file that contains the
    orders data. Click the **Next** button to continue.

![](./media/image202.png){width="5.609075896762905in"
height="1.9284372265966754in"}

> **Figure 173 \--Selecting the CSV File**

6.  In the **CSV Format Parameters** page of the wizard, click the
    **Comma** checkbox from the **Delimiters** group. Click the **Next**
    button to continue.

![](./media/image203.png){width="5.473197725284339in"
height="3.155624453193351in"}

7.  In the \"Select Records\" page of the wizard, leave the defaults to
    use all the records and click the **Next** button to continue.

![](./media/image204.png){width="4.693610017497813in"
height="2.9270833333333335in"}

> **Figure 174 \--Selecting The Record Range**

8.  In the **Update Values** page of the wizard, drop down the Value
    list for each data entry field and select the corresponding column
    from the data. In the screenshot below, the \"Customer\" data entry
    field is being assigned the \"Customer\" column from the data table.
    Click the **Finish** button to create the data table and data driven
    loop.

![](./media/image205.png){width="5.483486439195101in"
height="3.165937226596675in"}

9.  Notice in the Keyword Test Editor, we have a new Data-Driven Loop.
    The Value for the loop is the local \"Orders\" variable. Each text
    box assignment now comes from columns in the \"Orders\" table.

![](./media/image206.png){width="4.518367235345582in" height="2.5625in"}

> **Figure 175 \--The Data Driven Loop**

10. Navigate to the Variables tab and notice the \"Orders\" DB Table
    variable that was created for us. You can see that the DB Table
    variable points to the \"Orders.txt\" CSV file.

![](./media/image207.png){width="5.0311570428696415in"
height="1.7531244531933508in"}

> **Figure 176 \--The DB Table Variable**
>
> []{#Database_Table_Checkpoint .anchor}**Database Table Checkpoint**
>
> The **Table Checkpoint** verifies live database content, both rows and
> columns, against a static snapshot of the data stored when the
> checkpoint was created. Using the **Table Checkpoint** is very similar
> to using the Table checkpoint with the exception being the location
> where the data is retrieved. To use a **Table Checkpoint** we need:
>
> A connection string that defines access to a data provider so we can
> connect to a data store.
>
> A specific Table, View or Query that defines criteria used to fetch
> data from the store.
>
> The connection string allows for connecting to any ADO or ADO.NET
> supported data provider including data sources such as .CSV files,
> Excel spreadsheets or a wide variety of database servers.

#### Creating a DBTables Store

> For this example, we\'ll use Microsoft\'s Text Driver which provides
> access to data stored in . CSV files to illustrate the DBTable store.
> We\'ll use this provider as it does not require an actual database
> server backend and is generally available on most computers. The
> connection string for the Microsoft Text Driver is:
>
> Driver={Microsoft Text Driver (\*.txt;
> \*.csv)};Dbq=c:\\;Extensions=asc,csv,tab,txt;
>
> In this connection string the name **Dbq** specifies the folder where
> our CSV files are located. We\'ll use a file called \"c:\\order.txt\"
> to create our store from.

1.  If the **Stores \| DBTables** node does not exist in the Project
    Explorer, right-click the **Stores** node, select **Add \| New
    Item\...** from the context menu. Select the **DB tables** item from
    the list of item types and click the **OK** button to close the
    dialog.

2.  Right-click the **Stores \| DBTables** node in the Project Explorer
    and select the **Add \| New Item\...** option. This will display a
    dialog that allows you to define the store.

3.  Select the **Create a new item in Stores** option and click
    **Next**. If there are no existing DBTables stores, skip this step.

4.  Use the following values on the **Specify Connection Settings\...**
    page of the wizard.

> **Name** \-- Orders
>
> **Connection** \-- Driver={Microsoft Text Driver (\*.txt;
> \*.csv)};Dbq=c:\\;Extensions=asc,csv, tab,txt;
>
> **Custom query** \-- radio button should be checked

![](./media/image208.png){width="5.190495406824147in"
height="4.03125in"}

> **Figure 177 \--Setting the Connection**

5.  Type \"select Customer, Street from Orders.txt\" as the SQL
    statement and click **Next**.

![](./media/image209.png){width="5.152006780402449in"
height="1.9903116797900262in"}

> **Figure 178 \--Entering SQL**
>
> Note that you can also click the Design button here to get help
> building your SQL string.

6.  The **Specify Data Range** page of the wizard defines the number of
    rows and which columns to store. Click **Next** (we\'re using the
    defaults here).

![](./media/image210.png){width="5.159082458442695in"
height="4.041666666666667in"}

> **Figure 179 \--Setting the Data Range**

7.  Next, preview of the data then click **Finish** to complete the
    DBTable checkpoint.

![](./media/image211.png){width="5.151218285214348in"
height="2.0521872265966756in"}

> **Figure 180 \--Preview ing the Data**

#### Creating a Database Table Checkpoint

> To create a Database Table checkpoint that compares the current state
> of the data with a DBTable store:

1.  Create a new Keyword test called \"DBTableCheckpoint\".

2.  Select the **Checkpoints** category on the Operations palette of the
    Keyword editor.

3.  Drag/Drop the **Database Table Checkpoint** onto the test.

![](./media/image212.png){width="3.0258366141732282in"
height="2.911457786526684in"}

> **Figure 181 \--Adding the DBTable Checkpoint**

4.  In the **Specify DBTable Element** page of the wizard, select the
    **Use an existing stores item** option, make sure that the
    \"Orders\" store is selected and click **Next**.

![](./media/image213.png){width="5.163638451443569in"
height="3.0208333333333335in"}

> **Figure 182 \--Specifying an Existing DBTable Store**

5.  Notice that the DBTable Checkpoint has been created in the Keyword
    Test.

![](./media/image214.png){width="5.132080052493438in"
height="0.6635411198600175in"}

> **Figure 183 \--New DBTable Checkpoint**

#### Modifying the Checkpoint

> Once the checkpoint has been created we\'ll see a new Orders node
> under **Stores \| DBTables** in our Project Explorer and we can review
> the data in the Checkpoint editor window. Using the **Edit\...**
> button we can walk through the wizard again and modify any part of the
> checkpoint.

![](./media/image215.jpeg){width="5.906521216097988in"
height="3.3366666666666664in"}

> **Figure 184 \--DBTables Checkpoint Editor**
>
> The DBTables Checkpoint editor also allows you to specify which rows
> and columns to use as well as edit the data in any individual cell. As
> an example, make a few changes here to modify the stored data. In the
> screenshot below, notice that the \"Customer\" name in row
>
> \#2 is changed.

![](./media/image216.png){width="2.0833333333333335in"
height="2.0833333333333335in"}

> **Figure 185 \--Editing the Data**

#### Executing the Table Checkpoint

> Now we can execute our test to compare the DBTable data against the
> actual CSV file on disk. Again, this checkpoint is reading data from
> the CSV file and comparing it to the data we stored in the DBTables
> checkpoint for our project. When the checkpoint executes it will open
> the CSV file, execute our \"select\" query statement, return the
> results and perform the comparison. Notice, we now get a error because
> the stored data no longer matches the data from the CSV file:
>
> \"Warning: The \'Customer\' field of row 1 contains a value (John
> Smith) that differs from the stored one (Sam).\"

![](./media/image217.png){width="3.834070428696413in"
height="2.8885411198600175in"}

> **Figure 186 \--DBTables CheckpointFailure**
>
> []{#_bookmark193 .anchor}**Summary**
>
> This chapter demonstrated how you can drive tests from data stored in
> a database, spreadsheet or text document. You learned about the DB
> Table object used to automatically feed data to your test and how to
> leverage the DBTable checkpoint to verify database contents.

### Web Testing

11. []{#Web_Testing .anchor}**Web Testing**

> **Objectives**
>
> This chapter examines TestComplete web application testing features
> and functionality. First, you\'ll learn about the significant
> differences between Windows client and web application testing.
> You\'ll learn about the primary automation challenges web applications
> typically present. You\'ll also explore a few of the essential methods
> TestComplete provides to effectively automate web applications.
>
> []{#_bookmark195 .anchor}**Materials**
>
> \\Projects\\Web Testing
>
> []{#Web_Application_Testing_Issues .anchor}**Web Application Testing
> Issues**
>
> First, let\'s highlight some of the important differences between
> Windows and Web applications. For example, the following statements
> are true of Web applications:
>
> The client UI loads asynchronously, meaning the browser fetches
> different parts of the same page at the same time. The primary impact
> this has on web testing is that the test must allow for the UI to
> completely render prior to interacting with the page contents. In many
> cases this is handled automatically. However, there may be instances
> where you\'ll need to add code to allow the browser to completely
> download a page prior to your test continuing.
>
> Are typically \"stateless\", meaning that the client functions in a
> disconnected manner from the server.
>
> Use HTML/browser-based controls for data entry.
>
> May have dynamically changing UI as a result of JavaScript, AJAX or
> Silverlight executing on the page.
>
> Typically have different functional behavior than Windows
> applications. Generally, require page refreshes thus requiring a
> refresh of the Object Browser. Multiple web browsers (Internet
> Explorer, Firefox, Chrome).
>
> Multiple browser versions and platforms (x86, x64).
>
> These differences make the already challenging task of Web automation
> more difficult than automating Windows applications. To deal with
> these issues TestComplete provides special functions that take Web
> application behavior into account. Before looking to these functions,
> let\'s first take a look at the Object Browser and examine how
> TestComplete \"sees\" web application from an object perspective.
>
> []{#Understanding_The_TestComplete_View_of_W .anchor}**Understanding
> the TestComplete View of Web Applications**
>
> Below is a screenshot of the Object Browser displaying information
> about a typical web application in Internet Explorer.
>
> ![](./media/image218.png){width="0.10416666666666667in"
> height="0.10416666666666667in"}![](./media/image219.png){width="0.15625in"
> height="0.13541666666666666in"}![](./media/image220.png){width="0.13541666666666666in"
> height="0.13541666666666666in"}![](./media/image221.png){width="0.13541666666666666in"
> height="0.13541666666666666in"}Earlier versions of Internet Explorer
> may look significantly different in Object Browser than the screenshot
> below. Recent versions of Internet Explorer show \"Browser
> (iexplore)\" in two different locations. \"Browser (iexplore)\" is the
> first instance of the browser while \"Browser (\"iexplore\", 2)\" is a
> completely separate browser window. The two pages in \"Browser
> (iexplore)\" are represented by two tabs in the browser. Each page
> contains HTML objects. Also notice that browser instances are open
> applications that expose internal information to TestComplete. Each
> browser instance is indicated by the open application icon . Special
> icons in the Object Browser tree indicate the type of open
> application, e.g. Flash ![](./media/image222.png){width="0.15625in"
> height="0.14583333333333334in"}, .NET , Silverlight , Java , etc.

![](./media/image223.jpeg){width="5.886606517935258in"
height="3.180833333333333in"}

> Internet Explorer, Firefox and Chrome handle multiple browser
> instances and tabs differently and these differences show up in the
> Object Browser. Let\'s set up an example where you open a Chrome
> browser window and navigate to Google, then open a second tab on the
> Falafel site and finally open a completely separate browser instance
> and navigate to [http://www.SmartBear.com](http://www.SmartBear.com/).
> The browsers would look something like the screenshot below.

![](./media/image224.jpeg){width="5.3998654855643045in"
height="3.8593744531933507in"}

> **Figure 187 \--Two Browser Windows, Three Tabs**
>
> Now replicate this configuration to open browsers and tabs for
> Internet Explorer and FireFox. The Object Browser Objects panel might
> look something like the screenshot below.

![](./media/image225.png){width="4.3329461942257215in" height="4.5in"}

> **Figure 188 \--Object Browser View of Browsers**
>
> To design effective web application tests, it\'s important to be aware
> of differences in browser design. Browser design will vary according
> to browser type (Internet Explorer, Firefox, etc.) and version.

#### Processes and Tabs

> Modern browsers use individual processes to isolate web applications
> hosted in separate tabs within the browser\'s main window, offering
> greater stability. In the event an individual process fails, the
> browser and other open tabs remain unaffected. If you're testing on
> earlier browser versions, you\'ll only see one process for the browser
> regardless of the number of open tabs.
>
> When recording tests against browsers that use individual processes
> for each tab, be consistent regarding the number of open browser
> windows and tabs at the time of the recording. This guideline makes it
> easier to create reliable tests and to allow TestComplete to capture
> consistent Name Mapping information.
>
> []{#Web_Tree_Models .anchor}**Web Tree Models**
>
> **Web Tree Models** define how web page elements are shown in the
> Object Browser and how they are addressed in tests. TestComplete
> supports four models:
>
> **DOM** \-- Document Object Model, the native way that Internet
> Explorer looks at web pages. The DOM model creates a very flat tree in
> the Object Browser. All items on the web page need to be re-read each
> time the web page is updated. This is the slowest method for using web
> pages.
>
> **TAG** \-- All HTML elements are sorted by their TAG value. If a link
> (\<A\> HTML tag) gets created, only the \"A\" node part of the Object
> Browser tree gets updated.
>
> **Tree** \-- Treats a web page like a normal application where the
> list follows the hierarchy of HTML elements on the web page. The names
> of the objects are taken from the element type names (rather than tag
> names). This model creates a very deep tree for most web pages. The
> tree only contains elements with text and also does not include
> document, window or body objects. This is the fastest method for using
> web pages. This is the default.
>
> **Hybrid** \-- Hybrid is a combination of both DOM and Tree.
>
> The Hybrid model, used in earlier versions of the product as the
> default, has been replaced by the Tree model. The Tree model is faster
> and is recommended for new tests. The Tree model is also required for
> cross browser tests.

#### Naming Conventions

> The naming convention for HTML elements used by TestComplete depends
> on the web page model used:
>
> **DOM** \-- HTML elements are in the form of Item(index). The index
> will be either the ID or Name attribute, if any (with the
> Identification attribute having priority). If the element does not
> have either attribute, TestComplete will assign an index number based
> on the order the item was created.
>
> **TAG** \-- HTML elements have the same form as DOM but are sorted by
> type.
>
> **Tree** \-- HTML elements have the form ObjectType(Index), for
> example: Panel(0) - div element, Image(\"Logo.gif\") - image element.

#### Setting the Project Web Tree Model

> To set the web page model used for the project:

48. In the Project Explorer, select the project node and then click on
    the workspace

##### Properties tab.

49. Select **Open Application \| Web Testing**.

50. Select the Tree model from the drop-down list.

![](./media/image226.jpeg){width="5.900003280839895in"
height="3.754166666666667in"}

> **Figure 189 \--Setting the Web Page Model**
>
> []{#Web_Stores_&_Checkpoints .anchor}**Web Stores & Checkpoints**
>
> TestComplete provides two Checkpoints specific to web testing called
> **Web Comparison** and **Web Accessibility**. In this topic we\'ll
> walk through using both Checkpoints against the \"Orders\" sample web
> site. As with all other Checkpoints, Web Comparison and Web
> Accessibility Checkpoints can be added from the Recording toolbar,
> dragged to a Keyword Test as a Checkpoint operation or created from
> the Script Editor toolbar.

#### Web Comparison

> The **Web Comparison Checkpoint** is geared towards verifying the HTML
> contents of a specific web page. Here are the steps to setup a Web
> Comparison checkpoint:

1.  Create a Web Comparison Checkpoint either from the Recording
    toolbar, drag as a Keyword Test Operation or create from the Script
    toolbar.

2.  On the **Create Web Comparison Checkpoint** dialog, drag & drop the
    cross-hairs icon anywhere onto a web page within Internet Explorer.
    For this example, we\'re using the \"Orders\" sample application
    located at
    [[http://training.falafel.com/Orders]{.underline}](http://training.falafel.com/Orders).
    Click the **Next** button.

![](./media/image227.png){width="5.544225721784777in"
height="2.46875in"}

> **Figure 190 \--Selecting the Page**

3.  The **Specify a Stores element for this checkpoint** page lets you
    configure exactly how and what on the page is stored. To make a new
    store choose the **Create new item in stores** option and supply a
    **Stores object name**. In the **Mode** drop down list decide if you
    want to compare the entire page, only the tag structure or only
    specified tags. If you select the last option for only specified
    tags, you can specify that only **Links**, **Images**, **Input
    Elements** or some combination will be compared. By default, the
    page is read from the browser, but you can **Read content from the
    server** instead. Click the **Finish** button to close the dialog.

![](./media/image228.png){width="5.407373140857393in"
height="4.001248906386702in"}

4.  Click **OK** on the **Create Web Comparison Checkpoint** dialog.

5.  From the **Project Explorer**, navigate to the **Advanced \| Stores
    \| Web Testing** node. Double click the web comparison node to open
    the **Web Comparison Checkpoint** editor. From the editor window you
    can modify the options selected on the **Web Comparison Checkpoint**
    dialog as well as edit the actual HTML markup used during the
    comparison.

![](./media/image229.jpeg){width="5.939494750656168in"
height="3.7199989063867016in"}

> **Figure 191 \--Web Com parison Checkpoint Editor**

#### Web Comparison Options

> The Web Comparison options provides several options that dictate the
> web elements included in the comparison. Use these options to reduce
> the scope of the Checkpoint:

![](./media/image230.png){width="3.0673982939632545in"
height="1.2375in"}

> **Figure 192 \--Web Comparison Options**
>
> **Mode \--** This drop-down list specifies if the comparison will
> verify the contents of the entire web page, \"only tag structure\" or
> \"only specified tags\". If the last option to compare only specified
> tags is selected, the check boxes for **Links**, **Images** and
> **Input elements** are enabled.
>
> **Read the web contents directly from the web server \--** This
> option, controls whether TestComplete should fetch the content
> directly from the web server or from the web browser window. In some
> cases, the content can be considerably different and using this option
> can improve the stability of the results.

#### Web Accessibility

> The **Web Accessibility Checkpoint** ensures that specific web pages
> adhere to guidelines designed to improve the usability of the page by
> people with disabilities. Similar to the Web Comparison Checkpoint,
> you can control the scope of the Web Accessibility Checkpoint to focus
> on the specific items of interest. Most web applications tend to have
> accessibility issues, so you shouldn\'t be surprised if your pages
> have many warnings when applying this Checkpoint using the full range
> of available options. To use a Web Accessibility Checkpoint:

1.  Create a **Web Accessibility Checkpoint** either from the Recording
    toolbar, drag as a Keyword Test Operation or create from the Script
    toolbar

2.  On the **Create Web Accessibility Checkpoint** dialog, drag & drop
    cross-hairs icon anywhere onto a web page within the browser. This
    action will automatically set the name of the Page object. For this
    example, we\'re using the "Orders\" sample application at
    [[http://training.falafel.com/Orders]{.underline}](http://training.falafel.com/Orders).
    Click the Next button to continue.

![](./media/image231.png){width="4.213719378827647in" height="2.6075in"}

> **Figure 193 \--Web Accessibility Checkpoint**

3.  Provide a name for the Checkpoint, de-select any check boxes that
    should not be part of the comparison and click the **OK** button to
    create the Checkpoint.

![](./media/image232.png){width="5.935020778652668in" height="4.9875in"}

#### Web Accessibility Checkpoint Options

> The available options for the Web Accessibility checkpoint are as
> follows:
>
> **Check \"alt\" attribute** \-- All IMG, APPLET, AREA and INPUT
> elements must have a non- empty ALT attribute.
>
> **Check \"mailto:\"** \-- Web page must have at least one A element
> (link), whose REF attribute starts with mailto:
>
> **Check image sizes** \-- All IMG elements must have the WIDTH and
> HEIGHT attributes specified.
>
> **Check \"title\" tag** \-- The web page must have a non-empty TITLE
> element.
>
> **Check tab indexes** \-- All INPUT, SELECT, and TEXTAREA elements
> must have the TABINDEX attribute.
>
> **Check link accessibility** \-- Checks for broken links.
>
> **Check ActiveX objects** \-- Verifies there are no ActiveX objects on
> the web page.
>
> **Check Applet object** \-- Verifies there are no Applet objects on
> the web page.
>
> **Check multimedia links** \-- Verifies there are not AVI or SWF files
> on the web page.
>
> **Check server-side images** \-- Verifies that none of the IMG
> elements SRC attributes contain parameters (i.e. the question mark
> \"?\" is not detected in the SRC attribute).
>
> []{#_bookmark207 .anchor}**Summary**
>
> In this chapter, we looked at Web Testing and how it differs from
> standard Windows client testing. We learned:
>
> How TestComplete \"sees\" the elements of a web page from the Object
> Browser. What the Page object provides regarding web testing.
>
> How specific Web testing methods can be used to solve real world
> problems. To deal with dynamic JavaScript client-side UI.
>
> How to dynamically locate objects on a page.

### Mobile

12. []{#Mobile .anchor}**Mobile**

> **Objectives**
>
> Does the mobile application you\'re testing show up in a browser on
> the device? Perhaps you\'re working with a native Android application
> but you don\'t have access to the source code. Maybe the native
> Android application is developed in-house. TestComplete provides
> testing mechanisms that make the best use for each approach. This
> chapter shows how TestComplete handles mobile web applications that
> may have multiple layouts based on screen dimension, \"black-box\"
> native Android applications where you don\'t have access to the
> application\'s internals and \"white-box\" native Android applications
> that are open to inspection.

[]{#_bookmark209 .anchor}

> **Mobile Testing Strategies**
>
> Here are some questions that can help determine which TestComplete
> feature will work best for your needs:
>
> Do you need to test a mobile site on a wide variety of devices,
> regardless of manufacturer and operating system, for example, iPhone,
> Android, Blackberry, Windows and so on?
>
> Do you need to test a mobile site that uses responsive design, that
> is, where the page layout changes based on device characteristics and
> dimensions?
>
> Do you need access to a device\'s GPS or hardware sensors? Do you need
> access to the internal objects of an application? Are you testing
> Xamarin applications?
>
> The [Mobile Web]{.underline} testing option covers the greatest number
> of devices. In mobile web testing, TestComplete virtual browsers can
> be configured to any set of device characteristics and dimensions.
> This option is relatively easy to set up, leverages your existing
> knowledge of testing web applications and doesn\'t require that you
> have the actual physical devices. This option is also very good at
> testing sites that make heavy use of responsive design. The drawback
> is that you will not have access to the devices internal objects or
> hardware.
>
> Within the [Android]{.underline} category, there are two approaches
> for native Java applications that you can use separately or
> mix-and-match. If you don\'t have access to the application\'s source
> code, you can perform black-box testing using [Image Based
> Testing]{.underline}. TestComplete has a powerful mechanism that
> recognizes images on the screen and allows you to work with that area
> of the screen programmatically and through keyword tests. If you have
> access to an Android application\'s source code, you can perform
> white-box testing by configuring the application as an [Open Android
> Application]{.underline}. This will provide you with deep access to an
> Android application\'s internal screen objects and hardware. Android
> is fully supported and iOS is on the way.
>
> []{#Mobile_Web .anchor}**Mobile Web**
>
> Verifying that websites work on all devices, dimensions and platforms
> has become a major scalability challenge. You certainly can\'t keep a
> junkyard full of physical devices and emulator platforms usually
> require download and configuration of one or more libraries for
> support. TestComplete approach is to create *virtual browsers* that
> run with a set of characteristics and dimensions that mimic a
> particular physical device. TestComplete comes with a stock set of
> pre-configured virtual browsers that run from the test recording
> toolbar.

![](./media/image233.png){width="4.121692913385827in"
height="2.454374453193351in"}

> The screenshot below shows a composite of several virtual browsers
> running the same site on iPad, iPhone 5 and Samsung Galaxy Mini.

![](./media/image234.jpeg){width="5.082027559055118in"
height="6.4518744531933505in"}

> Be aware that TestComplete uses the Chrome browser, no matter what
> browser the actual device is using. Be sure to [[prepare Chrome for
> Web
> Testing]{.underline}](http://support.smartbear.com/viewarticle/62859/?_ga=1.49190255.819616413.1378486108)
> and also [[install
> Chrome]{.underline}](http://support.smartbear.com/downloads/testcomplete/chrome-patches/?_ga=1.49190255.819616413.1378486108)
> [[patches]{.underline}](http://support.smartbear.com/downloads/testcomplete/chrome-patches/?_ga=1.49190255.819616413.1378486108)
> to match the Chrome version you have.

#### Using Virtual Browsers in Keyword Tests

> Mobile web tests use the **Run Virtual Browser** and **Virtual Browser
> Loop** operations instead of their standard browser counterparts **Run
> Browser** and **Browser Loop**. When you drag the **Run Virtual
> Browser** operation to the keyword tested editor, first select a
> virtual browser from the list and click the **Next** button.

![](./media/image235.png){width="5.680190288713911in" height="4.375in"}

> In the **Operation Parameters** page of the wizard, enter the **URL**
> the virtual browser should navigate to. You can also specify the
> number of seconds to wait while the page loads. Click the **Finish**
> button to add the operation to the test.

![](./media/image236.png){width="3.73584864391951in" height="1.65in"}

> From here you can use the **Web** group of keyword operations just as
> you would for standard [cross browser testing]{.underline}. The
> example keyword test below shows the **Run Virtual Browser** operation
> followed by a standard web **Navigate** operation to
> [www.smartbear.com.](http://www.falafel.com/) The **Navigate**
> operates against the **Current Browser**, so the actual run of the
> test loads the site into the virtual browser.

![](./media/image237.png){width="5.940080927384077in"
height="0.4793744531933508in"}

#### Defining Your Own Virtual Browsers

> As new devices become available, you can define them without waiting
> for SmartBear to update the list. You will need a *user agent string*
> and the dimensions of the device.
>
> The characteristics of the device are defined by a user agent string;
> here\'s an example of a user agent string for Apple\'s iPhone 5:
>
> Mozilla/5.0 (iPhone; CPU iPhone OS 6\_1\_4 like Mac OS X)
>
> AppleWebKit/536.26 (KHTML, like Gecko) Version/6.0 Mobile/10B350
> Safari/8536.25
>
> To learn more about user agent strings, you can Google for lists of
> user agent strings and even utilities that will return the user agent
> string for the device you\'re browsing from.
>
> The following lab will show you how to set up a new device. For this
> example, we will set up a Nokia Lumia 920 with dimensions 480 x 800.

51. From the TestComplete menu, open the **Tools** menu and select
    **Current Project Properties**.

52. In the left-hand tree-view, select **Open Applications \| Web
    Testing \| Virtual Browsers**. This step will display all of the
    current virtual browsers (see the screenshot below).

![](./media/image238.png){width="5.985in" height="3.255in"}

53. Click the **Add\...** button.

54. In the **Add Virtual Browser** dialog, paste the user agent string
    (see below), then click the **Next** button.

> Mozilla/5.0 (compatible; MSIE 10.0; Windows Phone 8.0; Trident/6.0;
> IEMobile/10.0; ARM; Touch; NOKIA; Lumia 920)

55. Enter the screen dimensions as 480 x 800 and click the **Next**
    button. Note that the prompt is for \"CSS pixels\". Typically, the
    browser and device screen dimensions are identical. In some cases,
    the physical device screen may have more pixels than the browser
    screen.

![](./media/image239.png){width="4.152938538932633in"
height="2.46875in"}

56. Enter a browser name that will show up in the **Name** column of the
    **Virtual Browsers**

> list and click the **Finish** button.

![](./media/image240.png){width="3.1820078740157482in"
height="2.041874453193351in"}

> The next time you record a test, the new entry will show in the
> drop-down list and will be available for keyword and script tests to
> use.

![](./media/image241.png){width="4.161839457567804in"
height="2.7083333333333335in"}

> []{#Android .anchor}**Android**
>
> If you need greater control of an Android device than [[Mobile
> Web]{.underline}](#Mobile_Web) testing in a browser can provide,
> TestComplete has two solutions. For the best control but requiring
> knowledge of how to program an Android application, configure an [Open
> Android Application]{.underline}. This will open up the gates to an
> Android application\'s internal objects, sensors, GPS, operating
> system commands and so on. If you don\'t have access to the source,
> you can still use [[ Image Based Testing]{.underline}](\l) to access
> on-screen objects using image recognition. TestComplete image
> recognition handles differences between devices, resolutions, even
> minor variations in pixels and colors.

#### The Mobile Screen

> The **Mobile Screen** is the primary tool for testing physical
> devices. It is a device emulator with mobile testing capabilities and
> an interface used to record keyword and script tests. The Mobile
> Screen allows you to interact with a variety of devices in a
> standardized UI, create mobile checkpoints, add images to \"image
> sets\", take screenshots, record multi- touch gestures and install
> [Android Agent]{.underline} for use in \"white box\", [Open
> Android]{.underline} [Applications]{.underline}. The Mobile Screen can
> emulate devices hooked up through USB, Android SDK emulators and
> virtual machines running the Android OS (such as Oracle\'s
> VirtualBox).

![](./media/image242.jpeg){width="2.6758562992125983in" height="5.61in"}

> **Note**: The Mobile Screen connects only to devices hooked up via USB
> cable or some emulation of USB. Wi-Fi connections are not supported.
>
> You should interact with the Mobile Screen using keyboard, mouse or
> touchpad, rather than directly with the physical device. The only
> exception is that *gestures*, input involving multiple touches, are
> performed directly on a device.
>
> To get started using the Mobile Screen, click the **Show Mobile
> Screen** button that appears on the Test Engine toolbar.

![](./media/image243.png){width="3.008513779527559in"
height="0.3879155730533683in"}

> If no device is connected, you\'ll get a warning. If there\'s only a
> single device available it will connect and run. If multiple devices
> are connected, the **Select Current Device** window displays. You can
> **Connect** to a single device or **Connect All**. The screenshot
> below shows a connected physical Samsung device (\"SCH-I535\") and an
> Android SDK emulator. After connecting, display the Mobile Screen by
> selecting a device and clicking the **OK** button.

![](./media/image244.png){width="3.9846970691163603in"
height="2.856561679790026in"}

> The Mobile Screen user interface consists of a toolbar, a link to
> **Install TestComplete Agent**, the emulated screen and a footer that
> contains buttons that emulate hardware on the device. The toolbar is
> shown in the screenshot below.

![](./media/image245.png){width="5.067001312335958in"
height="2.0833333333333335in"}

> The **Size** button gives you a slider that resizes the emulated
> device\'s screen area and a
>
> **Best Size** link to get the optimal match between the device and the
> Mobile Screen.

![](./media/image246.jpeg){width="2.678590332458443in"
height="3.6093744531933507in"}

> **Record** and **Play** [[Gestures]{.underline}](#gestures) buttons
> allow you to test using complex, multiple touches on the device. See
> the [[Gestures]{.underline}](#gestures) topic for more on recording
> and playing gestures.
>
> [[Mobile Checkpoints]{.underline}](#mobile-checkpoints) allows you to
> take a snapshot of the device\'s screen for later comparison. This
> checkpoint option depends strictly on visual comparison.
>
> The **Add Image** button allows you to add an image to [[Image
> Sets]{.underline}](#image-based-testing).
>
> The **Select Device** drop down list lets you select the device that
> should show in the Mobile Screen.
>
> **Take Screenshot** records the emulated screen as a .bmp or .png
> image.
>
> [Install Android Agent]{.underline} loads a package on the device that
> exchanges data with open Android application and retrieves data from
> sensors on the device.
>
> The Mobile Screen footer emulates standard hardware buttons on the
> device. From left to right, the buttons are **Back**, **Home**,
> **Menu**, **Volume Down**, **Volume Up**, and **Power**.

![](./media/image247.jpeg){width="2.3546314523184604in"
height="0.29302055993000875in"}

#### Using TestedApp to Manage Packages

> Packages contain Android application definitions in the form of .apk
> files. You can install and launch these applications in TestedApps,
> keyword tests and scripts.
>
> You can define a package in a **TestedApp** and run the TestedApp from
> the TestComplete IDE, from a Keyword Test or from script. To create a
> TestedApp representing an Android Package:

1.  In the Project Explorer, Select, the **TestedApps** node.

![](./media/image248.png){width="2.279501312335958in"
height="2.18625in"}

2.  In the TestedApps editor, right-click and select **Add Android
    Application\...** from the context menu.

![](./media/image249.png){width="4.227226596675416in"
height="4.630311679790026in"}

3.  Define the path for the **Android application package file**. The
    path will point to the location of the .apk file on your local PC
    where TestComplete resides or in a shared network location. Select
    the **Deploy to the device on start** checkbox then click the **OK**
    button.

![](./media/image250.png){width="5.573920603674541in" height="3.7125in"}

4.  Now that you have defined the TestedApp, right-click the item and
    click **Run Selected**

> from the context menu.

![](./media/image251.png){width="5.905713035870516in"
height="4.102916666666666in"}

> The package will be loaded to the default device and will also show in
> the Mobile Screen. If the package was already loaded to the device it
> will be *refreshed*, that is, it will be deleted and reloaded to the
> device.
>
> For more on how to run a TestedApp from the IDE, keyword test or
> script, see the [[Running]{.underline}](#running-a-testedapp) [[a
> TestedApp]{.underline}](#running-a-testedapp) topic.

#### Using Keyword Tests to Manage Packages

> If you want to install an Android package and then run that package in
> a separate step, leave the TestedApp **Deploy to the device on start**
> option unchecked. The **Install Package** keyword operation from the
> **Mobile** group will load the package to the device without having to
> run it. The screenshot below shows the **Install Package** operation
> followed by the **Run Tested App** operation from the **Test Actions**
> group.

![](./media/image252.png){width="5.917707786526684in"
height="0.5606244531933509in"}

#### Managing Devices with Keyword Tests

> The **Mobile** group in the keyword test editor has methods and
> properties for all devices connected to TestComplete on your PC.

![](./media/image253.png){width="2.141907261592301in" height="3.4375in"}

> Mobile actions are run either on a device that you specify from a list
> or are applied to the *current device*. The **Select Device**
> operation specifies the current device that all future operations
> should run on. The **Parameterized Device** option allows you to
> select both a device *and an index* (assuming there are multiple
> devices with the same name). Choose the device from the **Select
> Device** dialog list and then click **Finish**.

![](./media/image254.png){width="4.6886734470691165in"
height="2.8256244531933508in"}

> To run the same operations against multiple devices, by drag the
> **Device Loop** operation onto the keyword test. This will display the
> **Device Loop** dialog to either Iterate through All **Connected
> Devices** or choose from a list using the **Iterate Through Specific
> Devices** option. Each iteration of the loop makes one of the
> connected devices the current device.

![](./media/image255.png){width="4.621738845144357in"
height="2.7395833333333335in"}

> With access to a device, you can run operations to [install and run
> packages on the device](#using-keyword-tests-to-manage-packages),
> touch the device surface, send keystrokes, [[touch
> images]{.underline}](#using-image-sets-in-keyword-tests) and [[play
> gestures]{.underline}](#gestures). The screenshot example below uses
> the **Image Touch** operation to open the Clock application, then
> performs a series of **Device Touch** operations to navigate to the
> world clock tab, add a city and use the **Device Keys** operation to
> enter \"San Francisco\".

![](./media/image256.png){width="5.928935914260717in"
height="1.0817705599300087in"}

##### Using the On-Screen Action

> The **Mobile** section has a sampling of general-purpose operations,
> but the **On-Screen Action** operation of the **Test Actions** group
> allows you to access the very powerful **Mobile Device** object. The
> Device goody bag includes properties for all device\'s information,
> access to the **Desktop** object that represents the device\'s screen,
> **GPS** and **Sensor** objects, simulate an **SMS**, and the ability
> to **Drag**/**Swipe**/**Touch**/**TouchAndHold**/
> **TouchPress**/**TouchRelease**. You can also execute Android shell
> commands and even **Reboot** the device. The screenshot below shows
> some of the methods for the **Mobile.**
>
> **Device()** object.

![](./media/image257.png){width="5.879571303587052in"
height="5.15625in"}

> The **On-Screen Action** operation dialog provides help with the
> parameters so you don\'t have to guess values. For example, the
> **PressButton** method expects a predefined button value. If you
> happen to know that **mbkHome** constant is actually a 4, then all is
> well. But selecting from a drop-down list is easier and more reliable.
> The screenshot below shows the mbkHome key constant being selected
> from a list.

![](./media/image258.png){width="3.318231627296588in"
height="1.8768744531933508in"}

#### Image Based Testing

> You can\'t always count on having a prepared, \"white-box\"
> application that is open and lets you easily get at all the controls
> on-screen. You won\'t always have that kind of access. In these cases,
> you can test based on recognizing images. A series of objections pop
> to mind, like \"what about devices that have different sizes and
> resolutions?\", \"if I change color scheme or theme, will the image
> recognition fail?\", and \"will colors bleeding through transparent
> areas of images fool the image recognition?\" TestComplete has
> intelligent mechanisms to recognize images in all of these situations,
> including variable percentages of pixel variation and transparency.
>
> The heart of the approach is the **ImageRepository** in the Project
> Explorer. The ImageRepository has **Image Sets** where each set
> contains multiple images representing a single on-screen object. The
> screenshot below shows the ImageRepository node with two image sets
> named \"Calculator\" and \"HomeScreen\".

![](./media/image259.png){width="2.2128324584426946in"
height="1.4025in"}

> Let\'s say you want to automate a clock icon on your device\'s home
> screen. The icon may be displayed using more than one image, depending
> on manufacturer and operating system version. Resolution can also
> vary, for example, when displayed by a Samsung Galaxy running in
> 720x1280 pixels vs. an HTC One running in 540x960. By using an Image
> Set you can recognize images for any configuration. The screenshot
> below shows the \"HomeScreen\" in the **Image Set Editor** where the
> clock is listed under **Items** on the left-hand side. The **Image
> Strip** at the bottom of the screen has a high-quality image of the
> clock from a device with 720x1280 resolution and another image taken
> from the emulator that only runs at 240x320. The resolutions are
> different, the actual artwork representing the clock is different, and
> the scary part is that the background colors are different based on
> the chosen wallpaper.
>
> When using a Keyword Test or script to reference the Clock object,
> TestComplete looks through the Image Strip and tries to match the
> image with the application under test. If it doesn\'t find the image,
> TestComplete moves to the next image in the strip and tries again.
> This mechanism handles varying resolutions and even helps recognize
> objects that use completely different artwork to represent the object.

![](./media/image260.jpeg){width="5.886568241469816in"
height="4.574998906386702in"}

> What if the wallpaper on the device changes or there is some variation
> in the pixel quality between devices? The **Image Parameters** section
> of the Image Set Editor allow tolerance of color or pixel variations.
> **Color tolerance** accepts a number between 0..255 where zero (the
> default) requires that colors match the stored image exactly and 255
> where pixels of any color are treated as identical. **Pixel
> Tolerance** is the number of pixels that can different from the stored
> Image Strip item. By default, Pixel Tolerance is 0 and all pixels in
> the tested application and the Image Strip item must match exactly.
> The slider below the Pixel tolerance spinner allows you to quickly set
> the percentage of pixel difference that will be allowed, without
> having to know about the number of pixels in the image.

##### Adding Images

> You can conveniently add new images to an Image Set by clicking the
> **Add Image** button on [[The Mobile
> Screen]{.underline}](#the-mobile-screen).

![](./media/image261.jpeg){width="2.278601268591426in"
height="1.1653116797900263in"}

> The **Add Image to Image Repository** dialog will display. After a few
> moments, a second window labeled **Select Object from Screen** will
> display. Use the mouse to surround a rectangular area. Click the
> **Select** button that appears to save the area to the **Add Image to
> Image Repository** dialog. You can change this selected area later.

![](./media/image262.jpeg){width="1.6205785214348207in"
height="1.4128116797900263in"}

> Provide an **Item name** to be used in scripts and keyword tests. Also
> select an image set from the drop-down list. If you need to retake the
> image, click the **Select Image\...** button. Click the **Finish**
> button to create a new item in the Image Set.

![](./media/image263.jpeg){width="5.927136920384952in"
height="5.958333333333333in"}

> The image will be added as an item to the Image Set editor. Notice the
> **Script line** at the bottom of the Image Set editor dialog that
> provides sample script showing how to programmatically touch the
> selected image.

![](./media/image264.jpeg){width="5.972109580052494in" height="4.17in"}

> You can add more images to the strip for the Image Set item by
> right-clicking and selecting **Add Image\...** or **Add Image From
> File\...** from the context menu. Use the **Set Recognition
> Parameters\...** context menu option to tweak color or pixel
> tolerances.

![](./media/image265.jpeg){width="5.915094050743657in" height="2.75in"}

> The Image Set Editor **Item Parameters** panel will display and allow
> you to change the **Item name**. You can change the Item name at any
> time, but if keyword tests or scripts refer to it, you will need to
> update those to match the new item name. The **Composite control**
> checkbox, when selected, use the exact coordinates of the selection.
> This checkbox should be selected when the control is composed of
> several smaller controls, such as a date-time picker or a tabbed
> control. For simple controls like buttons and check boxes, leave the
> option unchecked so that selection will occur at the exact center of
> the control.

![](./media/image266.png){width="2.6124037620297464in"
height="1.1240616797900262in"}

> The **Preview** panel shows the current selected Image Strip item and
> has two important rectangular regions (see screenshot below). The
> *initial target area* is the rectangle you first define when adding
> the image and is defined by a gray rectangle. The red rectangle
> defines the *recognition area* used when attempting to match the image
> set to the on- screen image being tested. You can drag the handles of
> the recognition area to refine your selection and omit problematic
> parts of the screen or right-click to drag the recognition area
> rectangle to a new location. In tests, the upper left corner of the
> initial target area is used as a reference point when touch actions
> have coordinates passed to them. Otherwise, the center of the
> recognition area is used for touch actions.

![](./media/image267.jpeg){width="2.0213024934383204in"
height="2.0109372265966754in"}

##### Using Image Sets in Keyword Tests

> Use the **Image Touch** operation from the **Mobile** group in the
> **Operations** window to simulate a touch action on an on-screen
> object. This will display the **Image Touch** dialog. Select the
> **Image Set** from the drop-down list and the item from the list, then
> click **Finish**. **Note**: The default touch action will press the
> center of the recognition area, but you can optionally click the
> **Next** button instead of Finish and supply X and Y coordinates or
> specify the index of the device.

![](./media/image268.png){width="5.62338801399825in" height="4.33125in"}

##### Mobile Checkpoints

> Mobile checkpoints use Image Sets to verify the state of the
> application. If an Image Set item is found in the tested application,
> the checkpoint passes. The setup for the example that follows uses
> images taken from the Calculator application as shown in the
> screenshot below.

![](./media/image269.jpeg){width="2.675910979877515in"
height="5.548124453193351in"}

> The example uses an Image set populated from the Calculator with
> sufficient image to multiply 12x12. The Image set also includes an
> image of the result \"= 144\".

![](./media/image270.jpeg){width="5.86129593175853in"
height="3.845832239720035in"}

> The **Create Mobile Checkpoint** dialog displays in response to a new
> keyword **Mobile Checkpoint** operation or by clicking the **Create
> Mobile Checkpoint** option from the recording toolbar. Your options
> are to **Create a new item** or to **Use an existing item**. The
> **Create a new item** option brings up essentially the same dialog as
> used for [[Adding]{.underline}](#adding-images)
> [[Images]{.underline}](#adding-images) to an image set. If you choose
> the **Use an existing item**, select an image from the list of Image
> Repository items and click the **Finish** button.

![](./media/image271.png){width="5.589114173228347in"
height="5.73375in"}

##### Mobile Checkpoints in Keyword Tests

> The test uses the calculator to multiply 12 x 12 and verifies that the
> result is an image of 144.

![](./media/image272.png){width="4.880765529308836in"
height="2.134687226596675in"}

#### Gestures

> *Gestures* represent multiple touch events. Gestures must be recorded
> on a touch-sensitive physical device; emulators cannot be used to
> record gestures. The Mobile Screen has a Record Gesture feature that
> allows you to record multiple touches on your device.
>
> Clicking the **Record Gesture** button on the Mobile Screen first
> prompts to add an **Android Gesture Collection** if a collection
> doesn\'t already exist. Then the **Add Gesture** dialog displays
> announcing that you can record gestures on your physical device. Once
> the dialog displays, the Mobile Screen is disabled and will display
> the message \"Use a physical device to record gestures\". Enter a name
> for the gesture, then touch your physical device to simulate
> multi-touch events. When you\'re done, click the **Stop Recording**
> button.

![](./media/image273.jpeg){width="5.329616141732283in"
height="4.379374453193351in"}

> TestComplete has a rather nifty way of graphically representing the
> movement of points touched on the device by animating each point in a
> unique color. The screenshot below shows the results of a pinching
> gesture using thumb (shown in red) and index finger (shown in green).
> Double-click the **Name** or **Playback Acceleration** column entries
> to edit them. The Playback Acceleration percentage value can be set
> between zero and 100. By default, acceleration is set to 10% for
> better accuracy. Click the **Play Gesture** button to select a
> recorded gesture and run it.

![](./media/image274.png){width="5.152462817147857in"
height="3.155624453193351in"}

##### Playing Gestures from Keyword Tests

> To play a recorded gesture from a keyword test, drag the **Play
> Gesture** operation onto the editor. Select an item from the Gesture
> collection drop down if necessary and then select a gesture from the
> list.

![](./media/image275.png){width="4.513636264216973in"
height="3.4479166666666665in"}

[]{#Xamarin_Open_Apps_Testing .anchor}

> **Summary**
>
> This chapter explored TestComplete mobile testing mechanisms including
> how to test mobile web applications that may have multiple layouts
> based on screen dimension, \"black-box\" native Android applications
> where you don\'t have access to the application\'s internals and
> \"white-box\" native Android applications that are open to inspection.

### Web Services Testing

13. []{#Web_Services_Testing .anchor}**Web Services Testing**

> **Objectives**
>
> This chapter discusses web services in general and looks at
> TestComplete support for testing web services. You\'ll learn how to
> import a web service and call a web service function directly in a
> test. You\'ll use Web Services Checkpoint and XML Checkpoint to verify
> results between test runs.
>
> []{#_bookmark230 .anchor}**Overview of Web Services**
>
> Web Services provide a standardized SOAP based mechanism for calling
> functions across a network of computers where the remote computer
> executes the specified routine and returns the results. From the
> calling computer a request is made using the SOAP protocol and the web
> service provided will execute the function specified and return the
> result.

![](./media/image276.jpeg){width="3.0108311461067365in"
height="1.5365616797900263in"}

> **Figure 194 \--Diagram of a Web Services Call**
>
> SOAP stands for Simple Object Access Protocol and is a standardized
> format for calling functions on remote computers.
>
> In order to work with Web Services, you must have access to a WSDL
> (Web Services Description Language) document that describes the
> available functions, their parameters and results. By importing the
> WSDL document into TestComplete, Web Services calls can be made using
> the Web Services checkpoint.
>
> You can use Web Services to supply data used in a test or you can test
> a Web Service itself. Web Services can be used directly from Keyword
> Tests or Script and the results used as just another data source.
>
> []{#Web_Service_Example .anchor}**Web Service Example**
>
> First, let\'s take a look at a sample web service that contains a
> number of math related functions. The web service is located at this
> URL:
>
> [http:*//training.falafel.com/testcompletews/*](http://training.falafel.com/testcompletews/)
>
> Using a web browser to hit the above URL, you can see a listing of the
> available functions provided by the web service. A link to the WSDL
> document (the link that reads \"Service Description\" in the
> screenshot below) describes the structure of each request and
> response. If you click on the \"Service Description\" link you will
> see the WSDL XML document that fully describes the web service.

![](./media/image277.png){width="5.906447944006999in" height="2.9325in"}

> **Figure 195 \--Sample Web Service**
>
> Not all web services frameworks provide a page like the one above that
> allows a user to examine each function call individually. In many
> cases you will only have a WSDL link pointing to the XML document
> describing the available functions and data types.
>
> []{#Importing_a_Web_Service .anchor}**Importing a Web Service**
>
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

### Distributed Testing

14. []{#_bookmark242 .anchor}**Distributed Testing**

> **Objectives**
>
> This chapter looks at TestComplete Distributed Testing features and
> illustrates how you can use this feature to leverage multiple machines
> during test execution. You'll learn how to create projects for use in
> distributed testing and how to make them available to remote machines.
> You\'ll also explore some of the issues with executing and
> synchronizing tests on multiple computers.

About the Network Suite
-----------------------

> Distributed tests are executed using the Project Explorer. To enable
> Distributed Testing within a project it is necessary to add the
> **Network Suite** Project Item. The Network Suite contains sub-nodes
> allowing you to configure which tests will execute and on which
> machines. The machine running the Distributed Test functions as a
> heads-up display, allowing you to monitor the status of the machines
> participating in the test.
>
> All of the machines participating in a Distributed Test must be using
> the same version of TestComplete.

#### Single Machine Test Execution

> To get a better understanding of how Distributed Testing works let\'s
> first take a look at how a single project works on one machine. In the
> illustration below we can see a single machine connected to a source
> code repository running a project where tests are executed locally.

![](./media/image304.jpeg){width="5.932162073490813in"
height="1.8525in"}

> **Figure 219 \--Single Project Executing on a Single CPU**
>
> In this setup the machine running TestComplete (or TestExecute) pulls
> the project source files from the repository and executes the test.
> Because the tests run synchronously, the total runtime is one hour.

#### Multiple Machine Test Execution

> Now, let\'s look at the same test run in a Distributed Testing
> environment using the Network Suite. In the illustration below, we see
> a single driver machine running a copy of TestComplete which controls
> test execution on multiple host machines running either TestComplete
> or TestExecute. All of the machines have access to the project, which
> contains the Network Suite Project Item, from the repository. In this
> setup the total running time of the project takes only 15 minutes as
> each machine executes different tests within the project.

![](./media/image305.jpeg){width="5.924021216097988in"
height="3.3881244531933508in"}

> **Figure 220 \--Running Parts of a Project Across Multiple Machines**
>
> In fact, this example illustrates just one scenario for Distributed
> Testing where all of the machines execute tests from a single project.
> However, tests can be executed from any project that has the Network
> Suite Project Item and do not have to be related in any significant
> way. TestComplete Distributed Testing features allow testers to tailor
> test execution to cover a wide variety of scenarios.

Setting up a Distributed Test
-----------------------------

> In this section we\'ll create a project with a simple test that we can
> execute using Distributed Testing. First, we\'ll use the recorder to
> create a basic test then modify the Project to add support for
> Distributed Testing.
>
> Our focus here is creating and configuring a Distributed Test,
> therefore we\'re going to record a very simplistic test for
> illustration purposes only.

#### Recording a Simple Test Case

63. Select **File \| New \| Project\...** and click the **OK** button on
    the Create Project dialog.

64. Right click the **TestedApps** node and select **Add \| New
    Item\...** Using the Add Tested Application dialog select
    \"C:\\Windows\\System32\\Notepad.exe\".

![](./media/image306.png){width="5.105459317585302in"
height="4.541666666666667in"}

> **Figure 221 \--Adding a TestedApp**

65. Double click the **TestedApps** node to open the editor in the
    Workspace.

66. Change the File Path for \"Notepad\" to %SystemRoot%\\System32\\
    using an environment variable to ensure the test will work on any
    Windows machine.

![](./media/image307.png){width="4.87323053368329in"
height="0.45937445319335085in"}

> **Figure 222 \--Change the File Path to use an Environm ent Variable**

67. Click the Record button on the recording toolbar.

68. Using the TestedApps drop down button start \"Notepad\".

![](./media/image308.jpeg){width="3.3686362642169727in"
height="1.2684372265966755in"}

> **Figure 223 \--Running Notepad**

69. In the Notepad main window type \"this is a test\".

70. On the Notepad main window select **File \| Exit** and click the
    **No** button on the confirmation dialog.

#### Configuring the Project for Distributed Testing

> We now have a test that will execute on any remote machine so let\'s
> add the **Network Suite** Project Item and configure our test to run
> on a remote system.

1.  Right click the Project node in the Project Explorer and select
    **Add \|New Item\...** from the context menu.

2.  In the Create Project Item dialog select **NetworkSuite**.

![](./media/image309.png){width="4.584633639545057in" height="4.0625in"}

> **Figure 224 \--Creating the Netw ork Suite Project Item**
>
> This adds the following nodes to our Project:

![](./media/image310.jpeg){width="5.651023622047244in"
height="1.8975in"}

> **Figure 225 \--Netw orkSuite nodes**
>
> Now we can begin to add Hosts and Jobs to our Network Suite to
> construct a Distributed Test.

#### Working With Hosts

##### Adding Hosts

> Under the **NetworkSuite**, **Hosts** are machines that will execute
> as part of a Distributed Test. From the **Project Explorer** you can
> double click the **Hosts** node to view the Hosts editor window in the
> Workspace and all of the hosts configured for the Distributed Test
> will appear in the list.
>
> To add a Host to the NetworkSuite:

1.  Right click the Hosts node and select **Add \| New Item\...** from
    the context menu. On the Create Project Item dialog specify \"LAB1\"
    for the Name field and click the **OK** button.

![](./media/image311.png){width="4.584633639545057in" height="4.0625in"}

> **Figure 226 \-- Adding a Host**

2.  In the Hosts Editor, set the **Address** column to the IP address or
    use the ellipsis to choose the machine by network name.

3.  Under the **Base Path** column assign a path relative to the Host
    machine (we\'re using \"C:

> \\Temp\" in this case).

4.  Under the **Source Path** column assign the file path to the
    Project\'s .MDS file.

![](./media/image312.png){width="4.889529746281715in"
height="0.408332239720035in"}

> **Figure 227 \--Setting the IP address, Base Path and Source Path**

##### Hosts Editor Columns

> The Hosts Editor has the following columns:

  **Column**       **Description**
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Name**         The name used to refer to the host from scripts, keyword tests and from the task properties.
  **Address**      The network name or IP address of the computer that the new host is mapped to.
  **Login Mode**   The Manual option requires the remote machine to be logged into before running the test. The Automatic RDB Session connects to the remote computer using Remote Desktop and leaves the computer locked and unavailable to users. The Automatic RDB Session connects to the remote computer using Remote Desktop but moves the session to the remote computer\'s console, leaving the computer unlocked and available for use.
  **Domain**       Specifies the domain to which the user specified in the User name column belongs.
  **User name**    Specifies the account used to open a user session on the slave computer automatically when verifying or running the network suite.
  **Password**     Specifies the password used to open a user session on the slave computer automatically when verifying or running the network suite. If the parameter is skipped, TestComplete will use an empty string.

  **Column**        **Description**
  ----------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Base path**     Specifies the common path for several projects, which are located on the computer specified by the Address property. TestComplete uses this value to prefix paths specified by a task's Path property.
  **Source path**   Specifies the path to the folder (located on the master computer) holding the slave project that can be copied from the master computer to the host computer. The path should be relative to the master computer.

> There are several other useful items available from the context menu
> on the Hosts Editor including

![](./media/image313.png){width="5.678537839020122in"
height="2.65625in"}

> **Figure 228 \--Hosts Editor Context Menu**

##### Verifying the Host Connection

> Due to the fact that remote machines may not be configured properly,
> TestComplete provides an option to verify the connection to a Host
> machine. You can use the context menu **Verify** option from the
> **Host Editor** as well as the **Project Explorer** context menu on
> the **Hosts** node.

![](./media/image314.png){width="3.7453094925634294in"
height="2.4166666666666665in"}

> **Figure 229 \--Verifying a Host connection**
>
> Refer to TestComplete online help for Firewall configuration details.

##### Copying the Project to the Host

> Now that we\'ve verified the connection and setup our project we can
> copy it to the host machine to prepare for execution. Once we finish
> configuring our test we may want to perform this step again to ensure
> all of our updates are on the Host machine. In practice, tests should
> be stored in a source control repository and loaded onto the host
> machines from there.
>
> 1\. Right click the \"LAB1\" host entry in the Hosts Editor window and
> select **Copy Project to Slave** from the context menu.

![](./media/image315.png){width="4.986001749781277in"
height="3.0104166666666665in"}

> **Figure 230 \--Copying the project to the Host (Slave) machine**

##### Other Remote Tasks

> Also, be aware that you can restart the remote computer by
> right-clicking and choosing
>
> **Reboot** from the context menu.

![](./media/image316.png){width="5.0948862642169725in"
height="4.59375in"}

> **Figure 231 \--Rebooting the Rem ote Machine**
>
> The **Run State** tab of the NetworkSuite editor displays information
> about the network suite, job or task execution. The **Remote Desktop**
> column actually shows you the window of the slave/host computer as it
> runs. The window displays in the resolution of the master computer.

#### Tasks Editor Window

> The columns in the Tasks Editor are as follows:

  **Column**   **Description**
  ------------ ---------------------------------------------------------------------------------
  **Active**   Specifies whether the task will be run when the job, to which it belongs, runs.

+-----------------------------------+-----------------------------------+
| **Column**                        | **Description**                   |
+===================================+===================================+
| **Name**                          | The name that is used to refer to |
|                                   | the task in tests.                |
+-----------------------------------+-----------------------------------+
| **Host**                          | The name of a computer where the  |
|                                   | project will be run.              |
+-----------------------------------+-----------------------------------+
| **Path**                          | The path to the TestComplete      |
|                                   | project or project suite which    |
|                                   | the task will run.                |
+-----------------------------------+-----------------------------------+
| **Test**                          | Specifies the test item to be     |
|                                   | executed by the task. There is a  |
|                                   | specific syntax for this string   |
|                                   | which is documented in            |
|                                   | TestComplete online help.         |
+-----------------------------------+-----------------------------------+
| **Tag**                           | Specifies an arbitrary string     |
|                                   | associated with the given task.   |
+-----------------------------------+-----------------------------------+
| **Action after run**              | Specifies what TestComplete will  |
|                                   | do after it finishes executing    |
|                                   | the task on the Host computer.    |
|                                   |                                   |
|                                   | Available options in the          |
|                                   | drop-down list are:               |
|                                   |                                   |
|                                   | > \[None\] - Do nothing (do not   |
|                                   | > close TestComplete or           |
|                                   | > TestExecute either). Use this   |
|                                   | > value in combination with the   |
|                                   | > Use value for the Use previous  |
|                                   | > instance option in order to     |
|                                   | > reduce the workload of the      |
|                                   | > remote computer. In this case,  |
|                                   | > after finishing the task the    |
|                                   | > TestComplete (TestExecute)      |
|                                   | > instance on the remote host     |
|                                   | > will not be closed and it will  |
|                                   | > be used for running the next    |
|                                   | > task.                           |
|                                   | >                                 |
|                                   | > \[Close\] - Close the           |
|                                   | > TestComplete (TestExecute).     |
|                                   | > Default value. \[Shut Down\] -  |
|                                   | > Shut down the Host computer.    |
|                                   | >                                 |
|                                   | > \[Reboot\] - Reboot the Host    |
|                                   | > computer.                       |
+-----------------------------------+-----------------------------------+

+-----------------------------------+-----------------------------------+
| **Column**                        | **Description**                   |
+===================================+===================================+
| **Copy remote log**               | Specifies whether and in which    |
|                                   | cases TestComplete should copy    |
|                                   | the remote log of the task        |
|                                   | execution to the master computer. |
|                                   | This property is only meaningful  |
|                                   | if the project specified by the   |
|                                   | Path property is located on a     |
|                                   | computer other than the master    |
|                                   | computer.                         |
|                                   |                                   |
|                                   | Available options in the          |
|                                   | drop-down list are:               |
|                                   |                                   |
|                                   | > \[Always\] - TestComplete       |
|                                   | > copies the results to the       |
|                                   | > master computer at the end of   |
|                                   | > the task execution. Copying     |
|                                   | > results increases the task      |
|                                   | > execution time and uses some    |
|                                   | > disk space, but you can review  |
|                                   | > the results at any time, even   |
|                                   | > if the remote computer is not   |
|                                   | > available. Copied results are   |
|                                   | > kept on your computer until you |
|                                   | > delete them.                    |
|                                   | >                                 |
|                                   | > \[When status is not OK\] -     |
|                                   | > TestComplete copies the results |
|                                   | > to the master computer only if  |
|                                   | > the log on the task execution   |
|                                   | > includes errors and/or          |
|                                   | > warnings.                       |
|                                   | >                                 |
|                                   | > \[Do not copy\] - The task      |
|                                   | > results remain on the remote    |
|                                   | > computer. To view them, you     |
|                                   | > must have access to the results |
|                                   | > folder. Storing results on the  |
|                                   | > remote computer saves disk      |
|                                   | > space on your computer, but you |
|                                   | > may not be able to view them,   |
|                                   | > since the remote computer can   |
|                                   | > be offline or the results       |
|                                   | > folder may be inaccessible.     |
+-----------------------------------+-----------------------------------+

+-----------------------------------+-----------------------------------+
| **Column**                        | **Description**                   |
+===================================+===================================+
| **Use previous instance**         | Specifies whether TestComplete    |
|                                   | will close the remote             |
|                                   | TestComplete (or TestExecute)     |
|                                   | process before executing the      |
|                                   | task.                             |
|                                   |                                   |
|                                   | Available options in the          |
|                                   | drop-down list are:               |
|                                   |                                   |
|                                   | > \[Use\] - Use the running       |
|                                   | > instance of the remote          |
|                                   | > TestComplete (TestExecute). Use |
|                                   | > this value in combination with  |
|                                   | > the None value for the Action   |
|                                   | > after run option in order to    |
|                                   | > reduce the workload of the      |
|                                   | > remote computer. In this case,  |
|                                   | > after finishing the task, the   |
|                                   | > TestComplete (TestExecute)      |
|                                   | > instance on the remote host     |
|                                   | > will not be closed and it will  |
|                                   | > be used for running the next    |
|                                   | > task.                           |
|                                   | >                                 |
|                                   | > \[Show Error\] - Display the    |
|                                   | > error message. Default value.   |
|                                   | >                                 |
|                                   | > \[Terminate\] - Reboot the      |
|                                   | > remote TestComplete             |
|                                   | > (TestExecute) process. Use this |
|                                   | > value to ensure that the task   |
|                                   | > will not fail if previous tasks |
|                                   | > or test runs caused critical    |
|                                   | > errors in the remote            |
|                                   | > TestComplete (TestExecute)      |
|                                   | > instance.                       |
+-----------------------------------+-----------------------------------+
| **Remote application**            | Specifies what testing            |
|                                   | application, TestComplete or      |
|                                   | TestExecute, will be used on the  |
|                                   | remote workstation.               |
+-----------------------------------+-----------------------------------+

#### Synchronizing Computers

> A **SynchPoint** delays execution of a test until all computers with
> that SynchPoint reach the synchronization point. When all the
> computers with a named SynchPoint hit that Synchronize Point, they
> will continue on with their test. An example of an effective use for
> SynchPoints: you want to avoid where two or more users try to edit the
> same record at the same time and post the data.

![](./media/image317.png){width="1.7247451881014872in"
height="1.381874453193351in"}

> **Figure 232 \--SyncPoints**

##### Using SynchPoint in Keyword Tests

> To use a SynchPoint, use a **Run Code Snippet** Operation and add the
> **NetworkSuite. Synchronize()** method, passing the name of the
> SynchPoint (\"WaitForMe\" in the example).
>
> **NetworkSuite**.Synchronize(\"WaitForMe\");
> **NetworkSuite**.Synchronize(\"WaitForMe\")

Executing Distributed Tests
---------------------------

> There are several options for executing Distributed Tests including
> manually in the Project Explorer, from Keyword Tests and from Script.

#### Manual Execution

> The easiest option is to use the context menu from the Project
> Explorer. You can execute either individual Jobs or specific Tasks
> within a job directly from the context menus.

![](./media/image318.png){width="4.444857830271216in" height="4.3725in"}

> ![](./media/image319.png){width="4.776375765529309in"
> height="4.104374453193351in"}

#### Keyword Test Execution

> You can execute a Distributed Test from a Keyword Test using the Run
> Test Operation, opening up the NetworkSuite test category and
> selecting the Job or Task that you want to run.

![](./media/image320.png){width="5.776921478565179in"
height="3.6458333333333335in"}

> **Figure 233 \--Running Distributed Test**

#### Runtime Behavior

> TestComplete uses Windows Remote Desktop to display the remote
> computer as the test runs. You will need to configure your remote
> computer to accept Remote Desktop connections for the distributed test
> to work. See the documentation for your operating system for more
> information on accepting Remote Desktop connections.

![](./media/image321.jpeg){width="5.932345800524934in"
height="2.7580205599300087in"}

> **Figure 234 \--A Running Distributed Test**

Lab: Simple Distributed Test
----------------------------

#### Configure The Project

1.  Create a master project with a NetworkSuite Project Item.

2.  Create a hosted (slave) project with a **NetworkSuite** Project
    Item.

![](./media/image314.png){width="3.7453094925634294in"
height="2.4166666666666665in"}

> **Figure 235 \--Verifying the Host**

3.  Add \"Notepad.exe\" to the **TestedApps** project Item of the hosted
    project.

4.  Modify the **File Path** property of the TestedApp to **\"\"**
    (blank).

#### Record a Test

1.  Create (or record) a script method to type something into notepad.
    For example:

> **var** p1;
>
> **var** w1; TestedApps.notepad.Run();
>
> p1 = Sys.Process(\"notepad\");
>
> w1 = p1.Window(\"Notepad\", \"\*\").Window(\"Edit\"); w1.Click(135,
> 29);
>
> w1 = p1.Window(\"Notepad\", \"\*\");
>
> w1.Window(\"Edit\").Keys(\"TestComplete Training - Distributed
> Testing\"); w1.Close();
> Aliases.notepad.dlgNotepad.DirectUIHWND.CtrlNotifySink.btnDontSave.ClickButton();
>
> **Dim** p1
>
> **Dim** w1 TestedApps.notepad.Run()
>
> p1 = Sys.Process(\"notepad\")
>
> w1 = p1.Window(\"Notepad\", \"\*\").Window(\"Edit\") w1.Click(135, 29)
>
> w1 = p1.Window(\"Notepad\", \"\*\")
>
> w1.Window(\"Edit\").Keys(\"TestComplete Training - Distributed
> Testing\") w1.**Close**()
>
> Aliases.notepad.dlgNotepad.DirectUIHWND.CtrlNotifySink.btnDontSave.ClickButton()

2.  Save the project.

#### Create the Distributed Test

1.  Select the **NetworkSuite** Project Item in the Master Project and
    enter the path to the project suite in the **Shared Path**.

2.  Expand the **Hosts** Project Item and select \"Host1\"

3.  Enter the name (or IP address) of the hosting (slave) computer.

4.  In the **Base** path property enter \"\\\\\<Master Computer
    Name\>\\\<Name of Project Suite directory\>\"

5.  Right-click on \"Host1\" and select **Verify** from the context
    menu.

6.  Expand the **Jobs** Project Item.

7.  Expand the \"Job1\" Project Item.

8.  Select the \"Task1\" Project Item.

9.  In the **Path** property enter \"\\\<Name of Hosted
    Project\>\\\<Name of Hosted Project\>. mds\".

10. In the **Copy remote log** property select \"\[Always\]\". 11.In the
    **Use previous instance** property select \"\[Use\]\".

<!-- -->

12. In the **Test** property enter the path to your test on the hosted
    machine. If you\'re running a Keyword Test then the path might be
    similar to \"\<Name of Hosted
    Project\>\\KeywordTests\\Test1\\Test1\". If running a Script then
    the path would look something like this path: \"\<Name of Hosted
    Project\>\\Script\\Unit1\\Test1\".

13. Right-click \"Task1\" and select **Verify** from the context menu.

14. Right-click the **NetworkSuite** project item and select **Run**
    from the context menu.

Summary
-------

> In this chapter, we looked at how TestComplete can distribute testing
> to remote machines. We looked at the structure of distributed tests
> and discussed why they can be beneficial.
>
> We also recorded a simple test and examined the necessary steps to
> execute the test in a distributed environment.

### Manual Testing

Manual Testing
==============

Objectives
----------

> This chapter looks at TestComplete support for Manual Testing
> including how to create, edit and execute Manual Tests. You\'ll learn
> about the upgrade path from manual to automatic tests using the
> TestComplete import and export features. You\'ll also learn how to use
> events within a manual test to allow interaction between manual and
> automated tests.

[]{#_bookmark267 .anchor}

About Manual Testing
--------------------

> If you've worked in any sort of Quality Assurance capacity you\'ll
> likely be intimately familiar with manual testing and perhaps more so
> than you might like. Manual testing while extremely valuable can be
> difficult for humans to perform consistently over long periods of time
> because of human nature itself. Manual testing generally takes a great
> deal of concentration and dedicated effort to consistently produce
> results. TestComplete provides an alternative to what could be
> considered the more classical approach of using Microsoft Word or
> Excel. TestComplete support for manual testing allows the test
> developer to guide the tester through a series of steps, capture data
> as the test is being performed and automatically log the results of
> the test. The benefits of manual testing through TestComplete are:
>
> The assurance that the required steps are followed Generation of a log
> file for every test execution Verification of the results based on
> Test Log contents Ability to interact with a manual test using Events
>
> Below is an example of the TestComplete manual test user interface:

![](./media/image322.png){width="5.947606080489939in" height="2.9425in"}

> **Figure 236 \--The TestComplete Manual Testing User Interface**

Creating Manual Tests
---------------------

> In this topic we\'ll walk through the process of creating a Manual
> Test in TestComplete.

71. Select **File \| New \| New Project\...** and click **OK** on the
    **Create New Project** dialog.

72. Right click the **Project** node in the **Project Explorer,** select
    **Add \| New Item\...** and choose **Manual Tests**.

![](./media/image323.png){width="3.4336461067366577in"
height="3.0468744531933507in"}

> **Figure 237 \-- Creating the Manual Tests Project Item**

73. Click **OK** on the **Create Project Item** dialog.

74. Right click the **ManualTests** node in the Project Explorer and
    select **Add \| New Item\...**

> to create a new Manual Test.

75. On the **Create Project Item** dialog enter \"CreateOrder\" as the
    name of the manual test and click **OK** to open the Manual Test
    Editor.

![](./media/image324.png){width="3.405962379702537in"
height="1.7806244531933508in"}

> **Figure 238 \--Creating the Manual Test Item**

#### Manual Test Editor

> The TestComplete Manual Test Editor allows for the creation of a
> multi-step test that prompts the user through a series of
> instructions, collecting results with every step.

![](./media/image325.png){width="5.929561461067366in"
height="3.8906244531933507in"}

> **Figure 239 \--Manual Test Editor**

#### Manual Test Editor Controls

  **Field**               **Description**
  ----------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------
  **Test Steps**          Tree of the steps contained within this test, used for navigation while editing.
  **Test Caption**        Window caption of the Manual Test dialog.
  **ID**                  Step ID for use within Manual Test events.
  **Test Description**    Sub caption of the Manual Test dialog.
  **Test Instructions**   Free-form HTML markup for communicating the actual actions to be performed during the test. Appears in the main portion of the Manual Test dialog.

  **Field**                     **Description**
  ----------------------------- -----------------------------------------------------------------------------
  **Test notes and comments**   Notes for the test writer that are not displayed when the test is executed.

#### Editing the Test Description

> By default, the **Manual Test Editor** opens with only the initial
> node created so we\'ll need to add steps to fill out the test. To
> create a Manual Test description:

1.  Click the **Test Caption** field and enter \"Create Order Manual
    Test\".

2.  Edit the **Test Description** field and set the text to \"In this
    test we will create a new customer order and validate a new record
    is created.\"

3.  Edit the **Test Instructions** field and set the test to \"Using the
    Orders sample application we will add a new order and verify the
    data appears in the list of customer orders.\" The result should
    look like the following:

![](./media/image326.png){width="5.93113188976378in" height="3.88125in"}

> **Figure 240 \--The Manual Test Editor w ith Test Description**

#### Adding Steps

> Once the description is completed we can start adding steps to the
> test as follows:

1.  Click the green (+) sign or right click in the Test Steps area and
    select **New Step** from the context menu.

![](./media/image327.png){width="3.112386264216973in"
height="1.7221872265966753in"}

> **Figure 241 \--Adding a new step to the Manual Test**

2.  Fill out the Step **Caption**, **Description** and **Instructions**
    for this step of our Manual Test. The actual information can be
    arbitrary or you can use the screenshot below to guide you.

![](./media/image328.png){width="5.941329833770778in"
height="4.523748906386702in"}

> **Figure 242 \--Completed Manual Test**

3.  Add one more manual step and fill out the Step **Caption**,
    **Description** and **Instructions**

> for this step

#### Running Manual Tests

> Keyword Tests can run Manual Tests using the **Test Actions \| Run
> Test** Operation. From the **Select Test** dialog, select the **Manual
> Test** you want to run from the Keyword Test.

![](./media/image329.png){width="5.901175634295713in" height="3.52in"}

> **Figure 243 \--Selecting a Test**

Manual Test Interaction With Automated Tests
--------------------------------------------

> In this topic we\'ll illustrate how manual tests interact with
> automated tests. You can call a manual test from a Keyword Test or
> Script. The reverse is also true. You an call Keyword Tests or Script
> from your manual test.
>
> You might be thinking \"Why would I do this?\" which is a fair
> question. The interesting thing about Manual Tests in TestComplete is
> that you can augment a test by performing actions automatically for
> the user and by incorporating a Manual Test into a Keyword Test or
> Script you can execute any actions necessary to ease the testing
> process such as setup test data, create/delete files, launch
> applications etc. You can also replace parts of your manual test
> incrementally as circumstances dictate, allowing you to move over to
> automated testing in a controlled manner.

#### Running Keyword Tests from Manual Tests

> Not only can you kick off a Manual Test from a Keyword Test, you can
> also run Keyword Tests from your Manual Test. For example, if on
> \"STEP\_2\", you need the tester to start the \"Orders\" application,
> you can have this done automatically from the keyword test. The
> screenshot below, shows the original manual step that requires the
> user to type a certain path into the Run dialog.

![](./media/image330.jpeg){width="5.950694444444444in"
height="3.7583333333333333in"}

> **Figure 244 \--The Manual Test Step**
>
> Use the **Content type** drop down list to select \"Keyword Test\".
> Use the Keyword Test entry ellipses to select an existing Keyword Test
> from a list. When you run the manual test and it reaches this step,
> the manual test dialog will disappear briefly while the Keyword Test
> runs.

![](./media/image331.png){width="5.892280183727034in"
height="3.121874453193351in"}

> **Figure 245 \--Step Uses Keyw ord Test Content Type**

#### Converting Manual Tests to Keyword Tests

> TestComplete provides extensive support for converting your existing
> manual tests to automated Keyword Tests. There are two related
> functions on the Test Steps toolbar that help you to convert from
> manual to Keyword Tests.

![](./media/image332.jpeg){width="2.90873687664042in"
height="0.9902077865266842in"}

> The **Convert Manual Test to Keyword Test** option launches the
> recorder and creates a keyword test for all your manual test steps.
> The nice thing about this approach is that you can read off the manual
> test step as you record the Keyword Test. The recorder starts and
> stops for each manual test step. Once the recording is complete, a
> prompt asks if you want a Keyword Test created that will call the
> Keyword Tests created for each step. The result looks something like
> this in the Keyword Test Editor:

![](./media/image333.png){width="4.979998906386702in"
height="1.7118744531933507in"}

> **Figure 246 \--Manual Test Converted to Keyw ord Test**
>
> The **Convert Manual Step to Keyword Test** option launches the
> recorder and creates a Keyword Test with the same name as the manual
> test step. Once the recording is complete, you can change the Content
> Type to \"Keyword Test\" and the new Keyword Test will be
> automatically selected.

#### Manual Test Event Handling

> One of the unique features TestComplete brings to manual testing is
> the ability for a test developer to inject actions into the test while
> it\'s being performed. For example, if you wanted to initialize some
> test data, delete certain files or perform Checkpoint validation of
> test data, all of those actions can be performed using the built-in
> Manual Test Events.

![](./media/image334.png){width="4.835881452318461in"
height="3.8854166666666665in"}

> **Figure 247 \--Manual Test Events provided by TestComplete**

Exporting a Manual Test
-----------------------

> Once you\'ve created a manual test you\'re given two options to export
> the test content using the context menu to either Microsoft Word or
> HTML:

![](./media/image335.png){width="3.47748687664042in"
height="4.145833333333333in"}

> **Figure 248 \--Exporting Manual Tests**
>
> TestComplete provides an option to customize the Microsoft Word export
> template on the Properties tab at the bottom of the editor window. The
> export functionality works in a mail merge like fashion and allows you
> to create a Microsoft Word document containing the contents of the
> test.

![](./media/image336.jpeg){width="5.900073272090989in"
height="4.368124453193351in"}

> **Figure 249 \--Manual Test Editor Properties tab**
>
> You can optionally, define your own Microsoft Word template for use
> with the TestComplete export feature. TestComplete includes a default
> template that looks like this:

![](./media/image337.jpeg){width="5.943008530183727in"
height="4.045416666666667in"}

> **Figure 250 --TestComplete Default Microsoft Word Template**

Importing a Manual Test
-----------------------

> The ability to migrate existing legacy manual tests can be a huge time
> saver. TestComplete lets you import manual tests stored in text files,
> Microsoft Word or Microsoft Excel files. TestComplete can handle
> several format arrangements:
>
> One level or multilevel, bulleted or numbered lists. Numbered lists
> can use any number style and formatting for levels.
>
> Test steps using different indents for steps of different levels.
> Tables used to organize the step hierarchy.
>
> Keywords to separate the step caption, description, instructions and
> notes.
>
> TestComplete ships with a set of sample files that can be imported.
> Each file demonstrates a particular format, e.g. text, Excel, Word
> document with headers, etc. The closer your files are to the example
> formats, the less editing you will need to perform in the Manual Tests
> editor. See the online help for complete details on supported formats.
>
> You can find example files to import at:
>
> \\TestComplete Samples\\Manual Testing\\Recommended Formats for Manual
> Test Instructions

#### Simple Text File Import

> If you open the document titled \"Test Instructions in .txt file.txt\"
> you will see steps for testing the Orders application that use numbers
> to indicate each step.

![](./media/image338.png){width="5.492455161854768in"
height="4.28125in"}

> **Figure 251 \--Sample Text File**
>
> If you open the document titled \"Test Instructions in .doc file
> (using headings).doc" you will see steps for testing the Orders
> application that uses the \"Heading1\" style to indicate a new step.

![](./media/image339.jpeg){width="5.929838145231846in" height="5.16in"}

> **Figure 252 \--Sam ple Im port Docum ent**
>
> Test steps can even be arranged in a hierarchy by using styles, i.e.
> \"Heading1\", \"Heading2\", where \"Heading2\" represents the set of
> steps indented from \"Heading1\".
>
> See the TestComplete online help topic \"Importing Manual Tests\" for
> detailed formatting information for each document type.

#### Lab

> Let\'s walk through importing one of the sample documents.

1.  From the TestComplete **File** menu choose **Import \| Test\...**

![](./media/image340.png){width="4.528034776902887in"
height="2.6770833333333335in"}

> **Figure 253 \-- Selecting the Im port Test Option**

2.  In the **Import Test Options** page of the wizard, enter the **Test
    Name** as \"OrdersTest\". Click the ellipses of the **Source File
    Name** and locate the \"Test Instructions in .doc file (using
    headings).doc\" file in the path indicated at the top of this topic.
    Click the **Next** button to continue.

![](./media/image341.png){width="6.199589895013124in"
height="3.0954166666666665in"}

> **Figure 254 \-- Import Test Options**

3.  The wizard will take a moment to process the file and then present a
    summary. Click the

> **Finish** button to close the wizard.

![](./media/image342.png){width="6.191743219597551in"
height="3.037916666666667in"}

> **Figure 255 \--Import Summary**

4.  The imported manual test will show under the ManualTests node in the
    Project Explorer, and all steps described in the document will be
    included in the ManualTests editor.

![](./media/image343.jpeg){width="6.200479002624672in"
height="3.7989577865266844in"}

> **Figure 256 \--The Imported Manual Test**

Legacy Migration
----------------

> The ability to import legacy manual test steps stored in external
> files coupled with TestComplete tools for converting Manual Test to
> fully automated Keyword Tests comprises a complete migration path.
> This path takes you from the labor-intensive, error prone and
> inconsistent to a wholly automated system that can be run reliably on
> a schedule.

Summary
-------

> In this chapter, we explored TestComplete Manual Testing features and
> discussed the advantages of developing manual tests using
> TestComplete. We learned to:
>
> Create, edit and execute Manual Tests. Call Manual Tests.
>
> Use Events within a Manual Test. Import and Export Manual Tests.

### Low Level Procedures

Low Level Procedures
====================

Objectives
----------

> This chapter explains TestComplete Low Level Procedure functionality
> and how it can be leveraged to deal with situations where they may be
> no easy alternative. You'll learn how to record, edit and execute Low
> Level Procedures. Along the way you will learn how Low-Level
> Procedures differ from standard test recordings, when to use a
> Low-Level Procedure and the difference between Window and Screen Low
> Level Procedures.

About Low Level Procedures
--------------------------

> Low Level Procedures are an alternative recording type provided by
> TestComplete where actual mouse and keyboard events are recorded. Low
> Level Procedures differ dramatically from standard recordings where
> TestComplete records higher level actions against specific onscreen
> objects.

#### Low Level Procedure Types

> There are two kinds of Low Level Procedures:
>
> **Screen Coordinates** \-- Captures events relative to the entire
> screen where the top left-hand corner of the screen is 0,0.
>
> **Window Coordinates** \-- Captures events relative to a user selected
> Window where the top left-hand corner of the window is 0,0.
>
> Window Coordinate Low Level Procedures tend to be more reliable as
> they are unaffected by the location of the selected window and will
> playback relative to the Window\'s current screen location.

#### When To Use Low Level Procedures

> From the outset, tests that rely on screen coordinates generally are a
> bad idea and usually that holds true regardless of which tool you're
> using. However, in certain situations you may find yourself attempting
> to record a scenario that simply refuses to playback properly due to
> the complexity of capturing a user\'s intent via a recorder. In these
> cases, resorting to Low Level Procedures can, at the very least, serve
> as a stop-gap until alternative solutions can be developed.
>
> Additionally, you can work on applications using third party controls
> not directly supported by TestComplete and that provide no visibility
> into the client region of the control such as a custom grid.

Recording Low Level Procedures
------------------------------

> In the \"Web Testing\" chapter we looked at a Web application that
> used JavaScript to dynamically display menu items on screen. The
> application poses an interesting challenge for GUI recorders that tend
> to capture interactions with controls such as clicks and keystrokes.
> Let\'s take a look at recording a Low-Level Window Coordinates
> Procedure to handle the menu selection and understand this alternative
> approach to recording.

#### Low Level Window Coordinates Procedure

76. For starters we\'ll launch Internet Explorer and browse to the
    Orders application located here:

> [http:*//training.falafel.com/dynamiccontent*](http://training.falafel.com/dynamiccontent)

77. Select **File \| New \| Project\...** and on the **Create Project**
    dialog click the **OK** button.

78. Start recording a new test. From the Recorder toolbar, drop down the
    Low Level Procedure button and select the **Record Low-Level
    Procedure (window coordinates)** option.

![](./media/image344.png){width="5.204438976377952in"
height="1.11375in"}

> **Figure 257 \--Recording a Low-Level Procedure**

79. A red selection rectangle will appear. Move the rectangle onto
    Internet Explorer and click the left mouse button to select it.

![](./media/image345.jpeg){width="2.1676990376202974in"
height="1.8046872265966754in"}

> **Figure 258 \--Selecting IE**

80. On the **Create Project Item** dialog click **OK** to add the
    **Low-Level Procedures Collection** item to the project.

![](./media/image346.png){width="4.311887576552931in"
height="2.0315616797900264in"}

> **Figure 259 \--Adding the Low-Level Procedures Collection**

81. On the **Create Project Item** dialog click **OK** to add a
    Low-Level Procedure to the project.

![](./media/image347.png){width="4.301522309711286in"
height="2.0315616797900264in"}

> **Figure 260 \--Adding a Low-Level Procedure**

82. Select the **Add \| New \| Customer \| Orders** menu item on the web
    page.

![](./media/image348.png){width="3.5686811023622047in"
height="2.2395833333333335in"}

> **Figure 261 \--Selecting from a Dynamic Menu**

83. Click the **Stop** button on the recording toolbar.

#### Examining the Recording

> At the completion of the recording you can see that a \"LLCollection\"
> has been added in the Project Explorer. Inside the collection will be
> the Low-Level Procedure you recorded.

![](./media/image349.png){width="1.9227165354330709in"
height="1.3303116797900263in"}

> **Figure 262 \--The Low-Level Procedure Collection**
>
> Next, look at the **Low-Level Procedure Editor** and the events
> captured by the Low-Level Procedure. Double click the **Advanced \|
> LLCollection1 \| LLP1** node from the **Project Explorer**.

![](./media/image350.png){width="3.6925984251968504in"
height="2.4791666666666665in"}

> **Figure 263 \--Low Level Procedure Editor**
>
> The columns in the Low-level Procedure Editor are:

  **Column**   **Value**
  ------------ ------------------------------------------
  **Icon**     Indicator of the type of event performed
  **N**        Ordinal value of this event in the list
  **Event**    Type of action to be performed

  **Column**       **Value**
  ---------------- --------------------------------------
  **Parameters**   Data specific to the specified event
  **Delay, ms**    Delay in milliseconds between events

> From the Low-level Procedure Editor window you can add, edit and
> delete events from the list using the right click context menu.

![](./media/image351.png){width="3.6925984251968504in"
height="2.4791666666666665in"}

> **Figure 264 \--The Editor Window Context Menu**
>
> The Edit Event dialog provides options to customize all facets of the
> captured event.

![](./media/image352.png){width="2.61334864391951in"
height="1.8459372265966754in"}

> **Figure 265 \-- The Edit Event Dialog**

Calling Low Level Procedures from Keyword Tests
-----------------------------------------------

> To run a Low-Level Procedure from a Keyword Test, use the **Call
> Object Method** Operation. Specify the collection (code insight will
> drop down a list of available objects), followed by a period \".\",
> then the name of the low level procedure, another period \".\" and
> finally the **Execute()** method.

![](./media/image353.png){width="2.039296806649169in"
height="1.1653116797900263in"}

> **Figure 266 \--Specifying an Object**
>
> To have the low-level procedure work in relation to a particular
> window, pass the window as a parameter to the Execute () method. It\'s
> also a good idea to make sure the window you're working with is
> activated and in front of the other windows. You can do this with the
> Run Code Snippet operation as shown in the screenshot below.

![](./media/image354.png){width="2.195365266841645in"
height="1.1653116797900263in"}

> **Figure 267 \--Activating a Window**

Summary
-------

> In this chapter, we looked at TestComplete Low Level Procedure
> capabilities and: Explained how this recording type differs from a
> standard object-based recording Recorded a scenario which otherwise
> requires special handling
>
> Examined the Low-Level Procedure Editor

### User Forms

User Forms
==========

Objectives
----------

> This chapter demonstrates how User Forms are used to display dialogs
> and windows onscreen during test execution. You\'ll learn how to use
> the TestComplete User Form\'s designer to create your own forms.
> You\'ll also see how modal and non-modal display modes manage form
> display during test execution.

[]{#Materials .anchor}

Using the Designer
------------------

> User Forms are not part of the default project template so you\'ll
> first need to add the **User Forms** Project Item to your project.
> Once you\'ve added User Forms support to your project you can right
> click the User Forms node in the Project Explorer and add a form to
> your project. In this example, we\'ll construct a User Form that can
> be used to prompt for login credentials.

![](./media/image355.png){width="2.613190069991251in"
height="1.8356244531933508in"}

> **Figure 268 \--User Forms Login Dialog**
>
> Once the form is created you will see the User Forms designer which is
> similar in style to those seen in Visual Basic, Visual Studio or other
> development tools supporting forms development. If you are familiar
> with any of these tools you\'ll immediately feel right at home in the
> designer. If not, don\'t fear. Learning the designer is quick and easy
> and you\'ll be able to construct dialogs in no time.

#### Layout of the User Forms Designer

> There are three panels of the User Forms editor including:

84. Component palette

85. Form Designer

86. Properties window

![](./media/image356.png){width="5.950223097112861in"
height="3.9459372265966755in"}

> **Figure 269 \--User Form s Editor**

#### Building a User Form

> To illustrate the functionality of the User Forms designer we\'ll
> build a Login dialog that you can call from within your tests. If the
> UserForms node doesn\'t already exist in the project explorer,
> right-click the project and select **Add \| New Item**. Choose \"User
> Forms\" from the list and click **OK** to create the project item.

![](./media/image357.png){width="4.3459667541557305in"
height="3.5833333333333335in"}

> **Figure 270 \--Adding User Form s**
>
> To create the form, right click the Project Explorer **UserForms**
> node and select **Add \| New Item\...** In the **Name** edit box enter
> \"PasswordDlg\".

![](./media/image358.png){width="4.312343613298338in"
height="1.9903116797900262in"}

> **Figure 271 \--Adding a User Form**
>
> Using the Component palette, we\'ll add the components (TcxTextEdit,
> TcxLabel and TcxButton) from the **Editors**, **Helpers** and
> **Buttons** categories respectively to the form by simply double
> clicking the components. After adding a component to the design-time
> form you can use the mouse to move/size the control and the Properties
> window to change its appearance/behavior. We now have a form that
> looks like this:

![](./media/image359.png){width="5.926007217847769in"
height="2.900624453193351in"}

> **Figure 272 \--Initial User Forms Layout**
>
> Next, we need to make the following property changes on the components
> placed on the form. The table below lists the components and the
> property/values for each. These changes improve the appearance of the
> dialog as well as set the expected behavior of a modal login dialog.

  **Component**   **Property**          **Value**
  --------------- --------------------- -------------
  cxTextEdit1     Name                  edUsername
                  Text                  (blank)
  cxTextEdit2     Name                  edPassword
                  Text                  (blank)
                  Properties.EchoMode   eemPassword
  cxLabel1        Caption               &Username:
                  FocusControl          edUsername

  **Component**   **Property**   **Value**
  --------------- -------------- ------------
  cxLabel2        Caption        &Password
                  FocusControl   edPassword
  cxButton1       Caption        OK
                  Default        True
                  ModalResult    mrOk
  cxButton2       Caption        Cancel
                  Cancel         True
                  ModalResult    True
  \[User Form\]   Caption        Login

> Once these properties have been assigned we\'ll have a completed User
> Form that we can use from within a Keyword Test.

![](./media/image360.png){width="5.915184820647419in"
height="3.1755205599300087in"}

> **Figure 273 \--The Com pleted Form**
>
> []{#Calling_User_Forms_in_a_Keyword_Test .anchor}**Calling User Forms
> in a Keyword Test**
>
> User Forms can be displayed from within a Keyword test using several
> different operations such as **Call Object Method**, **Run Code
> Snippet**, or **Run Script Routine**. In this example we\'ll use the
> **Call Object Method** operation and illustrate how to invoke a modal
> dialog and respond to the user\'s action to the dialog.

#### Creating a Keyword Test to call a User Form

> The first step is to drag/drop a **Call Object Method** onto a Keyword
> test. This will invoke the wizard to select the object and choose the
> specific method. In the case of a User Form there are two methods for
> displaying the form, Show and ShowModal. The prior will display the
> form as a non-modal window and test execution will continue to the
> next operation. The latter will display the form as a modal window
> where a user has to respond to the dialog prior to test execution
> continuing. The ShowModal method returns a value called ModalResult
> representing the user\'s response to the dialog. The ModalResult will
> be one of the following values:

  **Constant**     **Description**
  ---------------- ----------------------------------
  **mrNone**       None.
  **mrOk**         The dialog result is OK.
  **mrCancel**     The dialog result is Cancel.
  **mrAbort**      The dialog result is Abort.
  **mrRetry**      The dialog result is Retry.
  **mrIgnore**     The dialog result is Ignore.
  **mrYes**        The dialog result is Yes.
  **mrNo**         The dialog result is No.
  **mrAll**        The dialog result is All.
  **mrNoToAll**    The dialog result is No To All.
  **mrYesToAll**   The dialog result is Yes To All.

> For this operation, we\'ll specify the **UserForms.PasswordDlg**
> object:

![](./media/image361.png){width="4.550780839895013in"
height="2.4270833333333335in"}

> **Figure 274 \--Specifying a UserForm s Object**
>
> Clicking **Next** will display a list of the methods on the
> UserForms.PasswordDlg object including the **ShowModal** method. Type
> ShowModal to select the method then click the **Finish** button (the
> ShowModal method accepts no parameters).

![](./media/image362.png){width="5.524841426071741in"
height="3.9895833333333335in"}

> **Figure 275 \--Calling Show Modal**

#### Responding to a User Form

> Once displayed onscreen using the ShowModal method, the user must
> respond to the dialog prior to the test proceeding. The Keyword Test
> will need to respond to the ModalResult returned by the form. We can
> use an **If\...Then** operation to provide the logic. For the login
> dialog we\'ll inspect the form\'s ModalResult, username and password,
> validate the data and perform additional actions based on the result.
> All of these values can be inspected within a single **If\...then**
> operation.
>
> To respond to the User Form:

1.  Drag and drop the **If\...Then** operation just after the call the
    User Form.

2.  Under **Value1** use the ellipsis, set the **Mode** to **Last
    Operation Result**.

3.  Under **Value2** use the ellipsis, set the **Mode** to **Code
    Expression** and enter **mrOk** as the

##### Value.

4.  Click the **And** button to add a new row.

5.  Under **Value1** use the ellipsis, set the **Mode** to **Code
    Expression** and enter

##### UserForms.PasswordDlg.edUsername.Text.

6.  Under **Value2** use the ellipsis, set the **Mode** to **Constant**
    and \"admin\" (without the quotes) as the **Value**.

7.  Under **Value1** use the ellipsis, set the **Mode** to **Code
    Expression** and enter

##### UserForms.PasswordDlg.edPassword.Text.

8.  Under **Value2** use the ellipsis, set the **Mode** to **Constant**
    and \"**password**\" (without the quotes) as the **Value**.

![](./media/image363.png){width="5.6358497375328085in" height="2.75in"}

> **Figure 276 \--Specifying an If..Then Condition**
>
> Nested within the **If\...Then** operation we\'ll add a Log Message
> operation to indicate we\'ve logged in.

1.  Select the **Logging** category from the Operations palette and drag
    & drop the **Log Message** operation below the **If\...Then**
    operation.

![](./media/image364.png){width="6.206896325459318in"
height="3.3333333333333335in"}

> **Figure 277 \--Adding a Log Message Operation to the If\...Then**

2.  On the **Log Message** dialog type **\"**Logged In\" on the
    **Message** tab and click the **Finish**

> button.

3.  Click the **Right** arrow button on the Keyword toolbar to indent
    the **Log Message** step.

![](./media/image365.png){width="4.00501312335958in"
height="0.6329155730533683in"}

> **Figure 278 \--Indenting**
>
> We\'ve completed the logic for our User Form. The **Log Message**
> operation will be called if the correct user name and password are
> entered.
>
> []{#_bookmark303 .anchor}**Summary**
>
> In this chapter, we learned how to create user forms for input during
> test execution. We learned about the User Forms designer and how to
> incorporate user forms into a test.

### Best Practices

18. []{#Best_Practices .anchor}**Best Practices**

> **Objectives**
>
> This chapter includes real-world advice on how to plan, organize and
> version control your tests. Other handy tips tell you how to get the
> most out of \"smoke tests\" and how to communicate your test results
> with the team.
>
> []{#Communicating_Test_Results .anchor}**Communicating Test Results**
>
> Now you might be thinking \"huh? I haven\'t even started yet and I
> have to think about communicating my results?\" The answer is a
> resounding YES! Unfortunately, Quality Assurance and test automation
> specifically, at least in the software world, tends to get a bad rap.
> Creating solid test automation that can stand up over time and provide
> valuable ongoing feedback is a difficult task which leads a lot of
> people (read management) to think time and effort spent working on
> automation is wasted.
>
> To solve this problem, you'll want to focus on getting your test
> results published quickly and consistently to prove that your efforts
> are worth the investment. TestComplete provides some facilities for
> producing log output though you'll want to be sure and iron out your
> strategy from the start. For example, you may want to setup a web
> server where you can publish results. In fact, TestComplete supports
> exporting log results to HTML which could be a good starting place.
>
> []{#Plan_your_testing,_but_not_that_kind_of_ .anchor}**Plan your
> testing, but not that kind of planning\...**
>
> The preparation we\'re referring to has to do with your choice of
> testing tool, TestComplete. Although it\'s important to plan the
> application features to be tested, it\'s also important to be prepared
> with respect to the testing facilities available in TestComplete. You
> should gain a thorough understanding of TestComplete features before
> you embark on writing test automation to avoid a situation where your
> weeks into test development only to discover a feature that could have
> saved you numerous hours or days.
>
> TestComplete is rich with features that make test automation easier
> although like any development tool it provides many different ways to
> solve the same problem. For example, TestComplete has a powerful and
> indeed almost alluring recorder, making it easy to quickly create
> automated tests. While a test recorder is a great tool, recorded tests
> tend to be more brittle than hand written tests because they capture a
> single iteration at a given point in time and don\'t take into account
> unexpected events like an error dialog popping up. The alternative is
> handwritten tests where you can methodically plan how the test will
> react in unexpected circumstances. The down side of handwritten tests
> is they tend to take longer to develop though over the long run
> they\'ll likely require less maintenance because of the tendency to
> design the test more rigorously.
>
> []{#Organizing_your_TestComplete_Projects .anchor}**Organizing your
> TestComplete Projects**
>
> TestComplete provides the ability to customize the Project Items that
> are included by default on a new project using Project Templates. In
> order to maintain consistency across your testing organization you
> should work towards creating a project template(s) that\'s
> pre-configured for your test environment. For example, if you\'re
> testing a Window 32-bit GUI application, create a Project Template
> that has the Tested Applications node with your application already
> added to it. Also, look closely at how you can utilize Aliases to
> avoid using long dotted object names like:
>
> Sys.Process(\"iexplore\").IEFrame(0).Window(\"WorkerW\", \"\",
> 1).Window( \"ReBarWindow32\", \"\", 1).Window(\"ComboBoxEx32\", \"\",
> 1).Window(
>
> \"ComboBox\", \"\", 1).Window(\"Edit\", \"\", 1)
>
> TestComplete includes an automatic Name Mapping feature has been added
> to make this even easier.
>
> []{#Use_a_Source_Control_Repository .anchor}**Use a Source Control
> Repository**
>
> TestComplete is a development tool and as such the projects, scripts,
> data, etc. used in your tests should be kept under version control. If
> this is something you\'re already doing, skip ahead. If not, you
> should consider version control the next priority and work to get your
> test suites under version control. There are lots of options including
> some excellent Open Source projects which are freely available like
> Subversion, otherwise known as SVN. While it\'s beyond the scope of
> this document to discuss the specific merits of source control it\'s a
> subject that shouldn\'t be ignored.
>
> []{#Your_Most_Important_Test .anchor}**Your Most Important Test**
>
> Arguably, the first test you should focus on is a \"smoke test\". In
> this section we\'ll discuss what a smoke test is and provide guidance
> as to how to construct the test in such a way as to maximize its
> effectiveness.

#### Creating a Smoke Test

> Probably the most important test you\'ll write is your Smoke Test, at
> least it should be. Typically, the goal of a Smoke Test is to verify
> that the latest build delivered to QA is either worth further
> consideration or \"DOA\" (dead on arrival). The smoke test is crucial
> because of the time savings it can provide both R&D and QA. A good
> Smoke Test should:
>
> Run quickly \-- a smoke test should not last for hours but minutes and
> test the most crucial functionality.
>
> Fail quickly \-- as soon as a failure is detected in the smoke test
> should end and trigger a failure notification.
>
> Cover a broad range of functionality, focusing on breadth not depth.
> Require minimal setup/configuration of the application under test. Be
> setup to run against every build.
>
> Adapt over time as the application under test evolves. Serve as a
> model for new test automation.
>
> If you take the time to organize your Smoke Test to cover these goals
> you will undoubtedly save time and resources over the long run. Your
> Smoke Test should serve as a model that embodies your \"best
> practices\" from which your QA team can draw from for their own tests.
>
> If you\'ve never written a Smoke Test before, start small. In the
> beginning simply get the smoke test to verify even a single piece of
> functionality consistently. Over time, work to increase its coverage
> but remain focused on the quality of the test. It\'s unacceptable to
> have a Smoke Test that can\'t run consistently and without problems.

#### Executing your Tests Regularly

> Once your Smoke Test is written and under version control the next
> step is to automate its execution. SmartBear has a product called
> Automated Build Studio which can automate your TestComplete tests and
> trigger them to execute when a new build is delivered to QA, a process
> called **Continuous Integration** or **\"CI\"**. In addition to
> Automated Build Studio there are Open Source CI servers such as
> CruiseControl.NET.
>
> The main benefit of a CI server is to reduce the amount of time it
> takes to execute your test automation as well as ensure that it
> executes against every build. By setting up a CI server you can not
> only free your QA engineers from having to manually execute their
> tests. CI helps quickly identify tests that are unable to consistently
> run to completion and may require closer scrutiny. In addition, many
> CI servers include a means of publishing test results providing for
> greater visibility into the automation efforts.
>
> []{#General .anchor}**General**
>
> The following are general tips and best practices to help you get the
> most out of TestComplete:
>
> Record/Playback is a quick and easy way to get automated tests up and
> running but tend to be brittle leading to problems when the
> application changes, etc.
>
> Use the TestItems of the project as a framework for Test Cases (see
> the \"Project Organization\" chapter).
>
> Separate Data from the Test Framework (see \"Data Driven Testing\").
>
> Use the code metrics of the Code Explorer to improve the quality of
> the script code (see Overview of TestComplete).
>
> Use reusable routines whenever possible (see the \"Project
> Organization\" chapter). Keep routines short, i.e. less than a page of
> code.
>
> Use meaningful variable names. The default variable names of a
> recording are not acceptable for production use.
>
> []{#Web_Page .anchor}**Web Page**
>
> The following are tips for making effective use of TestComplete when
> testing web pages:
>
> Make sure that \"Make the Page object a child of the browser process\"
> is selected in the Project properties under **Open Applications \| Web
> Testing**.
>
> Use the \"Tree Model\" for best performance. You can set this under
> the Project properties in the General options.
>
> []{#Summary .anchor}**Summary**
>
> In this chapter you learned how to plan, organize and version control
> your tests. You also reviewed tips on how to get the most out of
> \"smoke tests\" and how to communicate your test results with the
> team.

### Appendix A - Cheat Sheet

19. []{#Appendix_A_-_Cheat_Sheet .anchor}**Appendix A - Cheat Sheet**

> **Keyboard Shortcuts**
>
> **Global Shortcuts** (keys that work when TestComplete is running even
> if TestComplete does not have focus)

  **Command**              **Default Key**
  ------------------------ -----------------
  Pause script execution   SHIFT-10
  Fix Information          SHIFT-CTRL-A
  Record                   SHIFT-F1
  Stop                     SHIFT-F2
  Run                      SHIFT-F3
  Pause recording          SHIFT-F11
  Low Level Record         SHIFT-F4

> **Key Mapping** (keys that work when TestComplete has focus, generally
> in the editors)

  **Command/Section**   **Default**   **Visual Studio**   **Borland Classic**
  --------------------- ------------- ------------------- ---------------------
  **Debugging**                                           
  Run                   F9            F5                  F9
  Reset                 CTRL-F2       SHIFT-F5            CTRL-F2
  Step Over             F8            F10                 F8
  Trace Into            F7            F11                 F7
  Run to Cursor         F4            F4                  F4
  Switch Breakpoint     F5            F9                  CTRL-F8

  **Command/Section**     **Default**      **Visual Studio**   **Borland Classic**
  ----------------------- ---------------- ------------------- ---------------------
  View Evaluate           CTRL-F7          CTRL-F2             CTRL-F4
  View Call Stack         CTRL-ALT-S       ALT-7               CTRL-ALT-S
  View Watches            CTRL-ALT-W       ALT-3               CTRL-ALT-W
  View Break Points       CTRL-ALT-B       CTRL-B              CTRL-ALT-B
  **Project/Units**                                            
  Close Page              CTRL-F4          CTRL-F4             ALT-F3
  Save Unit               CTRL-S           CTRL-S              CTRL-S
  Open Project            CTRL-F11         CTRL-SHIFT-0        CTRL-F11
  New Project                              CTRL-SHIFT-N        
  Save All                                 CTRL-SHIFT-S        CTRL-SHIFT-S
  Display previous page   CTRL-SHIFT-TAB   CTRL-SHIFT-TAB      CTRL-SHIFT-TAB
  Display next page       CTRL-TAB         CTRL-TAB            CTRL-TAB
  **Cursor movement**                                          
  Cursor Left             LEFT             LEFT                LEFT
  Cursor Right            RIGHT            RIGHT               RIGHT
  Beginning of Line       HOME             HOME                HOME
  End of Line             END              END                 END
  Up one line             UP               UP                  UP
  Down one line           DOWN             DOWN                DOWN

+-----------------+-----------------+-----------------+-----------------+
| **Command/Secti | **Default**     | **Visual        | **Borland       |
| on**            |                 | Studio**        | Classic**       |
+=================+=================+=================+=================+
| Up one page     | PGUP            | PGUP            | PGUP            |
+-----------------+-----------------+-----------------+-----------------+
| Down one page   | PGDN            | PGDN            | PGDN            |
+-----------------+-----------------+-----------------+-----------------+
| Beginning of    | CTRL-HOME       | CTRL-HOME       | CTRL-PGUP       |
| Document        |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| End of Document | CTRL-END        | CTRL-END        | CTRL-PGDN       |
+-----------------+-----------------+-----------------+-----------------+
| Move to word    | CTRL-LEFT       | CTRL-LEFT       | CTRL-LEFT       |
| before          |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Move to word    | CTRL-RIGHT      | CTRL-RIGHT      | CTRL-RIGHT      |
| after           |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| **Delete        |                 |                 |                 |
| operations**    |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Delete          | DEL             | DEL             | DEL             |
| character at    |                 |                 |                 |
| cursor          |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Delete          | BACKSPACE       | BACKSPACE       | BACKSPACE       |
| character       |                 |                 |                 |
| before cursor   |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Delete current  | CTRL-Y          | CTRL-SHIFT-L    | CTRL-Y          |
| line            |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Delete previous | CTRL-BACKSPACE  | CTRL-BACKSPACE  | CTRL-BACKSPACE  |
| word            |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Delete next     | CTRL-T          | CTRL-DEL        | CTRL-T          |
| word            |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| **Miscellaneous |                 |                 |                 |
| **              |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Indent selected | CTRL-SHIFT-I    | CTRL-SHIFT-I    | CTRL-SHIFT-I    |
| block           | **or** TAB      |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Unindent        | CTRL-SHIFT-U    | CTRL-SHIFT-U    | CTRL-SHIFT-U    |
| selected block  | **or**          |                 |                 |
|                 |                 |                 |                 |
|                 | SHIFT-TAB       |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Toggle insert/  | INS             | INS             | INS             |
| overwrite mode  |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+

+-----------------+-----------------+-----------------+-----------------+
| **Command/Secti | **Default**     | **Visual        | **Borland       |
| on**            |                 | Studio**        | Classic**       |
+=================+=================+=================+=================+
| Undo            | CTRL-Z **or**   | CTRL-Z **or**   | ALT-BACKSPACE   |
|                 | ALT- BACKSPACE  | ALT- BACKSPACE  |                 |
+-----------------+-----------------+-----------------+-----------------+
| Redo            | SHIFT-CTRL-Z    | SHIFT-CTRL-Z    | ALT-SHIFT-      |
|                 | **or**          | **or**          | BACKSPACE       |
|                 |                 |                 |                 |
|                 | ALT-SHIFT-      | ALT-SHIFT-      |                 |
|                 | BACKSPACE       | BACKSPACE       |                 |
+-----------------+-----------------+-----------------+-----------------+
| Print           | CTRL-P          | CTRL-P          | CTRL-P          |
+-----------------+-----------------+-----------------+-----------------+
| Scroll display  | CTRL-UP         | CTRL-UP         | CTRL-W          |
| up one line     |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Scroll display  | CTRL-DOWN       | CTRL-DOWN       | CTRL-Z          |
| down one line   |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Display context | ALT-F10 (Code   | ALT-F10 (Code   | ALT-F10 (Code   |
| menu            |                 |                 |                 |
|                 | Editor only)    | Editor only)    | Editor only)    |
+-----------------+-----------------+-----------------+-----------------+
| Find            | CTRL-F          | CTRL-F          | CTRL-F          |
+-----------------+-----------------+-----------------+-----------------+
| Replace         | CTRL-R          | CTRL-H          | CTRL-R          |
+-----------------+-----------------+-----------------+-----------------+
| Search Again    | F3              | F3              | CTRL-L          |
+-----------------+-----------------+-----------------+-----------------+
| Select All      | CTRL-A          | CTRL-A          |                 |
+-----------------+-----------------+-----------------+-----------------+
| Invoke Code     | CTRL-SPACE      | CTRL-SPACE      | CTRL-SPACE      |
| Completion      |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Code Templates  | CTRL-J          | CTRL-J          | CTRL-J          |
+-----------------+-----------------+-----------------+-----------------+
| **Bookmarks**   |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Set Numbered    | CTRL-SHIFT-\#   | CTRL-SHIFT-\#   | CTRL-SHIFT-\#   |
| Bookmark        |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Goto Numbered   | CTRL-\#         | CTRL-\#         | CTRL-\#         |
| Bookmark        |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+

  **Command/Section**        **Default**            **Visual Studio**      **Borland Classic**
  -------------------------- ---------------------- ---------------------- ----------------------
  Set Unnumbered Bookmark    CTRL-SHIFT-\'          CTRL-SHIFT-\'          CTRL-SHIFT-\'
  Goto Unnumbered Bookmark   CTRL-\'                CTRL-\'                CTRL-\'
  **Clipboard**                                                            
  Cut to Clipboard           CTRL-X or SHIFT- DEL   CTRL-X or SHIFT- DEL   CTRL-X or SHIFT- DEL
  Copy to Clipboard          CTRL-C or CTRL-INS     CTRL-C or CTRL-INS     CTRL-C or CTRL-INS
  Paste from Clipboard       CTRL-V or SHIFT-INS    CTRL-V or SHIFT-INS    CTRL-V or SHIFT-INS

> []{#Keyboard_Handling_in_Recorder .anchor}**Keyboard Handling in
> Recorder**
>
> TestComplete will record all keys entered to the active control while
> recording except for any keys that are in the Global Shortcuts.
>
> **Global Shortcuts** (keys that work when TestComplete is running even
> if TestComplete does not have focus)

  **Command**              **Default Key**
  ------------------------ -----------------
  Pause script execution   SHIFT-10
  Fix Information          SHIFT-CTRL-A
  Record                   SHIFT-F1
  Stop                     SHIFT-F2
  Run                      SHIFT-F3
  Pause recording          SHIFT-F11
  Low Level Record         SHIFT-F4

> []{#Configuring_Global_Shortcuts .anchor}**Configuring Global
> Shortcuts**
>
> To access and change Global Shortcuts:

87. Select **Tools \| Options** from the main menu.

88. Select **General \| Global Shortcuts** from the Options dialog.

89. Select the **Action**.

90. Type in the new keyboard shortcut (note: if it is already in use,
    you will need to clear the one using it first).

![](./media/image366.png){width="5.960137795275591in"
height="3.126457786526684in"}

> **Figure 279 \--Global Shortcuts**
>
> []{#Configuring_Keyboard_Emulation .anchor}**Configuring Keyboard
> Emulation**
>
> To access and change the keyboard emulation:

1.  Select **Tools \| Customize Keyboard\...** from the main menu.

2.  Choose the keyboard emulation that you want. (You can also set
    keyboard shortcuts for any command in this dialog).

![](./media/image367.png){width="4.519971566054243in"
height="4.927083333333333in"}

> **Figure 280 \-- Customize Keyboard Dialog**

### Appendix B - Types of Testing

20. []{#Appendix_B_-_Types_of_Testing .anchor}**Appendix B - Types of
    Testing**

> []{#Types_of_Testing .anchor}**Types of Testing**

#### Manual Testing

> Manual Testing is where a tester methodically exercises the features
> of a product or product area without the aid of test automation. The
> single greatest strength of manual testing is that it is truly
> real-world testing, meaning that the tester can utilize the
> application under test the same way an end user would. Through manual
> testing the tester can provide a wide variety of feedback about the
> application under test not limited to simply reproducing bugs.
>
> Manual tests are difficult to perform on a regular basis. The major
> weakness of manual testing is that it is time consuming, tedious and
> requires extended periods of focused attention. Manual testing tends
> to be quite error prone, leading to situations where consistently
> reproducing a bug can be very difficult.

#### Functional Testing

> Functional Testing focuses on interactions with an application\'s user
> interface (UI) via the mouse, keyboard or other input device with
> particular attention to how the application visually responds to
> input. The goal of Functional Testing is to methodically cover all of
> the various UI features exposed by an application. Functional Testing
> should be highly organized and structured in a manner that allows for
> additional tests to easily be incorporated as new features are added.

#### Unit Testing

> Unit Testing focuses on smaller atomic portions of an application.
> Typically, Unit Testing requires internal knowledge of how an
> application performs and seeks to test portions (objects, methods and
> function) of an application in isolation. In many cases, applications
> have to be designed with Unit Testing in mind in order for this type
> of testing to be truly effective. The benefit of unit testing is that
> it tends to force application developers to write smaller, well
> defined routines with fewer dependencies allowing for highly specific
> tests to be developed.

#### Regression Testing

> Regression Testing is the process of executing tests in a repeatable
> manner and comparing the latest results with previous test executions
> to ensure that the same outcome is achieved. Regression Testing is
> extremely important and is the means of realizing the value of test
> automation. Repeatedly executing tests over time allows you to verify
> the application is still performing as intended.

#### Distributed Testing

> Distributed Testing is the act of farming different portions of a test
> out to separate machines for execution. Distributed Testing is useful
> for simulating real world interactions on a networked application such
> as a web site or web service and can exercise functionality designed
> to handle concurrent use of application resources including, but not
> restricted to data.

#### HTTP Performance Testing

> HTTP Performance Testing is the simulation of real-world interactions
> with a web application from multiple machines. TestComplete provides
> the ability to leverage networked computers and virtual users to
> simultaneously submit HTTP transactions to a web application.

#### Multi-Tier

> In software development there are typically three Tiers which are used
> to describe various aspects of an application they are Client Tier,
> Middle Tier and Data Tier. These are each defined as:
>
> **Client** \-- The user interface or presentation of an application
> and its data which is typically covered through Functional Testing.
>
> **Data Tier** \-- The storage of an application\'s data which can be
> exercised by Functional Testing as well as Unit Testing
>
> **Middle Tier** \-- Refers to the portion of the application
> responsible for moving data back and forth between the Client and the
> Data Tiers. The code that resides in this Tier can be tested from
> either the Client Tier via Functional testing or through Unit Testing
> on the code in the Middle Tier itself. Keep in mind that these are not
> strict rules as to which type of testing should be used but more
> illustrative how the different types of testing can be used.