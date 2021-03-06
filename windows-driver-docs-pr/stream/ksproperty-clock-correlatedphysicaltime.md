---
title: KSPROPERTY\_CLOCK\_CORRELATEDPHYSICALTIME
description: Clients use the KSPROPERTY\_CLOCK\_CORRELATEDPHYSICALTIME property to compare the current physical time on a clock to the current system time.
ms.assetid: 49f74411-1489-4864-9213-e1894128e355
keywords: ["KSPROPERTY_CLOCK_CORRELATEDPHYSICALTIME Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_CLOCK_CORRELATEDPHYSICALTIME
api_location:
- ks.h
api_type:
- HeaderDef
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# KSPROPERTY\_CLOCK\_CORRELATEDPHYSICALTIME


Clients use the KSPROPERTY\_CLOCK\_CORRELATEDPHYSICALTIME property to compare the current physical time on a clock to the current system time.

## <span id="ddk_ksproperty_clock_correlatedphysicaltime_ks"></span><span id="DDK_KSPROPERTY_CLOCK_CORRELATEDPHYSICALTIME_KS"></span>


### Usage Summary Table

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>Get</th>
<th>Set</th>
<th>Target</th>
<th>Property Descriptor Type</th>
<th>Property Value Type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Yes</p></td>
<td><p>No</p></td>
<td><p>Pin</p></td>
<td><p>[<strong>KSPROPERTY</strong>](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ks/ns-ks-ksidentifier)</p></td>
<td><p>[<strong>KSCORRELATED_TIME</strong>](https://msdn.microsoft.com/library/windows/hardware/ff561033)</p></td>
</tr>
</tbody>
</table>

 

Remarks
-------

The KSCORRELATED\_TIME structure contains the current clock time in the **Time** member and the correlated physical time in the **SystemTime** member.

Also see [KS Clocks](https://msdn.microsoft.com/library/windows/hardware/ff567307).

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Header</p></td>
<td>Ks.h (include Ks.h)</td>
</tr>
</tbody>
</table>

## See also


[**KSPROPERTY\_CLOCK\_PHYSICALTIME**](ksproperty-clock-physicaltime.md)

[**KeQueryPerformanceCounter**](https://msdn.microsoft.com/library/windows/hardware/ff553053)

 

 






