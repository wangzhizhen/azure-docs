---
title: Create configurations from existing servers for Azure Automation State Configuration
description: This article tells how to create configurations from existing servers for Azure Automation State Configuration.
keywords: dsc,powershell,configuration,setup
services: automation
ms.subservice: dsc
ms.date: 08/08/2019
ms.topic: conceptual
---

# Create configurations from existing servers

> Applies To: Windows PowerShell 5.1

Creating configurations from existing servers can be a challenging task.
You might not want *all* settings,
just those that you care about.
Even then you need to know in what order the settings
must be applied in order for the configuration to apply successfully.

> [!NOTE]
> This article refers to a solution that is maintained by the Open Source community.
> Support is only available in the form of GitHub collaboration, not from Microsoft.

## Community project: ReverseDSC

A community maintained solution named
[ReverseDSC](https://github.com/microsoft/reversedsc)
has been created to work in this area starting SharePoint.

The solution builds on the
[SharePointDSC resource](https://github.com/powershell/sharepointdsc)
and extends it to orchestrate
[gathering information](https://github.com/Microsoft/sharepointDSC.reverse#how-to-use)
from existing servers running SharePoint.
The latest version has multiple
[extraction modes](https://github.com/Microsoft/SharePointDSC.Reverse/wiki/Extraction-Modes)
to determine what level of information to include.

The result of using the solution is generating
[Configuration Data](https://github.com/Microsoft/sharepointDSC.reverse#configuration-data)
to be used with SharePointDSC configuration scripts.

Once the data files have been generated,
you can use them with
[DSC Configuration scripts](/powershell/dsc/overview/overview)
to generate MOF files
and
[upload the MOF files to Azure Automation](./tutorial-configure-servers-desired-state.md#create-and-upload-a-configuration-to-azure-automation).
Then register your servers from either
[on-premises](./automation-dsc-onboarding.md#enable-physicalvirtual-linux-machines)
or [in Azure](./automation-dsc-onboarding.md#enable-azure-vms)
to pull configurations.

To try out ReverseDSC, visit the
[PowerShell Gallery](https://www.powershellgallery.com/packages/ReverseDSC/)
and download the solution or click "Project Site"
to view the
[documentation](https://github.com/Microsoft/sharepointDSC.reverse).

## Next steps

- To understand PowerShell DSC, see [Windows PowerShell Desired State Configuration overview](/powershell/dsc/overview/overview).
- Find out about PowerShell DSC resources in [DSC Resources](/powershell/dsc/resources/resources).
- For details of Local Configuration Manager configuration, see [Configuring the Local Configuration Manager](/powershell/dsc/managing-nodes/metaconfig).
