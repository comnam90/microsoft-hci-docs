# Feature Comparison

Microsoft introduced their Hyperconverged Infrastructure (HCI) stack in Windows Server 2016,
 and has since improved on it in Windows Server 2019/2022, even released a dedicated operating
 system for it called Azure Stack HCI (AzSHCI).

## Storage Spaces Direct Features

| Feature                            | WS2016             | WS2019             | WS2022             | AzSHCI 20H2        |
| ---------------------------------- | ------------------ | ------------------ | ------------------ | ------------------ |
| 2-way Mirror Volumes               | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| 3-way Mirror Volumes               | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| Single Parity Volumes              | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| Dual Parity Volumes                | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| Mirror-Accelerated Parity Volumes  | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| ReFS Deduplication                 | :x:                | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| Nested Resiliency                  | :x:                | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| SCM Support                        | :x:                | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| Automatic Storage Maintenance Mode | :x:                | :x:                | :white_check_mark: | :x:                |
| Stretch Cluster                    | :x:                | :x:                | :x:                | :white_check_mark: |

## Hyper-V Features

### VM Configuration Support

| Version | WS2016 | WS2019 | WS2022 | AzSHCI 20H2 |
| ------- | ------ | ------ | ------ | ----------- |
| 5.0     | Yes    | Yes    | No     | Yes         |
| 6.2     | Yes    | Yes    | No     | Yes         |
| 7.0     | Yes    | Yes    | No     | Yes         |
| 7.1     | Yes    | Yes    | No     | Yes         |
| 8.0     | Yes    | Yes    | Yes    | Yes         |
| 8.1     | No     | Yes    | Yes    | Yes         |
| 8.2     | No     | Yes    | Yes    | Yes         |
| 8.3     | No     | Yes    | Yes    | Yes         |
| 9.0     | No     | Yes    | Yes    | Yes         |
| 9.1     | No     | No     | Yes    | No          |
| 9.2     | No     | No     | Yes    | No          |
| 9.3     | No     | No     | Yes    | No          |
| 10.0    | No     | No     | Yes    | No          |

## Failover Clustering Features

## Software Defined Networking Features
