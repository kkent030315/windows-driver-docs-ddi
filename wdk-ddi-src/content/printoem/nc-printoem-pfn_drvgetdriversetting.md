---
UID: NC:printoem.PFN_DrvGetDriverSetting
title: PFN_DrvGetDriverSetting (printoem.h)
description: The DrvGetDriverSetting function is obsolete.
old-location: print\drvgetdriversetting.htm
tech.root: print
ms.date: 04/20/2018
keywords: ["PFN_DrvGetDriverSetting callback function"]
ms.keywords: DrvGetDriverSetting, DrvGetDriverSetting callback function [Print Devices], PFN_DrvGetDriverSetting, PFN_DrvGetDriverSetting callback, print.drvgetdriversetting, print_obsoletefunctions_655cde75-fc70-4d6c-a7b4-8eb1e068ebd9.xml, printoem/DrvGetDriverSetting
req.header: printoem.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - PFN_DrvGetDriverSetting
 - printoem/PFN_DrvGetDriverSetting
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - printoem.h
api_name:
 - PFN_DrvGetDriverSetting
---

# PFN_DrvGetDriverSetting callback function


## -description

The <b>DrvGetDriverSetting</b> function is obsolete.

 Windows 2000 and later printer drivers should use <a href="/windows-hardware/drivers/ddi/prcomoem/nf-prcomoem-iprintoemdriverui-drvgetdriversetting">IPrintOemDriverUI::DrvGetDriverSetting</a>, <a href="/windows-hardware/drivers/ddi/prcomoem/nf-prcomoem-iprintcoreui2-drvgetdriversetting">IPrintCoreUI2::DrvGetDriverSetting</a> (UI plug-ins), <a href="/windows-hardware/drivers/ddi/prcomoem/nf-prcomoem-iprintoemdriveruni-drvgetdriversetting">IPrintOemDriverUni::DrvGetDriverSetting</a> (Unidrv plug-ins) or <a href="/windows-hardware/drivers/ddi/prcomoem/nf-prcomoem-iprintoemdriverps-drvgetdriversetting">IPrintOemDriverPS::DrvGetDriverSetting</a> (Pscript plug-ins) 

This function pointer type defines the type of the <b>DrvGetDriverSetting</b> member of the <a href="/windows-hardware/drivers/ddi/printoem/ns-printoem-_oemuiprocs">OEMUIPROCS</a> and <a href="/windows-hardware/drivers/ddi/printoem/ns-printoem-_drvprocs">DRVPROCS</a> structures.

## -parameters

### -param pdriverobj

### -param Feature

### -param pOutput

### -param cbSize

### -param pcbNeeded [out, optional]



### -param pdwOptionsReturned [out, optional]



