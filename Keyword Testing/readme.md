### Keyword Testing

#### Objectives

This chapter explains what Keyword Testing is and what it\'s used for.
You\'ll learn how to create Keyword Tests from multiple points in the TestComplete user interface. You\'ll learn how to use the Keyword Test Editor to work with existing tests, variables and parameters.

#### Editing Keyword Test Steps

Using the TestComplete Keyword Test Editor is intuitive and supports many of the same operations a standard text/code editor supports such as cut, copy, paste, undo and selection. Functionally, the editor resembles a spreadsheet where you can modify both rows and columns within the test.

Test Steps can easily be added or deleted from a Keyword Test. To delete a Test Step, simply select the row and press the Delete key. To add a Test Step either drag and drop an item from the Operations palette onto the test editor, use the editor\'s right click menu and select **Insert New Operation** or use the **Append to Test** toolbar button to record additional steps onto the end of the current test.
The screenshot below shows an **If..Then** Operation dragged into an existing Keyword Test.

![](./media/image30.jpeg)


To edit a specific step, double-click the step to invoke the corresponding dialog (e.g. On Screen Action, Log Message, and so on) .

#### Editing Item Sub-objects

By default, the Keyword Test Editor records operations on objects that appear in the TestComplete **Object Browser** Tree view. Many of these objects include properties which return child objects you may want to manipulate in your test. To access these child object properties the Keyword Test Editor provides the **Work with Object Through Property\...** context menu option. The option allows you to choose a specific child object property on which to perform an action.

![](./media/image31.png)


For example, if you want to change the scroll position of a window that has scrollbars you\'ll need to manipulate the **HScroll** or **VScroll** object properties and set the **Pos** property of the scrollbar accordingly.

![](./media/image32.png)


#### Working with Operations

The Operations panel of the Keyword Test Editor contains the list of all of the available actions that can be added to a Keyword Test.
Operations are grouped by category, e.g. the \"Logging\" category includes \"Log Message\" and \"Post Screenshot\" Operations.

#### Adding Operations to a Test

There are several ways to add operations to a Keyword Test including:

- Drag and drop from the Operations palette.

- From the right click context menu.

- Using the recorder to append new steps to an existing test.

![](./media/image33.jpeg)


##### Using the Operations Palette

Using the mouse, drag and drop an **Operation** from the palette onto the **Test Steps** editor at the desired location. Operations can be inserted before or after existing steps depending on the placement of the mouse at the time of the drop. The mouse cursor will display an arrow indicating the specific placement of the new step in relation to the other steps. The screenshot below shows a \"Run TestedApp" Operation being dragged to the Test Steps editor.

![](./media/image34.png)

##### Using the Right Click Menu

From the editor\'s right click context menu, Operations can be added using the **Insert New Operation** submenu. Several common Operations are included along with a **More Operations\...** menu item.

![](./media/image35.png)


Selecting **More Operations\...** from the **Insert New Operation** submenu displays the **Insert Operation** dialog**.** The dialog allows you to choose from a complete list of the possible Operations available in the Operation palette.

![](./media/image36.png)

##### Using the Append to Test Button

TestComplete provides the ability to append recorded steps to existing Keyword Tests using the **Append to Test** tool button on the Keyword Editor Toolbar. When this button is clicked, TestComplete minimizes and new recorded steps are added at the end of the active Keyword test.

![](./media/image37.png)

**Adding Conditional Logic**

Like scripts, Keyword Tests support both branching and looping operations allowing you to control the flow of actions performed by the test. For conditional logic, TestComplete provides several options including \"**If\...Then\", \"Else** and \"**If Object\"** operations.
To control looping, TestComplete provides \"**For Loop\"** and \"**While Loop\"** operations. In this topic we'll examine the **If Object** operation.

#### Lab: \"If Object\" Operation

This example adds logic to take the screenshot only if the sample \"Orders\" main window is visible on screen. This example uses the \"Orders\" sample application located in your Public Documents folder. For help locating the sample projects refer to the TestComplete online help and search for \"samples\". To complete these steps, you\'ll need to have the \"Orders \"application running on your PC.

1.  Select **File \| New \| New Project\...**

2.  Click the **OK** button on the **Create Project** dialog

3.  Right-click the project node and select **Add \| New Item\...** from the context menu. This will display the Create Project Item dialog.

4.  In the Create Project Item dialog, select the Keyword Testing item from the list and then click the **OK** button.

5.  Right-click the KeywordTests node and select **Add \| New Item\...** from the context menu. This will display the Create Project Item dialog.

6.  In the Create Project Item dialog, select the Keyword Test item from the list and then click the **OK** button.

7.  Select the **Logging** category within the **Operations** palette, then drag and drop the **Post Screenshot** Operation onto the **Test Steps** editor. The Post Screenshot dialog will display.

8.  From the Post Screenshot dialog, drag the Finder Tool to the \"Orders\" window. Click the **Finish** button to close the dialog and create the test step.

11. Select the **Test Actions** category within the **Operations** palette, then drag and drop the **If Object** operation onto the **Test Steps** editor right before our **Post Screenshot** step as shown in the screenshot below.

![](./media/image38.png)

Notice there is an indicator arrow that will point up-left if the Operation will drop above the selected step or down-left if the Operation will drop after the selected step.

12. The **If Object** dialog will appear, allowing you to select the desired window.

13. With the Orders sample application still open, select the Order\'s Main window and click the **Next** button.

![](./media/image39.png)

14. Select the **Exists** condition and click **Finish** to complete adding the operation to your test.

![](./media/image40.png)

15. Next, indent the **Post Screenshot** step to make it a child step of the **If Object** operation.

![](./media/image41.png)

16. Run the test with and without the Orders window present.

We\'ve added conditional logic to our test so the **Post Screenshot** step only executes if the Main form of the Orders application Exists.

#### \"If\...Then\" Operation

We can use the same logic we added above using the **If\...Then** operation. The only difference is the structure of the condition used in the **If** operation. TestComplete supports a variety of options for specifying conditions of a logic statement including:
- Constant
- Code Expression 
- Variable
- Last Operation Result 
- Test Parameter 
- Onscreen Object

By default, an **If\...Then** operation will not contain child operations, so the step will have no effect on test execution. Use the indent toolbar button to choose which subsequent operation(s) to perform when the If statement succeeds. Likewise, to remove a step from within an **If\...Then** operation, use the **Outdent** button on the editor toolbar. Let\'s take a look\...

1.  To add an **If\...Then** operation to a Keyword Test select the Statements category within the Operations palette then drag and drop the **If..Then** operation onto the Test Steps editor. Dropping an If\...Then operation will invoke the If\...Then dialog to assist with constructing a Boolean condition for the operation:

![](./media/image42.png)

2.  Click the ellipsis button under the **Value1** column to display the Edit Value dialog:

3.  Select **Code Expression** from the **Mode** drop down and type \"Aliases.Orders.MainForm. Exists\" as the **Value** then click the **OK** button.

![](./media/image43.png)

4.  Under the **Value2** column type \"True\" and click the **OK** button.

![](./media/image44.png)

5.  Use the Indent button on the Post Screenshot step to make it a child of the If\...Then operation.

We\'ve now looked at adding \"if\" logic to our Keyword Test using two different operations.

#### Working with Variables

TestComplete includes support for creating user defined **Variables** at the **ProjectSuite** and **Project** levels. 
**ProjectSuite** variables can be used throughout all of the projects contained within the suite whereas Project variables are limited in scope to the project itself.

TestComplete supports two types of variables:

**Persistent** \-- Retain their value between test executions on the same machine.

**Temporary** \-- Reset to their default value with each execution of the test.

To view ProjectSuite or Project Variables double click the respective node from the Project Explorer and select the Variables tab at the bottom of the Workspace.

![](./media/image45.png)

#### Temporary and Persistent Variables

The meanings for Temporary and Persistent Variables columns are explained below:

  **Column**          **Description**
  ------------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Name**            Specifies the variable name.
  **Type**            Specifies the type of the project or project suite variable.
  **Default Value**   A project can be shared between several testers working on different workstations. The variable values are computer-specific. Using the Default Value column, you can specify the value that will be used when the project is opened for the first time on the remote computer

  **Column**        **Description**
  ----------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Local Value**   Specifies the current value of the variable. This value depends on the computer where the project has been opened. Note that the Local Value applies to Persistent variables only.
  **Category**      The category is used to group variables. Use the Field Chooser option on the context menu to view this column. This column is not visible by default.
  **Description**   Any descriptive text related to the variable.

#### Creating and Deleting Variables

To create or delete variables use the right click context menu of the editor:

![](./media/image46.png)

To modify existing variables simply click the appropriate cell within the editor to change its value.

#### Lab: Using Variables in a Keyword Test

In this section will look at an example of using a Project Variable within a Keyword Test. First, we\'ll create a new project and declare a Temporary project Variable.

1.  Select **File \| New \| New Project\...** and click **OK** on the Create New Project dialog

2.  Double click the Project node within the Project Explorer and click the **Variables** tab at the bottom of the Workspace:

![](./media/image47.png)

3.  Right click the **Temporary Variables** section and select **New Item.**

![](./media/image48.png)

4.  Click the **Name** column and enter \"MyTempVar\". Under the **Default Value** column enter \"a Project Variable\" (without the quotes)

5.  Right click the **KeywordTests** node in the Project Explorer and select **New \| New Item\...** then click **OK** on the Create Project Item dialog to create a new Keyword Test.

6.  Click the **Logging** category of the Operations palette and drag & drop the **Log Message** operation onto the editor:

![](./media/image49.png)

7.  Click the **Next** button on the Log Message dialog and then click the ellipsis at the far right of row 1 to view the Edit Parameter dialog.

8.  In the **Mode** drop down, select **Variable**. In the **Value** drop down select Project. Variables.MyTempVar.

![](./media/image50.png)

9.  Click the **Finish** button on the Log Message dialog. When you run this test, TestComplete will output the value of the Project Variable to the Test Log.

![](./media/image51.png)

In this section, we used a **Project Variable**, though we could have used a **ProjectSuite** or **Keyword Variable** in the same manner.

#### Error Handling

Keyword Tests provide support for structured exception handling, allowing your tests to manage errors that could change the normal flow of your test execution. There are three operations that specifically support this style of error handling: **Try**, **Catch**, and **Finally.** If you are familiar with exception handling from a programming perspective, these operations provide the same level of functionality.

#### Error Handling Operations

These three operations must work in concert with one another, meaning that each **Try** operation must be followed by a **Catch** and/or a **Finally** Operation. The **Try** operation allows you to group Test Steps that may cause a potential error. The **Catch** operation handles exceptions thrown by Test Steps that are part of a **Try** block/group. The **Finally** operation allows you to perform any steps that always need to execute in spite of the fact an error occurred.
Typically, a **Finally** block is used to restore any resources allocated during the steps contained within a **Try** block/group.

Let\'s look at an example of a Keyword Test that utilizes these operations. Our focus here isn\'t so much on the error being raised rather the structure of the **Try** and **Catch** operations within a Keyword Test. For illustration purposes we\'ll use a one line JScript function that contains a syntax error that raises an exception.

*// Jscript routine with a syntax error for demonstrating*

*// the Keyword Testing try\...catch handling*

**function** DoSomething()

{

*// Message is spelled incorrectly which raises an exception*

  Log.Messag(\"test\");

}

Notice that the call to \"Log.Messag\" is misspelled (missing an \"e\") which results in an \"Object doesn\'t support this property or method\" exception.

Error handling differs between scripting languages. For more details between scripting languages, refer to TestComplete online help.

#### Lab: Error Handling

In this lab you will first generate an error, then handle it within a Keyword Test.

##### Generating an Error

Let\'s create a Keyword Test that calls this function wrapped with **Try** and **Catch** operations to illustrate exception handling logic.

1.  Create a new JScript project and add the function below to Unit1 (You can find the unit under **Advanced \| Script**):

![](./media/image52.png)

2.  Next, add a new Keyword Test to the project by right clicking the KeywordTests node in the Project Explorer and selecting **Add \| New Item\...**

3.  Drag and drop the **Run Script Routine** Operation from the **Test Actions** group onto the Test Steps list.

4.  On the Select Test dialog, select the \"DoSomething\" routine and click the **OK** button:

![](./media/image53.png)

5.  Click the **Run** button on the Keyword Test Editor. You should see this dialog and the test execution will end:

![](./media/image54.png)

When you look at the resulting log you can see that the test execution was interrupted by an exception:

![](./media/image55.png)

##### Handling the Error

To catch this error and continue processing we can add the **Try** and **Catch** operations bracketing the **Run Script Routine** Operation, allowing us to handle the error. To do that:

1.  Drag and drop the **Try** Operation from the **Statements** category to a point just above the Run Script Routine step. Next, indent the Run Script Routine step so that it appears nested under the Try operation:

![](./media/image56.jpeg)

2.  Drag and drop the **Catch** operation below the **Run Script Routine**. Use the Indent/ Outdent buttons to make the Try and Catch operations appear at the same level, as shown in the screenshot below.

![](./media/image57.jpeg)

At this point, all we need to do is add a **Log Message** Operation nested under our **Catch** step so we can output some information and illustrate that our Try\...Catch block is working. To do that:

1.  Drag and drop a **Log Message** operation with a simple output message:

![](./media/image58.png)

2.  Indent the Log Message operation and the resulting Keyword Test should look like this:

![](./media/image59.png)

3.  Double-click the Project node and navigate to the Properties tab at the bottom of the Workspace. In the Playback category of options, uncheck the **Error Dialog** and **Stop on Error** check boxes.

![](./media/image60.png)

4.  Now, run the test again and review the resulting log output. The error still occurs, but the Log step from inside the Catch runs.

![](./media/image61.png)

#### Summary

In this chapter we looked at what Keyword Testing is and what it\'s used for. You learned how to create Keyword Tests from multiple points in the TestComplete user interface. You also learned how to use the Keyword Test Editor to work with existing tests, variables and parameters.
