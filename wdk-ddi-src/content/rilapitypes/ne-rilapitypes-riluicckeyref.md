---
UID: NE:rilapitypes.RILUICCKEYREF
title: RILUICCKEYREF (rilapitypes.h)
description: "Microsoft reserves the RILUICCKEYREF enumeration for internal use only. Don't use this enumeration in your code."
old-location: netvista\riluicckeyref_2.htm
tech.root: netvista
ms.date: 02/26/2018
keywords: ["RILUICCKEYREF enumeration"]
ms.keywords: RILUICCKEYREF, RILUICCKEYREF enumeration [Network Drivers Starting with Windows Vista], RIL_UICCKEYREF_NEV, RIL_UICCKEYREF_PIN1, RIL_UICCKEYREF_PIN2, RIL_UICCKEYREF_UPIN, netvista.riluicckeyref_2, rilapitypes/RILUICCKEYREF, rilapitypes/RIL_UICCKEYREF_NEV, rilapitypes/RIL_UICCKEYREF_PIN1, rilapitypes/RIL_UICCKEYREF_PIN2, rilapitypes/RIL_UICCKEYREF_UPIN
req.header: rilapitypes.h
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
req.lib: NtosKrnl.exe
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RILUICCKEYREF
req.product: Windows 10 or later.
f1_keywords:
 - RILUICCKEYREF
 - rilapitypes/RILUICCKEYREF
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - rilapitypes.h
api_name:
 - RILUICCKEYREF
---

# RILUICCKEYREF enumeration (rilapitypes.h)


## -description

This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## -enum-fields

### -field RIL_UICCKEYREF_ALW

### -field RIL_UICCKEYREF_PIN1

### -field RIL_UICCKEYREF_UPIN

### -field RIL_UICCKEYREF_PIN2

### -field RIL_UICCKEYREF_NEV

## -syntax

```cpp
typedef enum _RILUICCKEYREF {
  RIL_UICCKEYREF_PIN1,
  RIL_UICCKEYREF_UPIN,
  RIL_UICCKEYREF_PIN2,
  RIL_UICCKEYREF_NEV
} RILUICCKEYREF;
```

