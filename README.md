# ODAF
Open Digital Assistant Framework

![alt text](https://github.com/ajdfnwjf/odaf/blob/master/ODAFArchitectureOverview.png)

# High Level Model Description

1.	There can be multiple clients attached to a digital assistant (DA) that have different capabilities. These clients have to be controlled. Therefore all messages run through a central client control function.
2.	Centerpiece of a DA are the dialogs. Templates for these dialogs are stored in separate files. Dialogs can be triggered via incoming messages, time triggers or data triggers. There needs to be a central dialog state manager function. Actions that are executed as part of a dialog are separated into core, open access and private actions. Core actions are necessary for the DA functionality. Open source and private actions are domain specific and might use their own data.
3.	Project Setup is a very complex action and thus treated separately. Projects are based on templates and result in ToDos which are then used to trigger dialogs on a time base. Another way to generate the ToDos are to import them from a project management software.
4.	Time triggers implement a chronjob which constantly scans for due dialogs.
5.	Another way to trigger dialogs are data conditions. Data triggers are defined by templates that are stored in separate files. Data triggers are the place to use all the state of the art sophisticated AI-machine-learning-deep-learning-predictions. Data triggers can use all available data.
6.	All templates: dialog, project, data are maintained using an admin client user interface.
7.	A DA needs to manage a lot of content, e.g. reminder texts. This content is also maintained via the admin client.
