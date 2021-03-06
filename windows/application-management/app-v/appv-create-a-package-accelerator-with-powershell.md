---
title: How to Create a Package Accelerator by Using Windows PowerShell (Windows 10)
description: How to Create a Package Accelerator by Using Windows PowerShell
author: MaggiePucciEvans
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
---


# How to Create a Package Accelerator by Using Windows PowerShell

**Applies to**
-   Windows 10, version 1607

App-V package accelerators automatically sequence large, complex applications. Additionally, when you apply an App-V package accelerator, you are not always required to manually install an application to create the virtualized package.

**To create a package accelerator**

1.  Install the App-V sequencer. For more information about installing the sequencer see [How to Install the Sequencer](appv-install-the-sequencer.md).

2.  To open a Windows PowerShell console, click **Start** and type **PowerShell**. Right-click **Windows PowerShell** and select **Run as Administrator**. Use the **New-AppvPackageAccelerator** cmdlet.

3.  To create a package accelerator, make sure that you have the .appv package to create an accelerator from, the installation media or installation files, and optionally a read me file for consumers of the accelerator to use. The following parameters are required to use the package accelerator cmdlet:

    -   **InstalledFilesPath** - specifies the application installation path.

    -   **Installer** – specifies the path to the application installer media

    -   **InputPackagePath** – specifies the path to the .appv package

    -   **Path** – specifies the output directory for the package.

    The following example displays how you can create a package accelerator with an .appv package and the installation media:

    **New-AppvPackageAccelerator -InputPackagePath &lt;path to the .appv file&gt; -Installer &lt;path to the installer executable&gt; -Path &lt;directory of the output path&gt;**

    An additional optional parameter that can be used with the **New-AppvPackageAccelerator** cmdlet is as follows:

    -   **AcceleratorDescriptionFile** - specifies the path to user created package accelerator instructions. The package accelerator instructions are **.txt** or **.rtf** description files that will be packaged with the package created using the package accelerator.

## Have a suggestion for App-V?

Add or vote on suggestions on the [Application Virtualization feedback site](https://appv.uservoice.com/forums/280448-microsoft-application-virtualization).<br>For App-V issues, use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/en-US/home?forum=mdopappv).

## Related topics

[Administering App-V by Using Windows PowerShell](appv-administering-appv-with-powershell.md)
