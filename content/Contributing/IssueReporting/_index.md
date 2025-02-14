---
title: "Issue Reporting"
description: "This article provides information on how to report issues to TrueNAS."
weight: 10
aliases:
  - /contributing/issuereporting/bugsfeatures/
  - /contributing/issuereporting/debug/
  - /contributing/issuereporting/savewebconsolelog/
tags:
- corecontributing
- scalecontributing
- coreissues
- scaleissues
---

We encourage all users to help us make TrueNAS the best NAS by reporting issues, requesting potentially helpful features, and relaying security vulnerabilities.  

## Issue Reporting
iXsystems uses [Jira](https://www.atlassian.com/software/jira) to track bugs and develop features.
You can view public issues without logging in, but you must create a Jira account to report bugs or suggest features.

![TrueNAS Jira Project](/images/Contribute/Jira.png "TrueNAS Jira Project")

### Bug Reports

Go to the [TrueNAS project on Jira](https://ixsystems.atlassian.net/jira/software/c/projects/NAS/issues) and click **Create** in the top bar.

![Create Ticket](/images/Contribute/JiraCreate.png "Create Ticket")

Set the **Issue Type** to **Bug**. The form reloads with more fields.
Developers use most of them, but you should fill out the **Summary** and **Description** to provide a useable report.

The **Summary** is a short, descriptive title that helps developers find the issue and understand the topic.

The **Description** lets you enter specific issue details.

![JiraSummaryDescription](/images/Contribute/JiraSummaryDescription.png "Summary and Description Field")

A good bug report includes these elements:

* A brief, specific, description detailing the problem you encountered.

* Steps to reproduce the issue. A simple list of the steps you took to see the issue is fine.

* An explaination of what should have happened while taking the steps listed above.

* A description of what actually happened while taking the steps listed above.

* Your TrueNAS software version (found in **Dashboard**).

* If the bug is service-related, include the current service configuration to help developers replicate your system.

* Always include a TrueNAS Debug file. Include a console log if the error is a web interface issue.
  If unsure how to save these, refer to the TrueNAS Debug and Web Console Log tabs on this page.

* Include screenshots if the bug is a web interface glitch or a formatting problem.

* Include a video if screenshots do not adequately show the issue.

* Include additional details you think can help the developer investigate.

When finished filling out the **Description**, click **Create** at the bottom of the form.

![Submit Ticket](/images/Contribute/JiraCreateBottom.png "Submit Ticket")

Developers review and update the ticket if/when they need additional information.
The Jira account receives emails about the ticket status.
Developers may request more details as they work to resolve the issue, so check the ticket periodically.

### Feature Suggestions

{{< include file="static/includes/General/CreateJiraSuggestion.md.part" markdown="true" >}}


### Security Issues


We publish previous security reports at https://security.truenas.com/.

Security issues do not appear on public issue trackers due to their sensitive nature.
If you have discovered a suspected security vulnerability in the latest version of a software release, you can [report this directly to the Security Team](mailto:security-officer@ixsystems.com).


## Creating a Debug File
{{< expand "Expand for more information about creating a debug file." "v" >}}
{{< include file="static/includes/CORE/CreateDebug.md.part" markdown="true" >}}

### Adding a Debug File to a Report
Jira provides a public facing area for files that do not require privacy. There is also a secure, developer only, area for uploading files with sensitive information like a system debug.

### New Tickets

Drag and drop public facing files into the **Attachment** box when creating a new ticket:

![JiraAttachmentNew](/images/Contribute/newjiraattachments.png "NAS Project Bug Creation Form")

### Existing Tickets

For public facing files, open the ticket in your browser and either click **Attach**, at the top of the ticket, or click the **+**, in the **Attachments** section, to open a local system file browser to select the files. You can also drag and drop the file onto the **Attacments** box and add any comments about it.

Upload private files to our secure private upload service located at 
https://ixsystems.atlassian.net/servicedesk/customer/portal/15/group/37/create/153”. Files uploaded to this service are only visible to project developers. JIRA removes them when closing the ticket.
{{< /expand >}}

## Web Console Log
Web console logs help diagnose problems with the user interface.
You can add logs to TrueNAS issues for debugging.

{{< expand "Expand for more information about the web console log." "v" >}}

### Firefox

Open the web console by clicking <i class="fa fa-bars" aria-hidden="true" title="Menu"></i> **(Menu) > More Tools > Web Developer Tools** (<kbd>Ctrl-Shift-I</kbd>).

In the upper right, set *Persist Logs*.
Click <i class="fa fa-bars" aria-hidden="true" title="More"></i> (More) > Settings. In the Web Console section, set **Enable timestamps**. 

Select the *Console* tab, then click <i class="fa fa-cog" aria-hidden="true" title="Settings"></i> (Settings) and set *Show Timestamps* and *Persist Logs*.

Leave the console open and perform the action that encounters problems.
Right-click in the console window and select *Export Visible Messages To > Clipboard*.
Open an editor, paste the clipboard contents, and save to a new <file>console.log</file> file.

After saving the file, open the console with <i class="fa fa-bars" aria-hidden="true" title="Menu"></i> **(Menu) > More Tools > Web Developer Tools** (<kbd>Ctrl-Shift-I</kbd>) and unset *Persist Logs*.

### Chrome

Open the console by clicking <i class="fa fa-ellipsis-v" aria-hidden="true" title="Options"></i> **(Options) > More Tools > Developer tools** (<kbd>Ctrl-Shift-I</kbd>).

Click <i class="fa fa-cog" aria-hidden="true" title="Settings"></i> **(Preferences)** and set *Preserve log* and *Show timestamps*. Close the **Preferences** window.

Leave the console open and perform the action that encounters problems. Right-click the console window. Choose *Save as…* and save the file.

After saving the file, open the console with <i class="fa fa-ellipsis-v" aria-hidden="true" title="Options"></i> **(Options) > More Tools > Developer tools** (<kbd>Ctrl-Shift-I</kbd>) and unset *Preserve log*.

## Attaching a Console Log File to a Report

Go to the [iXsystems Bug Tracker](https://ixsystems.atlassian.net/jira/software/c/projects/NAS/issues). Locate an existing ticket or create a new one reporting the problem.
Attach the console log file to the ticket by dragging it to **Attachments**.
{{< /expand >}}

{{< taglist tag="corecontributing" limit="10" >}}
