---
UID: NF:ntifs.RtlRandom
title: RtlRandom function (ntifs.h)
description: The RtlRandom routine returns a random number that was generated from a given seed value.
old-location: ifsk\rtlrandom.htm
tech.root: ifsk
ms.date: 04/16/2018
keywords: ["RtlRandom function"]
ms.keywords: RtlRandom, RtlRandom routine [Installable File System Drivers], ifsk.rtlrandom, ntifs/RtlRandom, rtlref_c9c196b4-7335-4320-ae7f-7c565b6f73e6.xml
req.header: ntifs.h
req.include-header: Ntifs.h, Fltkernel.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later.
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
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: < DISPATCH_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - RtlRandom
 - ntifs/RtlRandom
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - RtlRandom
---

# RtlRandom function


## -description

The <b>RtlRandom</b> routine returns a random number that was generated from a given seed value.

## -parameters

### -param Seed [in, out]


Unsigned long value from which to generate a random number.

## -returns

<b>RtlRandom</b> returns a random number in the range [0..MAXLONG-1].

## -remarks

<b>RtlRandom</b> returns values that are uniformly distributed over the range from zero to the maximum possible LONG value less 1 if it is called repeatedly with the same <i>Seed</i>.

The <b>RtlRandomEx</b> function is an improved version of the <b>RtlRandom</b> function that is twice as fast and produces better random numbers.

## -see-also

<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlrandomex">RtlRandomEx</a>
