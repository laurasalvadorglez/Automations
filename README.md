# Automations 🔃
## Table of Contents
1. [Create diplomas](#Create-diplomas)
2. [Sending diplomas to the students of a course](#Sending-diplomas-to-the-students-of-a-course)


### Create diplomas

| **Description** | **Power Automate** |
|:-----:|:---------------:|
|As a trigger for this flow we will use a Microsoft form, so we start by creating one.|    In Microsoft Forms   ![Microsoft Form](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/form1.png)         |
|**To find the identifier execute the flow, and go to the outputs in "Get response details" there, in body, you will find the identifier, it will look like this: "r430a1759d1734798a85fd621869aedf6"** |   ![form identifier](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/id.png)         |
|**To create the schema, we go to the executed flow and copy the specified address** |   ![Parse json](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/json2.png)         |
|Add 2 Parse Json, and configure them with the previous steps.|       ![json](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/json.png)      |






### Sending diplomas to the students of a course 

| **Description** | **Power Automate** |
|:-----:|:---------------:|
|As a trigger for this flow we will use a Microsoft form, so we start by creating one.|    In Microsoft Forms   ![Microsoft Form](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/form.png)         |
|Add the trigger and the action “Get response details”.|       ![Microsoft Form](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/form2.png)        |
|Create a Parse Json for the excel (the file we will attach to the form) and add a “Get file content”.|     ![3rd step](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/3.png)          |
|Create the table so that the flow can read the excel|         ![Create table](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/converttable1.png)       |
|To verify that there are the same number of files as rows in the excel.|         ![Number of files 1](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/numfiles.png)       |
|We add a condition so that, if there is a mismatch, the technician is notified and the flow is stopped.|         ![Number of files 2](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/numfiles2.png)       |
|We initialize the variables in order to create the next block.|         ![Variables](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/variables.png)       |
|Now we make a second check. This time, we check that each Excel row has its respective document.|         ![Check names](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/checknames.png)       |
|We create an Apply to each where we make a row comparison with the file names.|         ![Check names 2](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/checknames2.png)       |
|We create another comparison, in which if “Missing files” is true it sends a message to the technician with the name of the missing file and stops the flow. |         ![Check names 3](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/checknames3.png)       |
|Start a variable to store the documents |         ![Initialize variable](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/Initvar.png)       |
|Start the for each. We add a Parse Json and the action of Get file content using path.|      ![For Each 1](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/ForEach1.png)         |
|Name the variable created before|      ![Name var](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/ForEach2.png)         |
|Configure the sending of emails.|      ![Emails](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/ForEach3.png)         |
|Finally, add 2 actions, one to write in the channel that the process has been carried out correctly and the other to notify the technician if there has been an error|      ![End](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/end.png)         |

