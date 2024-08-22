---
title: Eadsv5 size series
description: Information on and specifications of the Eadsv5-series sizes
author: mattmcinnes
ms.service: azure-virtual-machines
ms.subservice: sizes
ms.topic: conceptual
ms.date: 08/01/2024
ms.author: mattmcinnes
ms.reviewer: mattmcinnes
---

# Eadsv5 sizes series

[!INCLUDE [eadsv5-summary](./includes/eadsv5-series-summary.md)]

## Host specifications
[!INCLUDE [eadsv5-series-specs](./includes/eadsv5-series-specs.md)]

## Feature support
[Premium Storage](../../premium-storage-performance.md): Supported <br>[Premium Storage caching](../../premium-storage-performance.md): Supported <br>[Live Migration](../../maintenance-and-updates.md): Supported <br>[Memory Preserving Updates](../../maintenance-and-updates.md): Supported <br>[Generation 2 VMs](../../generation-2.md): Supported <br>[Generation 1 VMs](../../generation-2.md): Supported <br>[Accelerated Networking](/azure/virtual-network/create-vm-accelerated-networking-cli): Supported <br>[Ephemeral OS Disk](../../ephemeral-os-disks.md): Supported <br>[Nested Virtualization](/virtualization/hyper-v-on-windows/user-guide/nested-virtualization): Supported <br>

## Sizes in series

### [Basics](#tab/sizebasic)

vCPUs (Qty.) and Memory for each size

| Size Name | vCPUs (Qty.) | Memory (GB) |
| --- | --- | --- |
| Standard_E2ads_v5 | 2 | 16 |
| Standard_E4ads_v5 | 4 | 32 |
| Standard_E8ads_v5 | 8 | 64 |
| Standard_E16ads_v5 | 16 | 128 |
| Standard_E20ads_v5 | 20 | 160 |
| Standard_E32ads_v5 | 32 | 256 |
| Standard_E48ads_v5 | 48 | 384 |
| Standard_E64ads_v5 | 64 | 512 |
| Standard_E96ads_v5 | 96 | 672 |
| Standard_E112iads_v5 | 112 | 672 |

#### VM Basics resources
- [Check vCPU quotas](../../../virtual-machines/quotas.md)

### [Local storage](#tab/sizestoragelocal)

Local (temp) storage info for each size

| Size Name | Max Temp Storage Disks (Qty.) | Temp Disk Size (GiB) | Temp Disk Random Read (RR)<sup>1</sup> IOPS | Temp Disk Random Read (RR)<sup>1</sup> Speed (MBps) | Temp Disk Random Write (RW)<sup>1</sup> IOPS | Temp Disk Random Write (RW)<sup>1</sup> Speed (MBps) | Local-Special-Disk-Count | Local-Special-Disk-Size-GB | Local-Special-Disk-RR-IOPS | Local-Special-Disk-RR-MBps |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Standard_E2ads_v5 | 1 | 75 | 9000 | 125 |  |  |  |  |  |  |
| Standard_E4ads_v5 | 1 | 150 | 19000 | 250 |  |  |  |  |  |  |
| Standard_E8ads_v5 | 1 | 300 | 38000 | 500 |  |  |  |  |  |  |
| Standard_E16ads_v5 | 1 | 600 | 75000 | 1000 |  |  |  |  |  |  |
| Standard_E20ads_v5 | 1 | 750 | 94000 | 1250 |  |  |  |  |  |  |
| Standard_E32ads_v5 | 1 | 1200 | 150000 | 2000 |  |  |  |  |  |  |
| Standard_E48ads_v5 | 1 | 1800 | 225000 | 3000 |  |  |  |  |  |  |
| Standard_E64ads_v5 | 1 | 2400 | 300000 | 4000 |  |  |  |  |  |  |
| Standard_E96ads_v5 | 1 | 3600 | 450000 | 4000 |  |  |  |  |  |  |
| Standard_E112iads_v5 | 1 | 3800 | 450000 | 4000 |  |  |  |  |  |  |

#### Storage resources
- [Introduction to Azure managed disks](../../../virtual-machines/managed-disks-overview.md)
- [Azure managed disk types](../../../virtual-machines/disks-types.md)
- [Share an Azure managed disk](../../../virtual-machines/disks-shared.md)

#### Table definitions
- <sup>1</sup>Temp disk speed often differs between RR (Random Read) and RW (Random Write) operations. RR operations are typically faster than RW operations. The RW speed is usually slower than the RR speed on series where only the RR speed value is listed.
- Storage capacity is shown in units of GiB or 1024^3 bytes. When you compare disks measured in GB (1000^3 bytes) to disks measured in GiB (1024^3) remember that capacity numbers given in GiB may appear smaller. For example, 1023 GiB = 1098.4 GB.
- Disk throughput is measured in input/output operations per second (IOPS) and MBps where MBps = 10^6 bytes/sec.
- To learn how to get the best storage performance for your VMs, see [Virtual machine and disk performance](../../../virtual-machines/disks-performance.md).

### [Remote storage](#tab/sizestorageremote)

Remote (uncached) storage info for each size

| Size Name | Max Remote Storage Disks (Qty.) | Uncached Disk IOPS | Uncached Disk Speed (MBps) | Uncached Disk Burst<sup>1</sup> IOPS | Uncached Disk Burst<sup>1</sup> Speed (MBps) | Uncached Special<sup>2</sup> Disk IOPS | Uncached Special<sup>2</sup> Disk Speed (MBps) | Uncached Burst<sup>1</sup> Special<sup>2</sup> Disk IOPS | Uncached Burst<sup>1</sup> Special<sup>2</sup> Disk Speed (MBps) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Standard_E2ads_v5 | 4 | 3750 | 82 | 10000 | 600 |  |  |  |  |
| Standard_E4ads_v5 | 8 | 6400 | 144 | 20000 | 600 |  |  |  |  |
| Standard_E8ads_v5 | 16 | 12800 | 200 | 20000 | 600 |  |  |  |  |
| Standard_E16ads_v5 | 32 | 25600 | 384 | 40000 | 800 |  |  |  |  |
| Standard_E20ads_v5 | 32 | 32000 | 480 | 64000 | 1000 |  |  |  |  |
| Standard_E32ads_v5 | 32 | 51200 | 768 | 80000 | 1600 |  |  |  |  |
| Standard_E48ads_v5 | 32 | 76800 | 1152 | 80000 | 2000 |  |  |  |  |
| Standard_E64ads_v5 | 32 | 80000 | 1200 | 80000 | 2000 |  |  |  |  |
| Standard_E96ads_v5 | 32 | 80000 | 1600 | 80000 | 2000 |  |  |  |  |
| Standard_E112iads_v5 | 64 | 120000 | 2000 | 120000 | 2000 |  |  |  |  |

#### Storage resources
- [Introduction to Azure managed disks](../../../virtual-machines/managed-disks-overview.md)
- [Azure managed disk types](../../../virtual-machines/disks-types.md)
- [Share an Azure managed disk](../../../virtual-machines/disks-shared.md)

#### Table definitions
- <sup>1</sup>Some sizes support [bursting](../../disk-bursting.md) to temporarily increase disk performance. Burst speeds can be maintained for up to 30 minutes at a time.
- <sup>2</sup>Special Storage refers to either [Ultra Disk](../../../virtual-machines/disks-enable-ultra-ssd.md) or [Premium SSD v2](../../../virtual-machines/disks-deploy-premium-v2.md) storage.
- Storage capacity is shown in units of GiB or 1024^3 bytes. When you compare disks measured in GB (1000^3 bytes) to disks measured in GiB (1024^3) remember that capacity numbers given in GiB may appear smaller. For example, 1023 GiB = 1098.4 GB.
- Disk throughput is measured in input/output operations per second (IOPS) and MBps where MBps = 10^6 bytes/sec.
- Data disks can operate in cached or uncached modes. For cached data disk operation, the host cache mode is set to ReadOnly or ReadWrite. For uncached data disk operation, the host cache mode is set to None.
- To learn how to get the best storage performance for your VMs, see [Virtual machine and disk performance](../../../virtual-machines/disks-performance.md).


### [Network](#tab/sizenetwork)

Network interface info for each size

| Size Name | Max NICs (Qty.) | Max Bandwidth (Mbps) |
| --- | --- | --- |
| Standard_E2ads_v5 | 2 | 12500 |
| Standard_E4ads_v5 | 2 | 12500 |
| Standard_E8ads_v5 | 4 | 12500 |
| Standard_E16ads_v5 | 8 | 12500 |
| Standard_E20ads_v5 | 8 | 12500 |
| Standard_E32ads_v5 | 8 | 16000 |
| Standard_E48ads_v5 | 8 | 24000 |
| Standard_E64ads_v5 | 8 | 32000 |
| Standard_E96ads_v5 | 8 | 40000 |
| Standard_E112iads_v5 | 8 | 50000 |

#### Networking resources
- [Virtual networks and virtual machines in Azure](/azure/virtual-network/network-overview)
- [Virtual machine network bandwidth](/azure/virtual-network/virtual-machine-network-throughput)

#### Table definitions
- Expected network bandwidth is the maximum aggregated bandwidth allocated per VM type across all NICs, for all destinations. For more information, see [Virtual machine network bandwidth](/azure/virtual-network/virtual-machine-network-throughput)
- Upper limits aren't guaranteed. Limits offer guidance for selecting the right VM type for the intended application. Actual network performance will depend on several factors including network congestion, application loads, and network settings. For information on optimizing network throughput, see [Optimize network throughput for Azure virtual machines](/azure/virtual-network/virtual-network-optimize-network-bandwidth). 
-  To achieve the expected network performance on Linux or Windows, you may need to select a specific version or optimize your VM. For more information, see [Bandwidth/Throughput testing (NTTTCP)](/azure/virtual-network/virtual-network-bandwidth-testing).

### [Accelerators](#tab/sizeaccelerators)

Accelerator (GPUs, FPGAs, etc.) info for each size

> [!NOTE]
> No accelerators are present in this series.

---

[!INCLUDE [sizes-footer](../includes/sizes-footer.md)]