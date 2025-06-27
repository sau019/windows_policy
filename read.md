#Task 4 - Setup and Use a Firewall (Windows - GUI Method)

##Internship Task - Cyber Security

###Objective:
To configure and test firewall rules using **Windows Defender Firewall with Advanced Security (GUI)** to understand how traffic filtering works.

## Operating System:
- Windows 11

#Tool Used:
- Windows Defender Firewall with Advanced Security (GUI)
- Telnet Client (Command-line tool for testing)


##  Steps Performed (GUI Method):

### 1] Open Firewall Manager
- Press `Win + R`
- Type: `wf.msc`
- Press **Enter**

### 2] View Existing Rules
- Click on **Inbound Rules** in the left panel
- All current incoming traffic rules are listed here
- Similarly, check **Outbound Rules** for outgoing traffic rules

### 3] Create Rule to Block Telnet (Port 23)
- Right-click **Inbound Rules** → click **New Rule**
- Select **Port** → click **Next**
- Select **TCP** → enter port `23` → click **Next**
- Choose **Block the connection** → click **Next**
- Apply to all profiles (Domain, Private, Public) → click **Next**
- Name the rule: `Block Telnet Port 23` → click **Finish**

### 4] Enable Telnet Client (for testing)
Open Command Prompt as Administrator and run:
command
dism /online /Enable-Feature /FeatureName:TelnetClient
