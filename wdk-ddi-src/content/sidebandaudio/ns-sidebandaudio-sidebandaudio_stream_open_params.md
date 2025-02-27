---
UID: NS:sidebandaudio.__unnamed_union_2
title: SIDEBANDAUDIO_STREAM_OPEN_PARAMS (sidebandaudio.h)
description: Describes the variable I/O parameters for IOCTLs.
ms.date: 09/07/2018
keywords: ["SIDEBANDAUDIO_STREAM_OPEN_PARAMS structure"]
ms.keywords: SIDEBANDAUDIO_STREAM_OPEN_PARAMS, SIDEBANDAUDIO_STREAM_OPEN_PARAMS, *PSIDEBANDAUDIO_STREAM_OPEN_PARAMS,
req.header: sidebandaudio.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: SIDEBANDAUDIO_STREAM_OPEN_PARAMS, *PSIDEBANDAUDIO_STREAM_OPEN_PARAMS
targetos: Windows
tech.root: audio
ms.custom: RS5
f1_keywords:
 - PSIDEBANDAUDIO_STREAM_OPEN_PARAMS
 - sidebandaudio/PSIDEBANDAUDIO_STREAM_OPEN_PARAMS
 - SIDEBANDAUDIO_STREAM_OPEN_PARAMS
 - sidebandaudio/SIDEBANDAUDIO_STREAM_OPEN_PARAMS
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sidebandaudio.h
api_name:
 - PSIDEBANDAUDIO_STREAM_OPEN_PARAMS
 - SIDEBANDAUDIO_STREAM_OPEN_PARAMS
---

# SIDEBANDAUDIO_STREAM_OPEN_PARAMS structure


## -description

Describes the variable I/O parameters for IOCTLs.

## -struct-fields

### -field EpIndex

0 based index indicating the Endpoint on device.

### -field Format

Stream Format KSDATAFORMAT.

### -field SiopCount

Number of Input parameters.

### -field Alignment

Alignment - Allows for byte alignment.

## -remarks

Union fields described here.

#### EpIndex

0 based index indicating the Endpoint on device.

#### Format

Stream Format KSDATAFORMAT.

#### SiopCount

Number of Input parameters.

## -see-also

[sidebandaudio.h](index.md)

