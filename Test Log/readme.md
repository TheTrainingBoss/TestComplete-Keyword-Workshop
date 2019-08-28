### Test Log

#### Objectives

This chapter discusses the test log and the types of messages available in TestComplete. You will learn how to navigate, analyze and share the test log. You will learn about the Log Window user interface, about the types of available logging message and how images are logged. You will learn how to structure Test Log folders and change the appearance of messages. You will also learn how to view test logs in Internet Explorer and how to communicate your test results by email.

#### Test Results

Up to this point we\'ve focused on building tests and playing them back. Another key element of testing is analyzing and communicating the test results. TestComplete includes a **Log Window** to review all of the output produced during a test run. It\'s important to understand how TestComplete manages log output so we\'ll start by looking at the Project Explorer. At the bottom of the Project Explorer window is a node which contains all of the log output for all projects contained within the ProjectSuite. Expanding this node lets you see all of the test executions for a given project. To view the Log Window, simply double click one of the **Project Log** nodes as illustrated below:

![](../media/image76.png)

#### Log Window

Logs are used to persist feedback from your tests including errors, warning messages and events as well as entire files and images. Logs are stored in a directory as XML files. The Log Window displays all of the output produced by the test and is divided into several regions, as shown in the screenshot below.

![](../media/image77.jpeg)

#### Test Log Pane

This panel displays the actual log output from the test including **Errors**, **Warnings**, **Messages**, **Events**, and **Images**.

Each of the above types has a unique glyph and can be filtered using the check boxes found at the top of the **Test Log** pane. Notice in the screenshot below that **Error** items are *not* displayed and the yellow bar to the left of the list indicates the view is filtered.

![](../media/image78.png)


To fine-tune filtering behavior, right-click the log and choose **Filter Data** from the context menu. This displays the Filter Builder dialog. The Simple Filter tab of the dialog lets you choose from the same set of categories available directly in the log window.
Log messages can be organized in a tree structure. The **Show all parents** and **Show all children** check boxes allow all parents and children of a log message to display.

![](../media/image79.png)


The **Extended Filter** tab allows you to build complex filters complete with AND/OR/NOT AND/NOT OR sections. The first part of each statement can be clicked to get a list of log elements that can be used such as \"Priority\" or \"Message\". The next link will display a list of comparison operators that work with the first part of the statement. The last part of the statement will be a value to compare against.

![](../media/image80.png)

#### Picture Tab

The **Test Log** can also display pictures captured during the test execution. For example, you can post a screenshot using the Log object in your script or keyword test. Here is an example of a screen capture displayed in the **Test Log** upon completion of the test.

![](../media/image81.jpeg)

#### Additional Information

The **Additional Information** of the **Test Log** pane contains information associated with a specific **Test Log** item (if any). For example, Log Message includes a Remarks parameter that can be used to add straight text or HTML.

![](../media/image82.png)

#### Log Structure

You can create a hierarchical structure via creating and pushing log folders onto the log using the Log object. Here are **Log** object methods that can be used to restructure the log:

**AppendFolder:** Creates a folder in the test log and activates this folder.

**PopLogFolder:** Pops the folder that is currently at the top of the folder stack out of the stack. The folder left at the top of the stack is now the default folder of the test log.

![](../media/image83.png)

All messages by default go into the active log folder (i.e., the top of the stack). Each \"AppendFolder\" moves the logging inside a folder and each \"PopLogFolder\" moves the logging out one level.

#### Logging in Keyword Tests

The Keyword Test shown in the screenshot below creates the log shown in the preceding topic. Simply use **Append Log Folder** to add a folder and make that the active folder so that all logged messages and new folders are created inside of the folder. Use **Pop Log Folder** to move one level outside the current folder.

![](../media/image84.png)

#### Logged Images

TestComplete automatically takes screenshots of Test Steps as they are recorded and another set during the test playback. As you click through the test log you can see the recorded **Expected Image** next to the **Actual Image** recorded during the test playback.

![](../media/image85.jpeg)

#### Image Toolbar

The toolbar for the **Actual Image** is shown in the screenshot below.

![](../media/image86.png)

The **Synchronize View** button is on by default and simply makes the Expected and Actual Image stay together as you scroll the window, e.g. when you scroll the Expected Image window to the right, the Actual Image will also scroll to the right.

The **View Comparison Result** button makes analyzing the log quicker. When this button is pressed, the Actual Image shows the pixel differences between the two images in red. In the screenshot below, the Expected Image shows that **Customer Name is** \"Bart Simpson and the actual image is \"Marge Simpson\". Toggling the **View Comparison Result** button makes changes stand out in red. The button's drop-down sets the background to white, light or dark.

![](../media/image87.jpeg)

#### Changing Log Appearance

If you need to make a logged message or remarks stand out, you can format both the Message and the Remarks. The formatting can apply to messages, folders and logged images. The screenshot below shows the log message \"Incomplete results\" where the background is green and the font is red, bold and italic. In the Remarks section, the last sentence is actually a bit of HTML surrounded by bold \"\<b\>\" tags.

The topic that follows will show you how to achieve a similar result.

![](../media/image88.jpeg)

#### Formatting the Log with Keyword Operations

The formatted message requires two Operations, both from the Logging section of the Operations palette. The **Log Attributes** Operation configures how following log messages are formatted. The **Log Message** Operation then specifies the Log Attributes in its Attrib property.

![](../media/image89.jpeg)

When you drop the Log Attributes Operation, a dialog will appear where you can set the **Message** font color, background and formatting. The **Remarks** can be formatted as either \"HTML\" or \"Plain Text\". In this example we\'re using the HTML format.

![](../media/image90.png)


When you add the Log Message Operation to the test you need to surround the message with \<HTML\> tags and any other HTML formatting you want showing in the Remarks. The example below surrounds the second sentence with Bold \"\<b\>\" tags.

![](../media/image91.png)


To have the Log Message use the Log Attributes, click the ellipses for the Attrib and set the Mode to \"Last Operation Result\".

![](../media/image92.jpeg)


#### Summary

In this chapter you became familiar with the test log and the types of messages available in TestComplete. You learned how to navigate, analyze and share the test log. You learned about the Log Window user interface, about the types of available logging message and how images are logged. You learned how to structure Test Log folders and change the appearance of messages. You also learned how to view test logs in Internet Explorer and how to communicate your test results by email.