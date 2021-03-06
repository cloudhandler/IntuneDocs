---
# required metadata

title: Early edition
description:
keywords:
author: brenduns  
ms.author: brenduns
manager: angrobe
ms.date: 10/19/2017
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: f49650f4-31fa-406c-a4da-d8c9a4a8384d

# optional metadata

ROBOTS: NOINDEX,NOFOLLOW
#audience:
#ms.devlang:
ms.reviewer: cacampbell
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-classic
---

# The early edition for Microsoft Intune - October 2017

The **early edition** provides a list of features that are coming in upcoming releases of Microsoft Intune. This information is provided on a limited basis and is subject to change. Do not share this information outside of your company. Some features listed here are at risk of not making the cutoff dates and may be delayed until a future release. Other features are being tested in a pilot (flighting) to ensure they're customer-ready. Reach out to your Microsoft product group contact if you have any questions or concerns.

This page is updated periodically. Check back for additional updates.

> [!Note]
>The following changes are under development for Intune. For more information about new hybrid features, check out our [hybrid What’s New page](/sccm/mdm/understand/whats-new-in-hybrid-mobile-device-management).

<!--
## What's coming to Intune in the Azure portal  
## What's coming to Intune apps
## Notices
-->



## Intune in the Azure portal

### Azure Active Directory web sites can require the Intune Managed Browser App and support Single Sign-On for the Managed Browser (Public Preview) <!-- 710595 -->   
Using Azure Active Directory (Azure AD), you will be able to restrict access to web sites on mobile devices to the Intune Managed Browser app. In the managed browser, web site data will remain secure and separate from end-user personal data. In addition, the Managed Browser will support Single Sign-On capabilities for sites protected by Azure AD. Signing in to the Managed Browser, or using the Managed Browser on a device with another app managed by Intune, allows the Managed Browser to access corporate sites protected by Azure AD without the user having to enter their credentials. This functionality applies to sites like Outlook Web Access (OWA) and SharePoint Online, as well as other corporate sites like intranet resources accessed through the Azure App Proxy.

### Troubleshoot enrollment issues  <!--- 746324 --->  
The Troubleshoot workspace will show user enrollment issues. Details about the issue and suggested remediation steps can help admins and help desk operators troubleshoot problems. Certain enrollment issues aren't captured and some errors might not have remediation suggestions.

### Admins can now configure the Firewall settings on a device using a device configuration profile <!-- 951708 -->   
Admins can turn on firewall for devices, and also configure various protocols for domain, private, and public networks.  These firewall settings can be found in the "Endpoint protection" profile.

### Windows Defender Application Guard helps protect devices from untrusted websites, as defined by your organization <!-- 958257 -->   
Admins can define sites as "trusted" or "corporate" using a Windows Information Protection workflow or the new "Network boundary" profile under device configurations. Any sites that aren't listed in on a 64-bit Windows 10 device’s trusted network boundary, if they are viewed with Microsoft Edge, open instead in a browser within a Hyper-V virtual computer.

Application Guard can be found in the device configuration profiles, in the "Endpoint protection" profile. From there, admins can configure interaction between the virtualized browser and the host machine, nontrusted sites and trusted sites, and storing data generated in the virtualized browser. To use Application Guard on a device, a network boundary first must be configured. It's important to define only one network boundary for a device.  

### Windows Defender Application Guard on Windows 10 Enterprise provides mode to trust only authorized apps <!-- 1031096 -->    
With thousands of new malicious files created every day, using antivirus signature-based detection to fight against malware might no longer provide an adequate defense against new attacks. Using Windows Defender Application Guard on Windows 10 Enterprise, you can change device configuration from a mode where apps are trusted unless blocked by an antivirus or other security solution, to a mode where the operating system trusts only apps authorized by your enterprise. You assign trust to apps in Windows Defender Application Guard.

Using Intune, you can configure the application control policies either in "audit only" mode or enforce mode. Apps will not be blocked when running in “audit only” mode. “Audit only” mode logs all events in local client logs. You can also configure whether only Windows components and Windows Store apps are allowed to run or whether additional apps with good reputations as defined by the Intelligent Security Graph will be allowed to run.

### New enrollment status page for Windows 10 enrollments <!--1063201-->    
You can now configure a greeting that appears when your users enroll Windows 10 devices. Use the **Enrollment Status Screen** to configure a custom message and a hyperlink to be displayed to your end users when they enroll their Windows 10 devices.  The **Enrollment Status Screen** will also give end users a view into the progress of policy settings that are being applied to their device.  

### Window Defender Exploit Guard is a new set of intrusion prevention capabilities for Windows 10 <!-- 1063615 -->   
Window Defender Exploit Guard includes custom rules to reduce the exploitability of applications, prevents macro and script threats, automatically blocks network connections to low reputation IP addresses, and can secure data from ransomware and unknown threats. Windows Defender Exploit Guard consists of the following components:

- **Attack Surface Reduction (ASR)** provides rules that allow you to prevent macro, script, and email threats.
- **Controlled Folder access** automatically blocks access to content to protected folders.
- **Network Filter** blocks outbound connection from any app to low rep IP/domain
- **Exploit Protection** provides memory, control flow, and policy restrictions that can be used to protect an application from exploits.

### App-conditional launch support <!-- 1193313 -->
IT admins can now set a requirement through the Azure admin portal to enforce a passcode instead a numeric PIN through the mobile app management (MAM) when the application launch. If configured, the user will be required to set and use a passcode when prompted before getting access to MAM-enlightened applications. A passcode is defined as a numeric PIN with at least one special character or upper/lowercase alphabet. This release of Intune will enable this feature **on iOS only**. Intune supports passcode in a similar way to numeric PIN, it sets a minimum length, allowing repeat characters and sequences. This feature requires the participation of applications (i.e WXP, Outlook, Managed Browser, Yammer) to integrate the Intune APP SDK with the code for this feature in place for the passcode settings to be enforced in the targeted applications.

### App version number for line-of-business in device install status report <!-- 1233999 -->  
The device install status report will display the app version number for the line-of-business apps for iOS and Android. You may use this information to troubleshoot your apps, or find devices that are running outdated app versions.

### Co-management for Windows 10 devices  <!-- 124445 -->
Co-management is a solution that provides a bridge from traditional to modern management, and it provides you with a path to make the transition using a phased approach. At its foundation, co-management is a solution where Windows 10 devices are concurrently managed by Configuration Manager and Microsoft Intune, as well as joined to Active Directory (AD) and Azure Active Directory (Azure AD).  This configuration provides you with a path to modernize over time, at the pace that’s right for your organization if you can’t move all at once.  

### Set access for apps by minimum Android security patch on the device<!-- 1278463 -->   
An administrator will be able to define the minimum Android security patch that must be installed on the device in order to gain access to a managed application under a managed account.

> [!Note]  
> This feature only restricts security patches released by Google on Android 6.0+ devices.

### New device restriction settings for Windows 10      <!-- 1308850 -->
-    Messaging (mobile only) - disable testing or MMS messages
-    Password - settings to enable FIPS and the use of Windows Hello devices secondary devices for authentication 
-    Display - settings to turn on or off GDI Scaling for legacy apps


### Windows 10 kiosk mode device restrictions <!-- 1308872 -->   
You will be able to restrict Windows 10 device users to kiosk mode, which limits users to a set of predefined apps.  To do so, create a Windows 10 device restriction profile and set the Kiosk settings.

Kiosk mode supports two modes: **single app** (allows a user to run just one app) or **multi app** (permits access to a set of apps).  You define the user account and device name, which determines the supported apps).  When the user is logged in, they're limited to the defined apps.  To learn more, see [AssignedAccess CSP](https://docs.microsoft.com/windows/client-management/mdm/assignedaccess-csp). 

Kiosk mode requires:

- Intune must be the MDM authority.
- The apps must already be installed on the target device.
- The device must be [properly provisioned](https://docs.microsoft.com/windows/configuration/set-up-a-kiosk-for-windows-10-for-desktop-editions).

### New device configuration profile for creating network boundaries <!-- 1311967 -->   
We have created a device configuration profile called **Network boundary** that can be found with your other device configuration profiles. Use this profile to define online resources that you want to be considered corporate and trusted. You must define a network boundary for a device *before* features such as Windows Defender Application Guard and Windows Information Protection can be used on the device. It’s important to define only one network boundary for each device.

You can define enterprise cloud resources, IP address ranges, and internal proxy servers that you want to be considered trusted. Once defined, the network boundary can be consumed by other features such as Windows Defender Application Guard and Windows Information Protection.

###  Two additional settings for Windows Defender Antivirus <!-- 1338409 -->  
**File blocking level**

| | |
|---|---|
| Not Configured | **Not Configured** uses the default Windows Defender Antivirus blocking level and provides strong detection without increasing the risk of detecting legitimate files. |
| High | **High** applies a strong level of detection.
| High +  | **High +** provides the High level with additional protection measures that might impact client performance.
| Zero tolerance  | **Zero tolerance** blocks all unknown executables. |

While unlikely, setting to **High** may cause some legitimate files to be detected.
We recommend you set File blocking level to the default, **Not configured**.

**Timeout extension for file scanning by the cloud**  

| | |
|--|--|
| Number of seconds (0-50) | Specify the maximum amount of time that Windows Defender Antivirus should block a file while waiting for a result from the cloud. The default amount is 10 seconds: any additional time specified here (up to 50 seconds) is added to those 10 seconds. In most cases, the scan takes much less time than the maximum. Extending the time allows the cloud to thoroughly investigate suspicious files. We recommend that you enable this setting and specify at least 20 additional seconds. |


### Support for Symantec Cloud Certification Authority (CA)  <!-- 1333638 -->    
Intune now supports Symantec Cloud CA which allows the Intune Certificate Connector to issue PKCS certificates from the Symantec Cloud CA to Intune managed devices. If you're already using the Intune Certificate Connector with Microsoft Certification Authority (CA), you can leverage the existing Intune Certificate Connector setup to add the Symantec CA support.



### Citrix VPN added for Windows 10 devices <!-- 1512457 -->  
Customer will be able to configure Citrix VPN for their Windows 10 devices. You can choose the Citrix VPN in the *Select a connection type* list in the **Base VPN** blade when configuring a VPN for Windows 10 and later.

> [!Note]
> Citrix configuration existed for iOS and Android.





<!-- the following are present prior to 1710 -->

### Google Play Protect support on Android <!-- 908720  -->  
With the release of Android Oreo, Google introduces a suite of security features called Google Play Protect that allow users and organizations to run secure apps and secure Android images. Intune will support Google Play Protect features, including SafetyNet remote attestation.  Admins can set compliance policy requirements that require Google Play Protect be configured and healthy. The **SafetyNet device attestation** setting requires the device to connect with a Google service to verify that the device is healthy and is not compromised. Admins can also set a configuration profile setting for Android for Work to require that installed apps are verified by Google Play services.  Conditional access might block users from accessing corporate resources if a device is not compliant with Google Play Protect requirements. 


### Support for Windows 10 edition upgrade policy   <!-- 903672(archived), 1119689 -->  
You will be able to create a Windows 10 edition upgrade policy that upgrades Windows 10 devices to Windows 10 Education, Windows 10 Education N, Windows 10 Professional, Windows 10 Professional N, Windows 10 Professional Education, and Windows 10 Professional Education N.
For details about Windows 10 edition upgrades, see [How to configure Windows 10 edition upgrades](edition-upgrade-configure-windows-10.md).


### Intune MAM and Outlook for Android add-ins  <!-- 1450688 -->
In a few weeks, the Office team will announce add-ins for Outlook on Android. This add-in feature set already exists in Outlook on Windows, iOS, web and Mac. Because add-ins are managed via Exchange, users will be able to copy and share data and messages across Outlook and unmanaged add-in applications, unless access to add-ins is turned off by your Exchange admin. 

To manage user access permissions to add-ins, work with your Exchange admin to ensure that your MAM data protection policies apply to add-ins.

#### How does this affect me?
If your Exchange policies are already set to prevent side loading add-ins or installing add-ins, then read no further. Your MAM policies will apply as expected. If, however, you have set policies in MAM to restrict cut, copy, and paste operations within Outlook on Android and have not set your add-in policy in Exchange, you should know that by default, users will be able to install add-ins to Outlook. These add-ins can access message body, subject and other message properties. You can turn off the user's ability to install add-ins by having your Exchange Admin remove the “My Marketplace Apps” and “My Custom Apps” roles.

The setting change in Exchange will apply to Outlook across Windows, iOS, web, Mac, and mobile. 

#### What do I need to do?
Review your Exchange policies today. Inform your IT and helpdesk staff. Contact our support team with any specific questions or concerns. 




<!-- the following are present prior to 1709 -->

### Actions for non-compliance  <!--730266  846515 -->     
*Actions for non-compliance* are a new feature of compliance policies that will let you take action on devices that are out of compliance. You can specify single or multiple actions and specify the time period at which those actions must occur. For example, you can notify users of non-compliant devices immediately after the devices become non-compliant through email, or you can block non-compliant devices from accessing corporate resources after a 3-day grace period via Conditional Access.

### Android for Work support for Lookout <!-- 1087312 -->   
Intune connector with Lookout will support Android for Work devices when using the Lookout for Work app. You are able to deploy the Lookout app inside or outside the container.

### Intune App Protection and Citrix MDX Development Tools <!-- 709185 -->
You can manage devices and apps with a combination of Citrix XenMobile MDX and Microsoft Intune. This allows you to manage apps with Intune app protection policy while using Citrix’s mVPN technology.

You are able to find a code repository that contains the Intune App Wrapping Tool and Intune App SDK for iOS and Android, integrating with Citrix MDX mVPN technology.

#### How integration with Intune works
Risk is assessed based on telemetry collected from devices running Zimperium. You can configure EMS conditional access policies based on Zimperium risk assessment enabled through Intune device compliance policies, which you can use to allow or block non-compliant devices to access corporate resources based on detected threats.

### On-premises Exchange connector high availability support  <!-- 676614 -->   
You are able to have multiple Client Access Server (CAS) roles for on-premises Exchange connector. For example, if the main CAS fails, the Exchange connector receives a query to fall back to other CASs. This feature ensures that the service is not interrupted.

### System Center Operations Manager management pack for Exchange connector <!-- 885457 -->   
The System Center Operations Manager management pack for Exchange connector will be available to help you parse the Exchange connector logs. This management pack gives you different ways of monitoring Intune when you need to troubleshoot issues.


## Intune apps


### Redirecting macOS users to our new Company Portal app <!--1380728-->   
When an end user logs into the Company Portal website to enroll their macOS device, they will be directed to download the new Company Portal app for macOS to complete the process. This occurs for macOS devices using OS X El Capitan 10.11 or above. 

### Certificate-based authentication support on the Company Portal for iOS <!--1029830-->
We have added support for certificate-based authentication (CBA) in the Company Portal app for iOS. Users with CBA enter their username, then tap the “Sign in with a certificate” link. CBA is already supported on the Company Portal apps for Android and Windows. You can learn more on the [sign in to the Company Portal app](https://docs.microsoft.com/intune-user-help/sign-in-to-the-company-portal) page.

<!-- the following are present prior to 1710 -->



### Apps that are available with or without enrollment can now be installed without being prompted for enrollment. <!-- 1334712 -->
Company apps that have been made available with or without enrollment on the Android Company Portal app can be installed without a prompt to enroll.


<!-- the following are present prior to 1709 -->

### Intune Managed Browser support for iOS and Android <!-- 1374196 -->
As of October 2017, the Intune Managed Browser app on Android app will support only devices running Android 4.4 and later. The Intune Managed Browser app on iOS will support only devices running iOS 9.0 and later. Earlier versions of Android and iOS will be able to continue using the Managed Browser, but will be unable to install new versions of the app and might not be able to access all of the app capabilities. We encourage you to update these devices to a supported operating system version.


### Improved error message for when a user reaches the maximum number of devices allowed to enroll <!-- 1270370 -->
Instead of a generic error message, end users see a friendly, actionable error message: "You have enrolled the maximum number of devices allowed by your IT admin. Please remove an enrolled device or get help from your IT admin."




## Notices

### Device and app management integration <!-- 677972 -->   
Now that Intune’s mobile device management (MDM) and mobile application management (MAM) are both accessible from the Azure portal, Intune started integrating the IT admin experience around application and device management. These changes are geared to simplify your device and app management experience.

Learn more about the MDM and MAM changes announced in the [Intune support team blog](https://blogs.technet.microsoft.com/intunesupport/2017/09/19/support-tip-setting-up-communication-between-mam-managed-and-mdm-managed-apps/).




### See also
See [What’s New in Microsoft Intune](whats-new.md) for details on recent developments.
