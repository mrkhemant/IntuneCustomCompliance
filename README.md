Custom Device Compliance Policy in Intune

With the Custom Device Compliance, you can able to create a create your own compliance. Below are the benefits for Custom device Compliance.

With the Intune help you can protect organizational data by requiring users and Device data with meet some requirements that’s called compliance policy.
In Intune we can set rules and settings that user and device must meet to be an compliant.
We can include actions on noncompliant device, User can alert if device is noncompliant.
It can be combined with the Conditional access to block user or device if not compliant.
Can override the configuration of settings that you also manage through device configuration policies.
Before you start, be ready with the PowerShell and Jason File.

You can download PowerShell and use it.

++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
To create a custom device compliance policy in Intune, you'll need to define a JSON file with the settings you want to check and a discovery script (PowerShell for Windows, any language for Linux) to evaluate those settings, then configure the policy to use these elements. 

1. Prerequisites:
JSON File: Create a JSON file that defines the settings and values you want to use for custom compliance. 
Discovery Script: Create a script (PowerShell for Windows, any language for Linux) that can evaluate the settings defined in the JSON file. 
Upload Script: Upload the discovery script to Intune.

2. Create the Compliance Policy:
Sign in to Intune: Access the Microsoft Endpoint Manager admin center.
Navigate to Compliance Policies: Go to Devices > Compliance Policies > Create Policy.
Select Platform: Choose the platform (Windows 10 and later, Linux) for the policy.
Basics Tab: Enter a name for the policy.
Select "Custom Compliance".
Compliance Settings Tab:
Expand "Custom Compliance".
Set "Custom compliance" to "Require".
Select your discovery script.
Upload and validate the JSON file.

Actions for Noncompliance Tab: Specify actions for noncompliant devices (e.g., alert, block access).

Assignment Tab: Select the group to which you want to deploy the policy.

Review + Create: Review the policy settings and click "Create". 

4. Monitoring and Refreshing Compliance Status:
Monitor Compliance: Use the device compliance dashboard in Intune to monitor the status of your policies. 
Refresh Compliance Status:

If you modify a device's configuration, you can refresh the compliance status by signing into the Intune app or using the "Refresh" link on the device details page. 

