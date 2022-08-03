[Back to main](index.md)

# Autopilot 

You can use the following documentation to troubleshoot general Device Enrollment issues. 
[Troubleshooting Autopilot](https://docs.microsoft.com/en-us/mem/autopilot/troubleshooting)

Collect the following information: 
1. Which device OS version is affected?  
2. What is the user experience? Be detailed - what is the type of profile/join being done?
3. What is the enrollment type being attempted? You can use the following doc to reference possible enrollment types in Intune.  
4. Gather MDM diagnostic logs using the below info during Out of Box Experience (OOBE).

[Use command to collect logs directly from Windows 10 PCs](https://docs.microsoft.com/en-us/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10#use-command-to-collect-logs-directly-from-windows10-pcs)

Press Shift + F10 during OOBE to launch a command prompt, and then run the below command to generate a diagnostics report:
```PowerShell
mdmdiagnosticstool.exe -area DeviceEnrollment;DeviceProvisioning;Autopilot -zip c:\users\public\documents\MDMDiagReport.zip
```

Upload this file with the case.