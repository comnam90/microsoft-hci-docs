# Feature Comparison

Microsoft introduced their Hyperconverged Infrastructure (HCI) stack in Windows Server 2016,
 and has since improved on it in Windows Server 2019/2022, even released a dedicated operating
 system for it called Azure Stack HCI (AzSHCI).

- [Feature Comparison](#feature-comparison)
  - [Storage Spaces Direct Features](#storage-spaces-direct-features)
  - [Hyper-V Features](#hyper-v-features)
    - [VM Configuration Support](#vm-configuration-support)
  - [Failover Clustering Features](#failover-clustering-features)
  - [Software Defined Networking Features](#software-defined-networking-features)

## Storage Spaces Direct Features

| Feature                                          | WS2016             | WS2019             | WS2022             | AzSHCI 20H2        |
| ------------------------------------------------ | ------------------ | ------------------ | ------------------ | ------------------ |
| [2-way Mirror Volumes][S2D-1]                    | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| [3-way Mirror Volumes][S2D-2]                    | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| [Single Parity Volumes][S2D-3]                   | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| [Dual Parity Volumes][S2D-4]                     | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| [Mirror-Accelerated Parity Volumes][S2D-5]       | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| [Nested Resiliency Volumes][S2D-7]               | :x:                | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| Maximum Volume Size                              | [32TB][S2D-13]     | [64TB][S2D-13]     | ?                  | 64TB               |
| [ReFS Deduplication][S2D-9]                      | :x:                | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| [SCM Support][S2D-10]                            | :x:                | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| [Delimited Volumes][S2D-8]                       | :x:                | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| Automatic Storage Maintenance Mode               | :x:                | :x:                | :white_check_mark: | :x:                |
| Thin provisioned Volumes                         | :x:                | :x:                | :white_check_mark: | :x:                |
| [Configurable Rebuild Priority][S2D-16]          | :x:                | :x:                | :white_check_mark: | :x:                |
| [Stretched Clusters][S2D-11]                     | :x:                | :x:                | :x:                | :white_check_mark: |
| [Sub-extent rebuilds][S2D-16]                    | :x:                | :x:                | :white_check_mark: | :white_check_mark: |
| [Bitlocker Encryption][S2D-12]                   | :x:                | :x:                | :white_check_mark: | :white_check_mark: |
| [Converged Deployment][deployment-options]       | :white_check_mark: | :white_check_mark: | :white_check_mark: | :x:                |
| [Hyper-Converged Deployment][deployment-options] | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| Maximum RAW Capacity per Server                  | [100TB][S2D-15]    | [400TB][S2D-15]    | [1.6PB][S2D-16]    | [400TB][S2D-6]     |
| Maximum RAW Capacity per Pool                    | [1PB][S2D-15]      | [4PB][S2D-15]      | [16PB][S2D-16]     | [4PB][S2D-6]       |
| Maximum Volumes                                  | [32][S2D-14]       | [64][S2D-14]       | ?                  | 64                 |

[S2D-1]: https://docs.microsoft.com/en-nz/azure-stack/hci/concepts/fault-tolerance#two-way-mirror
[S2D-2]: https://docs.microsoft.com/en-nz/azure-stack/hci/concepts/fault-tolerance#three-way-mirror
[S2D-3]: https://docs.microsoft.com/en-nz/azure-stack/hci/concepts/fault-tolerance#single-parity
[S2D-4]: https://docs.microsoft.com/en-nz/azure-stack/hci/concepts/fault-tolerance#dual-parity
[S2D-5]: https://docs.microsoft.com/en-nz/azure-stack/hci/concepts/fault-tolerance#mirror-accelerated-parity
[S2D-6]: https://docs.microsoft.com/en-nz/azure-stack/hci/concepts/choose-drives#general
[S2D-7]: https://docs.microsoft.com/en-us/windows-server/storage/storage-spaces/nested-resiliency
[S2D-8]: https://docs.microsoft.com/en-us/windows-server/storage/storage-spaces/delimit-volume-allocation
[S2D-9]: https://docs.microsoft.com/en-us/windows-server/storage/data-deduplication/whats-new
[S2D-10]: https://docs.microsoft.com/en-us/windows-server/storage/storage-spaces/deploy-pmem
[S2D-11]: https://docs.microsoft.com/en-nz/azure-stack/hci/concepts/stretched-clusters
[S2D-12]: https://docs.microsoft.com/en-us/azure-stack/hci/manage/volume-encryption-deduplication#turn-on-bitlocker-to-protect-volumes
[deployment-options]: https://docs.microsoft.com/en-us/windows-server/storage/storage-spaces/storage-spaces-direct-overview#deployment-options
[S2D-13]: https://docs.microsoft.com/en-us/windows-server/storage/storage-spaces/plan-volumes#choosing-the-size-of-volumes
[S2D-14]: https://docs.microsoft.com/en-us/windows-server/storage/storage-spaces/plan-volumes#choosing-how-many-volumes-to-create
[S2D-15]: https://docs.microsoft.com/en-us/windows-server/storage/storage-spaces/storage-spaces-direct-hardware-requirements#maximum-capacity
[S2D-16]: https://techcommunity.microsoft.com/t5/failover-clustering/talking-failover-clustering-and-azure-stack-hci-ignite-2019/ba-p/1015497

## Hyper-V Features

### VM Configuration Support

| Version | WS2016             | WS2019             | WS2022             | AzSHCI 20H2        |
| ------- | ------------------ | ------------------ | ------------------ | ------------------ |
| 5.0     | :white_check_mark: | :white_check_mark: | :x:                | :white_check_mark: |
| 6.2     | :white_check_mark: | :white_check_mark: | :x:                | :white_check_mark: |
| 7.0     | :white_check_mark: | :white_check_mark: | :x:                | :white_check_mark: |
| 7.1     | :white_check_mark: | :white_check_mark: | :x:                | :white_check_mark: |
| 8.0     | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| 8.1     | :x:                | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| 8.2     | :x:                | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| 8.3     | :x:                | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| 9.0     | :x:                | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| 9.1     | :x:                | :x:                | :white_check_mark: | :x:                |
| 9.2     | :x:                | :x:                | :white_check_mark: | :x:                |
| 9.3     | :x:                | :x:                | :white_check_mark: | :x:                |
| 10.0    | :x:                | :x:                | :white_check_mark: | :x:                |

## Failover Clustering Features

| Feature                             | WS2016 | WS2019 | WS2022             | AzSHCI 20H2        |
| ----------------------------------- | ------ | ------ | ------------------ | ------------------ |
| CSV Cache Default Size              | 0      | 1GB    | 1GB                | 1GB                |
| [Affinity/Anti-affinity Rule][FC-1] | :x:    | :x:    | :white_check_mark: | :white_check_mark: |

[FC-1]: https://docs.microsoft.com/en-nz/azure-stack/hci/manage/vm-affinity

## Software Defined Networking Features
