[Back to main](index.md)

# Windows
Please ensure that we start with [the details found here](index.md#required-for-all-cases) to begin. 

Additionally, there are (2) additional sets of logs that are useful to Support.

## One Data Collector

One Data Collector, aka "ODC", is the preferred and easily-readible way to gather logs from your Windows devices.

It does require administrator privileges, however, so it is not always possible - but it is the easiest way to gather logs and review them. 

[You can find the current steps to gather the ODC here](https://github.com/markstan/IntuneOneDataCollector#intune-one-data-collector)

***Please gather ODC logs by running the below in an elevated PowerShell prompt.***

```PowerShell
wget https://aka.ms/intunexml -outfile Intune.xml
wget https://aka.ms/intuneps1 -outfile IntuneODCStandAlone.ps1
powerShell -ExecutionPolicy Bypass -File .\IntuneODCStandAlone.ps1
```

You can then upload the generated file with the case.

## Collect Diagnostics
Alternatively, you can gather diagnostics from the Intune service. 
Intune will have the device generate logs, the device will upload the logs to Intune, and then you can download them from the portal. 

This can be much slower, but can be done remotely & from the Intune portal - so it is much more convenient.

[Collect diagnostics from a Windows device](https://docs.microsoft.com/en-us/mem/intune/remote-actions/collect-diagnostics)