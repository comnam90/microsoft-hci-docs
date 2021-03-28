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

| Feature                                    | WS2016             | WS2019             | WS2022             | AzSHCI 20H2        |
| ------------------------------------------ | ------------------ | ------------------ | ------------------ | ------------------ |
| [2-way Mirror Volumes][S2D-1]              | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| [3-way Mirror Volumes][S2D-2]              | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| [Single Parity Volumes][S2D-3]             | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| [Dual Parity Volumes][S2D-4]               | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| [Mirror-Accelerated Parity Volumes][S2D-5] | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| Nested Resiliency Volumes                  | :x:                | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| Maximum Volume Size                        | 32TB               | 64TB               | ?                  | 64TB               |
| ReFS Deduplication                         | :x:                | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| SCM Support                                | :x:                | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| Delimited Volumes                          | :x:                | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| Automatic Storage Maintenance Mode         | :x:                | :x:                | :white_check_mark: | :x:                |
| Thin provisioned Volumes                   | :x:                | :x:                | :white_check_mark: | :x:                |
| Configurable Rebuild Priority              | :x:                | :x:                | :white_check_mark: | :x:                |
| Stretch Cluster                            | :x:                | :x:                | :x:                | :white_check_mark: |
| Sub-extent rebuilds                        | :x:                | :x:                | :white_check_mark: | :white_check_mark: |
| Bitlocker Encryption                       | :x:                | :x:                | :white_check_mark: | :white_check_mark: |
| Converged Deployment                       | :white_check_mark: | :white_check_mark: | :white_check_mark: | :x:                |
| Hyper-Converged Deployment                 | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| Maximum RAW Capacity per Server            | 100TB              | 400TB              | ?                  | [400TB][S2D-6]     |
| Maximum RAW Capacity per Pool              | 1PB                | 4PB                | ?                  | [4PB][S2D-6]       |
| Maximum Volumes                            | 32                 | 64                 | ?                  | 64                 |

[S2D-1]: https://docs.microsoft.com/en-nz/azure-stack/hci/concepts/fault-tolerance#two-way-mirror
[S2D-2]: https://docs.microsoft.com/en-nz/azure-stack/hci/concepts/fault-tolerance#three-way-mirror
[S2D-3]: https://docs.microsoft.com/en-nz/azure-stack/hci/concepts/fault-tolerance#single-parity
[S2D-4]: https://docs.microsoft.com/en-nz/azure-stack/hci/concepts/fault-tolerance#dual-parity
[S2D-5]: https://docs.microsoft.com/en-nz/azure-stack/hci/concepts/fault-tolerance#mirror-accelerated-parity
[S2D-6]: https://docs.microsoft.com/en-nz/azure-stack/hci/concepts/choose-drives#general

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

| Feature                     | WS2016 | WS2019 | WS2022             | AzSHCI 20H2        |
| --------------------------- | ------ | ------ | ------------------ | ------------------ |
| CSV Cache Default Size      | 0      | 1GB    | 1GB                | 1GB                |
| Affinity/Anti-affinity Rule | :x:    | :x:    | :white_check_mark: | :white_check_mark: |

## Software Defined Networking Features
