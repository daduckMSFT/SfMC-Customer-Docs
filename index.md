# Opening quality Support cases for Intune

The purpose of this guideline is to provide a reference on how to open up great support cases. This will:
 - Minimize case resolution time. 
 - Reduce back & forth communications. 
 - Reduce progress towards the resolution from the moment the case is being assigned to a support representative.

Please use the table of contents to skip around this guide as needed.

> **NOTE:** This is not a troubleshooting document, but rather a guide on opening up high quality cases.
It will also not contain everything in the scope of Intune - this is just a high-level guide of *what* to submit for the majority of cases. 

&nbsp;
***
## Table of Contents
- [Purpose of this guide](#Opening-quality-Support-cases-for-Intune)
- [Required info for all cases](#required-for-all-cases)

- [How to find technical details](#finding-technical-detail)
- Additional Information to be collected by topic
    - [App Protection and Configuration Policies](app.md)
    - [App Deployment](AppDeploy.md)
    - [Device Configuration and Restriction Policies](DevConfig.md)
    - [Device Compliance Policies](DevCompli.md)
    - [Windows Autopilot](autopilot.md)
    - [Windows](windows.md)
    - [Android](android.md)
    - [iOS/macOS/Apple](apple.md)
    - [Portal/Reporting](portal.md)

&nbsp;
# Required for all cases

Each case should contains the following **mandatory** information:
> Expand each section for more details.

<!--# Problem Statement-->
<details><summary> &nbsp; 1. Problem Statement. </summary>
<p>

- Summarized description of problem at hand. Be clear and concise.
- What steps are being followed to reproduce the issue? 
</p>
</details>


<details><summary>&nbsp; 2. The scope of the problem.</summary>
<p>

- How many users or devices are affected? 
- Does the issue is impacting several offices or other regions?
- Which business unites are impacted? 
</p>
</details>

<details><summary>&nbsp; 3. Business impact.</summary>
<p>
Briefly describe the impact that this issue has on your business.
Please include specific details such as:

- Potential financial impact.
- Project delays.
- Lost productivity hours from users.
- Deployment blocker.
</p>
</details>

<details><summary>&nbsp; 4. Technical information.</summary>
<p>
The following technical assessment will help us to understand how does the issue reported is reproduced, narrow the behavior to the feature(s) related, and start  our initial investigations to define an action plan towards the solution. 

&nbsp; &nbsp; &nbsp;  **QUESTIONARY:**
>     Please include as much information as possible in every case. 
>     You can copy the questionary and paste it with answers on the new case notes.

1. Is this a new implementation or was working before and start failing?
    * If was working before; approximate when did you start seeing issues?
2. What platform is affected? (iOS, Windows, Android)
3. Is this is related to a policy? 
    * If so – what kind of policy? App Protection Policy? SCEP? VPN?
    * Include the exact name of the policy in the case.
4. Is there currently an affected device that we can actively use to troubleshoot? 
5. What is the User Principal Name (UPN) of a user affected?
    * If more than one user is affected include 2 or 3 users affected.
6. What is the Intune DeviceId? (Navigate to the device in the Intune Portal, and click on “Hardware”)
    * If more than one device is affected include 2 or 3 devices affected.
7. What is the device serial number?
8. How many users are affected? How many devices?
9. Does this affect the same user on other devices from the same or different platforms?


***
</p>
</details>

## 

&nbsp;
### Example: 
|  |  |
| --- | --- |
| TITLE: | Cannot reset Intune Managed App PIN |
| DESCRIPTION: | We tried to change the PIN App of the following App Edge and Outlook in iOS. The change apparently was successful, however, when we are requested to provide the PIN the previous one is persistent. |
| SCOPE: | The issue is impacting 2k iOS enrolled devices located on US coast region where 3 branch offices are located |
| BUSINESS IMPACT: | The issue affect the sales representatives and could not perform business. This issue has a potential financial impact.|
| TECHNICAL INFORMATION: | <ul><li>This was working before.</li><ul><li>It was reported on 01/31/2022. We could repro 24hr later the first report</li></ul><li>iOS Apps affected. Android Apps are working fine.</li><li>The policy related is an App protection policy.</li><UL><li>The policy name is "Prod-APP iOS - US Sales"</li></ul><li>This was reproduces on my test device and also sales representatives</li><li>My test user UPN affected is: test1@contoso.com </li><ul><li>Other users affected: sales1@contoso.com and sales2@contoso.com </li></ul><li>The IntuneDeviceID for my test device configured with my test user affected is: b4gf5dc3-5f97-4501-9640-0g70h3e8cd21</li><ul><li>The IntuneDeviceID for the other test users is: sales1: f6efe34e-5ed344700-9340-0ffad3687589. Sales 2: b6efh6ce-5567-47gt-9ga6-08ga63782521.</li></ul><li>This issue is affecting 2k users but the numbers are not increasing.</li>|
|  |  |

## Finding technical detail

- Devices
    - Serial Number 
    - Device Id. 
    These can be found under the “Hardware” tab
    - ![A device's Hardware Tab](images/device-details-hardware-tab.png)
- Users
    - User Principal Name (e.g., user@domain.com)
- Applications
    - The exact name of the application & the platform (e.g., iOS, Windows, Win32, MSI, etc.).
    - Application ID – found in the URL when you open an app:
    - ![Showing the ApplicationId in the URL](images/app-id-in-url.png)
- Policies
    - We just need the *exact name of the policy.*
