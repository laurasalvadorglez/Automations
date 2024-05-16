# Automations 🔃
## Table of Contents
1. [Create diplomas](#Create-diplomas)
2. [Sending diplomas to the students of a course](#Sending-diplomas-to-the-students-of-a-course)


### Create diplomas

| Description | Power Automate |
|-----:|---------------|
|As a trigger for this flow we will use a Microsoft form, so we start by creating one.|    In Microsoft Forms   ![Microsoft Form]


### Sending diplomas to the students of a course 

| **Description** | **Power Automate** |
|-----:|---------------|
|As a trigger for this flow we will use a Microsoft form, so we start by creating one.|    In Microsoft Forms   ![Microsoft Form](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/form.png)         |
|Add the trigger and the action “Get response details”.|       ![Microsoft Form](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/form2.png)        |
|Create a Parse Json for the excel (the file we will attach to the form) and add a “Get file content”.|     ![3rd step](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/3.png)          |
|Create the table so that the flow can read the excel|         ![Create table](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/4.png)       |
|Create a variable to initialize the attachments.|        ![Create Array](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/Array%205.png)       |
|Start the for each. We add a Parse Json and the action of Get file content using path.|      ![For Each 1](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/ForEach1.png)         |
|Name the variable created before|      ![Name var](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/ForEach2.png)         |
|Configure the sending of emails.|      ![Emails](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/ForEach3.png)         |
|Finally, add 2 actions, one to write in the channel that the process has been carried out correctly and the other to notify the technician if there has been an error|      ![End](https://github.com/laurasalvadorglez/Automations/blob/main/Assets/end.png)         |

