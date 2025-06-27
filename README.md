# firewall
 Windows (GUI + CMD):
1. Open Firewall Configuration Tool:

Go to Control Panel > System and Security > Windows Defender Firewall

Or run wf.msc in the Run dialog.

2. List Current Firewall Rules:

Go to Advanced Settings > Inbound Rules / Outbound Rules

CMD (PowerShell): netsh advfirewall firewall show rule name=all

3. Add Rule to Block Port 23 (Telnet):

In Advanced Settings, click Inbound Rules > New Rule

Choose Port > TCP > Specific port: 23

Action: Block the connection

Profile: All

Name: “Block Telnet Port 23”

4. Test the Rule:

Try: telnet localhost 23 (You may need to enable Telnet client via Windows Features)

It should fail to connect.

5. (Skip SSH for Windows)

6. Remove the Test Rule:

Go to the created rule > Right-click > Delete
