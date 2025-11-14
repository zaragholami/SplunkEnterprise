Windows Event Log Analysis Splunk App version 1.5.1
Copyright (C) 2016-2018 Adrian Grigorof All Rights Reserved.

The Windows Event Log Analysis Splunk App assumes that Splunk is collecting information from Windows servers and workstation via the Universal Forwarder, the local Windows event log collector or remotely via WMI.
It analyzes the entries from indexes matching the "index="wineventlog" OR source=*WinEventLog*" criteria. This matches the defaults used by the Universal Forwarder, the collection of local Windows event logs and the collection via WMI.
To collect the logs from remote computers without installing the Universal Forwarded on each computer, configure the forwarding of event logs to central location using the Windows built-in event forwarding.
The Interesting Processes section from the Processes dashboard is partially based on a presentation by Michael Gough from www.malwarearchaeology.com: "The Top 10 Windows Event ID's Used To Catch Hackers In The Act". See https://www.malwarearchaeology.com/home/2016/5/7/windows-top-10-event-logs-from-my-dell-enterprise-security-summit-talk for the presentation slides and information on how to enable the auditing of processes, including command-line based ones. The list of “interesting processes” is based on a study by JPCERT CC (Japan Computer Emergency Response Team Coordination Center) on detecting lateral movement through tracking of event logs (https://www.jpcert.or.jp/english/pub/sr/ir_research.html). The list is stored in C:\Program Files\Splunk\etc\apps\eventid\lookups\interesting_processes.csv and it can be adjusted with a text editor if needed.
If not data is displayed, please verify that the Universal Forwarder is installed properly and that the all the Windows event logs are sent to the "wineventlog" index (or the WinEventLog* sources).

See Configure Computers to Forward and Collect Events (https://msdn.microsoft.com/en-us/library/cc748890(v=ws.11).aspx) for details on how to configure a computer as a collector of logs.

Send any suggestions, questions etc. to adigrio@gmail.com or support@altairtech.ca.

For up-to-date documentation, see: https://www.eventid.net/splunk_addon.asp
