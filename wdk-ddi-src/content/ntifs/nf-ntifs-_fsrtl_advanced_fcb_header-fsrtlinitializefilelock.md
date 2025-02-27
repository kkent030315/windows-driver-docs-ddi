---
UID: NF:ntifs.FsRtlInitializeFileLock
title: FsRtlInitializeFileLock function (ntifs.h)
description: The FsRtlInitializeFileLock routine initializes a FILE_LOCK structure.
old-location: ifsk\fsrtlinitializefilelock.htm
tech.root: ifsk
ms.date: 04/16/2018
keywords: ["FsRtlInitializeFileLock function"]
ms.keywords: FsRtlInitializeFileLock, FsRtlInitializeFileLock routine [Installable File System Drivers], fsrtlref_227dc998-43e4-427b-afe5-6d26ff5d1c36.xml, ifsk.fsrtlinitializefilelock, ntifs/FsRtlInitializeFileLock
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
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
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: <= APC_LEVEL
targetos: Windows
req.typenames: 
ms.custom: RS5
f1_keywords:
 - FsRtlInitializeFileLock
 - ntifs/FsRtlInitializeFileLock
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - FsRtlInitializeFileLock
dev_langs:
 - c++
---

# FsRtlInitializeFileLock function


## -description

The <b>FsRtlInitializeFileLock</b> routine initializes a FILE_LOCK structure.

## -parameters

### -param FileLock [in]


Pointer to an uninitialized FILE_LOCK structure.

### -param CompleteLockIrpRoutine [in, optional]


Pointer to a <a href="/windows-hardware/drivers/ifs/pcomplete-lock-irp-routine">PCOMPLETE_LOCK_IRP_ROUTINE</a>-typed callback routine to be called when an <a href="/windows-hardware/drivers/ifs/irp-mj-lock-control">IRP_MJ_LOCK_CONTROL</a> request is completed. This parameter is optional and can be <b>NULL</b>.

### -param UnlockRoutine [in, optional]


Pointer to a <a href="/windows-hardware/drivers/ifs/punlock-routine">PUNLOCK_ROUTINE</a>-typed callback routine to be called when the byte range is unlocked. This parameter is optional and can be <b>NULL</b>.

## -remarks

<b>FsRtlInitializeFileLock</b> initializes an uninitialized FILE_LOCK structure. 

It is a programming error to call <b>FsRtlInitializeFileLock</b> for a FILE_LOCK structure that has already been initialized by <b>FsRtlInitializeFileLock</b> or <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlallocatefilelock">FsRtlAllocateFileLock</a>, unless the structure has been uninitialized by a subsequent call to <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-_fsrtl_advanced_fcb_header-fsrtluninitializefilelock">FsRtlUninitializeFileLock</a>.

Once initialized, the FILE_LOCK structure can be used to lock a byte range in a file by calling <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlprocessfilelock">FsRtlProcessFileLock</a> or <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-fsrtlfastlock">FsRtlFastLock</a>. <b>FsRtlProcessFileLock</b> processes lock IRPs. <b>FsRtlFastLock</b> performs non-IRP locking.

When the FILE_LOCK structure is no longer needed, it can be uninitialized by calling <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-_fsrtl_advanced_fcb_header-fsrtluninitializefilelock">FsRtlUninitializeFileLock</a>. The uninitialized FILE_LOCK structure can then be initialized for reuse by calling <b>FsRtlInitializeFileLock</b>.

Minifilters must call <a href="/windows-hardware/drivers/ddi/fltkernel/nf-fltkernel-fltinitializefilelock">FltInitializeFileLock</a> instead of <b>FsRtlInitializeFileLock</b>.

## -see-also

<a href="/windows-hardware/drivers/ddi/fltkernel/nf-fltkernel-fltinitializefilelock">FltInitializeFileLock</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlallocatefilelock">FsRtlAllocateFileLock</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-fsrtlaretherecurrentfilelocks">FsRtlAreThereCurrentFileLocks</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-fsrtlfastlock">FsRtlFastLock</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlprocessfilelock">FsRtlProcessFileLock</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-_fsrtl_advanced_fcb_header-fsrtluninitializefilelock">FsRtlUninitializeFileLock</a>



<a href="/windows-hardware/drivers/ifs/irp-mj-lock-control">IRP_MJ_LOCK_CONTROL</a>



<a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-iocompleterequest">IoCompleteRequest</a>



<a href="/windows-hardware/drivers/ifs/pcomplete-lock-irp-routine">PCOMPLETE_LOCK_IRP_ROUTINE</a>



<a href="/windows-hardware/drivers/ifs/punlock-routine">PUNLOCK_ROUTINE</a>
