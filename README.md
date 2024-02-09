# JamfCheck
[![Static Badge](https://img.shields.io/badge/SwiftUI-524520?logo=swift)](https://developer.apple.com/xcode/swiftui/)
![](https://img.shields.io/badge/macOS-10.13%2B-success)&nbsp;![GitHub all releases](https://img.shields.io/github/downloads/txhaflaire/JamfCheck/total)&nbsp;![GitHub](https://img.shields.io/github/license/txhaflaire/JamfCheck)
[![GitHub release (with filter)](https://img.shields.io/github/v/release/txhaflaire/JamfCheck?color=green&label=Latest%20Release)](https://github.com/txhaflaire/JamfCheck/releases)


The "JamfCheck" is a Apple code-signed and notarized macOS app that allows you to easily run a couple of check's for Jamf Pro, Jamf Connect and Jamf Protect in a single app.

You can find the latest version in the [releases](https://github.com/txhaflaire/JamfCheck/releases) section

<img width="256" alt="AppIcon" src="./Images/AppIcon.png">

#### Requirements

- A Mac running macOS Ventura (13.0) or higher

#### Usage
At launch the app requires to you make a selection in the NavigationView, select either
  - ###### Device Info
    - Displays generic Device, Endpoint Security and User related information which can be easily copied to clipboard, also provides notifications if Software Updates are available.
      
  - ###### Device Management
    - Displays Checks that are related to Jamf Pro, Jamf School or Jamf Now
    - Show and Export Jamf Pro logs
    - Jamf Network Test, providing an option to export results to CSV as well

  - ###### Identity and Access Management
      - Displays Checks that are related to Jamf Connect
      - Show or Stream and Export logs from Jamf Connect

  - ###### Endpoint Security
    - Displays Checks that are related to Jamf Protect
    - Show or Stream and Export logs from Jamf Protect
    - Provides various detections to be triggered in a single view
    - Provides a way to test Web Protection for Jamf Protect
    - Test connectivity to SIEM/Webhook solutions using HTTP
    - Initiate and review XProtect Remediator Scan Results
  
Data is automatically being fetch each 30 seconds or the preferred interval set in the Settings menu, or alternatively can be refreshed using the refresh button located on the right bottom corner (cmd+r)

The app does log to Unified Logging. You can view the logs like this:

`log show --predicate 'subsystem == "com.txhaflaire.JamfCheck"' --info`
`log stream --predicate 'subsystem == "com.txhaflaire.JamfCheck"' --level info`

#### Screenshots

*JamfCheck Auto Update*
<img width="1027" alt="JamfCheckDeviceInfo" src="./Images/JamfCheckDeviceInfo.png">
*JamfCheck for Jamf Pro*
<img width="1027" alt="JamfCheck" src="./Images/JamfCheck.png">
*JamfCheck for Jamf Pro and running a Network Test*
<img width="1027" alt="JamfCheckNetworkTest" src="./Images/JamfCheckNetworkTester.png">
*JamfCheck for Jamf Connect*
<img width="1027" alt="JamfCheckLight" src="./Images/JamfCheckLight.png">
*JamfCheck for Jamf Protect*
<img width="1027" alt="JamfCheckDark" src="./Images/JamfCheckDark.png">
*JamfCheck Analyze Diagnostics for Jamf Protect*
<img width="1027" alt="JamfCheckAnalyzeDiagnostics" src="./Images/JamfCheckAnalyzeDiagnostic.gif">
