### Test Log

5.  []{#Test_Log .anchor}**Test Log**

> **Objectives**
>
> This chapter discusses the test log and the types of messages
> available in TestComplete. You will learn how to navigate, analyze and
> share the test log. You will learn about the Log Window user
> interface, about the types of available logging message and how images
> are logged. You will learn how to structure Test Log folders and
> change the appearance of messages. You will also learn how to view
> test logs in Internet Explorer and how to communicate your test
> results by email.

[]{#_bookmark95 .anchor}

> **Test Results**
>
> Up to this point we\'ve focused on building tests and playing them
> back. Another key element of testing is analyzing and communicating
> the test results. TestComplete includes a **Log Window** to review all
> of the output produced during a test run. It\'s important to
> understand how TestComplete manages log output so we\'ll start by
> looking at the Project Explorer. At the bottom of the Project Explorer
> window is a node which contains all of the log output for all projects
> contained within the ProjectSuite. Expanding this node lets you see
> all of the test executions for a given project. To view the Log
> Window, simply double click one of the **Project Log** nodes as
> illustrated below:

![](./media/image76.png){width="3.572620297462817in"
height="3.6770833333333335in"}

> **Figure 66 \--Opening a Log**
>
> []{#Log_Window .anchor}**Log Window**
>
> Logs are used to persist feedback from your tests including errors,
> warning messages and events as well as entire files and images. Logs
> are stored in a directory as XML files. The Log Window displays all of
> the output produced by the test and is divided into several regions,
> as shown in the screenshot below.

![](./media/image77.jpeg){width="5.8924704724409445in"
height="4.620937226596675in"}

#### Test Log Pane

> This panel displays the actual log output from the test including
> **Errors**, **Warnings**, **Messages**, **Events**, and **Images**.
>
> Each of the above types has a unique glyph and can be filtered using
> the check boxes found at the top of the **Test Log** pane. Notice in
> the screenshot below that **Error** items are *not* displayed and the
> yellow bar to the left of the list indicates the view is filtered.

![](./media/image78.png){width="5.022623578302712in" height="2.3125in"}

> **Figure 67 \--The Filtered Test Log**
>
> To fine-tune filtering behavior, right-click the log and choose
> **Filter Data** from the context menu. This displays the Filter
> Builder dialog. The Simple Filter tab of the dialog lets you choose
> from the same set of categories available directly in the log window.
> Log messages can be organized in a tree structure. The **Show all
> parents** and **Show all children** check boxes allow all parents and
> children of a log message to display.

![](./media/image79.png){width="4.964430227471566in" height="3.09375in"}

> **Figure 68 \--The Filter Builder**
>
> The **Extended Filter** tab allows you to build complex filters
> complete with AND/OR/NOT AND/NOT OR sections. The first part of each
> statement can be clicked to get a list of log elements that can be
> used such as \"Priority\" or \"Message\". The next link will display a
> list of comparison operators that work with the first part of the
> statement. The last part of the statement will be a value to compare
> against.

![](./media/image80.png){width="4.964430227471566in" height="3.09375in"}

> **Figure 69 \--The Extended Filter**

#### Picture Tab

> The **Test Log** can also display pictures captured during the test
> execution. For example, you can post a screenshot using the Log object
> in your script or keyword test. Here is an example of a screen capture
> displayed in the **Test Log** upon completion of the test.

![](./media/image81.jpeg){width="5.935445100612424in"
height="3.311353893263342in"}

> **Figure 70 \--Picture Window of the Test Log**

#### Additional Information

> The **Additional Information** of the **Test Log** pane contains
> information associated with a specific **Test Log** item (if any). For
> example, Log Message includes a Remarks parameter that can be used to
> add straight text or HTML.

![](./media/image82.png){width="5.771224846894138in"
height="1.588124453193351in"}

> **Figure 71 \--Additional Inform ation**
>
> []{#Log_Structure .anchor}**Log Structure**
>
> You can create a hierarchical structure via creating and pushing log
> folders onto the log using the Log object. Here are **Log** object
> methods that can be used to restructure the log:
>
> **AppendFolder:** Creates a folder in the test log and activates this
> folder.
>
> **PopLogFolder:** Pops the folder that is currently at the top of the
> folder stack out of the stack. The folder left at the top of the stack
> is now the default folder of the test log.

![](./media/image83.png){width="3.2919225721784775in" height="1.485in"}

> **Figure 72 \--Hierarchical Structure in Log**
>
> All messages by default go into the active log folder (i.e., the top
> of the stack). Each \"AppendFolder\" moves the logging inside a folder
> and each \"PopLogFolder\" moves the logging out one level.

#### Logging in Keyword Tests

> The Keyword Test shown in the screenshot below creates the log shown
> in the preceding topic. Simply use **Append Log Folder** to add a
> folder and make that the active folder so that all logged messages and
> new folders are created inside of the folder. Use **Pop Log Folder**
> to move one level outside the current folder.

![](./media/image84.png){width="5.967701224846894in"
height="1.8112489063867017in"}

> **Figure 73 \--Appending and Popping Log Folders**
>
> []{#Logged_Images .anchor}**Logged Images**
>
> TestComplete automatically takes screenshots of Test Steps as they are
> recorded and another set during the test playback. As you click
> through the test log you can see the recorded **Expected Image** next
> to the **Actual Image** recorded during the test playback.

![](./media/image85.jpeg){width="5.9375in" height="3.28125in"}

> **Figure 74 \--Logged Im ages**

#### Image Toolbar

> The toolbar for the **Actual Ima**ge is shown in the screenshot below.

![](./media/image86.png){width="3.7275820209973753in"
height="0.8353116797900263in"}

> **Figure 75 \--Actual Im age Toolbar**
>
> The **Synchronize View** button is on by default and simply makes the
> Expected and Actual Image stay together as you scroll the window, e.g.
> when you scroll the Expected Image window to the right, the Actual
> Image will also scroll to the right.
>
> The **View Comparison Result** button makes analyzing the log quicker.
> When this button is pressed, the Actual Image shows the pixel
> differences between the two images in red. In the screenshot below,
> the Expected Image shows that **Customer Name is** \"Bart Simpson and
> the actual image is \"Marge Simpson\". Toggling the **View Comparison
> Result** button makes changes stand out in red. The button's drop-down
> sets the background to white, light or dark.

![](./media/image87.jpeg){width="5.920659448818897in"
height="3.5523950131233595in"}

> **Figure 76 \--Expected and Actual Im ages**
>
> []{#Changing_Log_Appearance .anchor}**Changing Log Appearance**
>
> If you need to make a logged message or remarks stand out, you can
> format both the Message and the Remarks. The formatting can apply to
> messages, folders and logged images. The screenshot below shows the
> log message \"Incomplete results\" where the background is green and
> the font is red, bold and italic. In the Remarks section, the last
> sentence is actually a bit of HTML surrounded by bold \"\<b\>\" tags.
>
> The topic that follows will show you how to achieve a similar result.

![](./media/image88.jpeg){width="5.923784995625547in"
height="3.78625in"}

> **Figure 77 \--Form atted Log Message and Rem arks**

#### Formatting the Log with Keyword Operations

> The formatted message requires two Operations, both from the Logging
> section of the Operations palette. The **Log Attributes** Operation
> configures how following log messages are formatted. The **Log
> Message** Operation then specifies the Log Attributes in its Attrib
> property.

![](./media/image89.jpeg){width="5.9703838582677164in"
height="2.0425in"}

> **Figure 78 \--Log Attributes and Message**
>
> When you drop the Log Attributes Operation, a dialog will appear where
> you can set the **Message** font color, background and formatting. The
> **Remarks** can be formatted as either \"HTML\" or \"Plain Text\". In
> this example we\'re using the HTML format.

![](./media/image90.png){width="3.4280555555555554in" height="3.125in"}

> **Figure 79 \--Setting Log Attributes**
>
> When you add the Log Message Operation to the test you need to
> surround the message with \<HTML\> tags and any other HTML formatting
> you want showing in the Remarks. The example below surrounds the
> second sentence with Bold \"\<b\>\" tags.

![](./media/image91.png){width="4.702015529308836in" height="3.34375in"}

> **Figure 80 \--Entering HTML Rem arks**
>
> To have the Log Message use the Log Attributes, click the ellipses for
> the Attrib and set the Mode to \"Last Operation Result\".

![](./media/image92.jpeg){width="5.933474409448819in"
height="4.913333333333333in"}

> **Figure 81 \--Setting the Log Message Attrib**
>
> []{#_bookmark107 .anchor}**Summary**
>
> In this chapter you became familiar with the test log and the types of
> messages available in TestComplete. You learned how to navigate,
> analyze and share the test log. You learned about the Log Window user
> interface, about the types of available logging message and how images
> are logged. You learned how to structure Test Log folders and change
> the appearance of messages. You also learned how to view test logs in
> Internet Explorer and how to communicate your test results by email.