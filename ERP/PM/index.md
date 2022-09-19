## Contents

- [ ] TODO Intro to EAM/PM

As of 2022 there are only minor differences between ECC and S/4 HANA in teh PM module.
SAP documentation for summary of [S/4 HANA Plant Maintenance](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/e72f747389b340229f7fa343975bfa57/b97cb6535fe6b74ce10000000a174cb4.html?locale=en-US&q=Plant%20Maintenance)

SAP documentation for [Technical Objects](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/e98c7c41bbe8439e90daa5c114a7573b/59bdb853dcfcb44ce10000000a174cb4.html?locale=en-US)

|                  |      Master Data       |         Transactional          |             Description            |
| :--------------- | :----------------: | :------------------: |  :-------------------------------- |
| **PM / EAM**        |  | | Plant Maintenance, Asset Management. |
| [Organisation](pm_org_levels.md) &check;  | &check; |    |Organisational levels, Plant. |
| [Work Center](pm_work_center.md)  &check;   | &check; |    | Work Centers are functional and logistical groups that perform the work. |
| **Technical Objects** | &check; |    |  |
| [Functional Location](pm_func_loc.md) &check;| &check; |    | FLOCs. |
| [Equipment](pm_equip.md) &check;            | &check; |    | Equipment. |
| [Bills of Material] (pm_bom.md) &check;            | &check; |    | Structures of FLocs and Equipment. |
| **Maintenance Processing** | &check; |    |  |
| [Notification](pm_noti.md)  &check;   |  |  &check;  | Notification.  |
| [Maintenance Order](pm_order.md)     |  |  &check;  | Work Order.  |
| [Operation](pm_order.md) &check;    |  |  &check;  | WO Operation.  |
| [Status](pm_status.md)       |  |  &check;  | System and User Status model used by many PM objects.  |
| **Other Processes** |  |    |  |

:white_check_mark: Complete
&check; In progress