## Contents

- [ ] TODO Intro to EAM/PM

As of 2022 there are only minor differences between ECC and S/4 HANA in the PM module.
SAP documentation for summary of [S/4 HANA Plant Maintenance](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/e72f747389b340229f7fa343975bfa57/b97cb6535fe6b74ce10000000a174cb4.html?locale=en-US&q=Plant%20Maintenance)

SAP documentation for [Technical Objects](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/e98c7c41bbe8439e90daa5c114a7573b/59bdb853dcfcb44ce10000000a174cb4.html?locale=en-US)

|     |  Topic       |      Master Data       |         Transactional          |             Description  |
| :-- | :--------------- | :----------------: | :------------------: |  :-------------------------------- |
|  | **PM / EAM**        |  | | Plant Maintenance, Asset Management. |
| &#127970; | [Organisation](pm_org_levels.md) &check;  | &check; |    |Organisational levels, Plant. |
| &#128119; | [Work Center](pm_work_center.md)  &check;   | &check; |    | Work Centers are functional and logistical groups that perform the work. |
|  | **Technical Objects** | &check; |    |  |
|&#127981;  | [Functional Location](pm_func_loc.md) &check;| &check; |    | FLocs based on Purpose, Technology, location/region |
| &#128297; | [Equipment](pm_equip.md) &check;            | &check; |    | Equipment. |
| &#128195;| [Bills of Material](pm_bom.md) &check;            | &check; |    | Structures of FLocs and Equipment. |
|  | **Maintenance Processing Objects** | &check; |    |  |
| &#128203; | [Notification](pm_noti.md)  &check;   |  |  &check;  | Notification.  |
| &#128197;| [Maintenance Order](pm_order.md)     |  |  &check;  | Work Order.  |
| &#128295; | [Operation](pm_order.md) &check;    |  |  &check;  | WO Operation.  |
| &#127988; | [Status](pm_status.md)       |  |  &check;  | System and User Status model used by many PM objects.  |
| &#128205; |Measurement Point |  |    |  |
| &#128207; |Measurement Document |  |    |  |
|  | **Maintenance Processing** | &check; |    |  |
| &#128203; | [Noti-Order](pm_proc_std.md)  &check;   |  |  &check;  | Standard Process.  |
| &#128197;| [Maintenance Order](pm_order.md)     |  |  &check;  | Work Order.  |
| &#128295; | [Operation](pm_order.md) &check;    |  |  &check;  | WO |
|  | **Other Processes** |  |    |  |
|  | **Other Processes** |  |    |  |

:white_check_mark: Complete  ✅
&check; In progress  🗸 ✓
✗ ❎
&#128178;	
&#127970;
	
&#9873;	
&#127937;
&#127987;	
&#127988;

&#128207;
&#128208;

![Alt text here](pm_example.svg)

https://app.diagrams.net/?mode=github#Hqurm%2Fsap-diagrams%2Fmain%2FERP%2FPM%2Fpm_example.svg
