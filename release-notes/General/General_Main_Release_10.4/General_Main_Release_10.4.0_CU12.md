---
uid: General_Main_Release_10.4.0_CU12
---

# General Main Release 10.4.0 CU12 - Preview

> [!IMPORTANT]
> We are still working on this release. Some release notes may still be modified or moved to a later release. Check back soon for updates!

> [!TIP]
>
> - For release notes related to DataMiner Cube, see [DataMiner Cube Main Release 10.4.0 CU12](xref:Cube_Main_Release_10.4.0_CU12).
> - For release notes related to the DataMiner web applications, see [DataMiner web apps Main Release 10.4.0 CU12](xref:Web_apps_Main_Release_10.4.0_CU12).
> - For information on how to upgrade DataMiner, see [Upgrading a DataMiner Agent](xref:Upgrading_a_DataMiner_Agent).

### Enhancements

#### SLLogCollector packages now also contain the ClusterEndpoints.json file [ID 41887]

<!-- MR 10.4.0 [CU12] - FR 10.5.3 -->

SLLogCollector packages now also include the *ClusterEndpoints.json* file.

### Fixes

#### Missing DATAMINER_NOTIFICATION_QUEUE thread [ID 41699]

<!-- MR 10.4.0 [CU12] - FR 10.5.3 -->

When DataMiner was restarted, an issue could occur, causing the DATAMINER_NOTIFICATION_QUEUE thread not to be registered in processes like SLDMS, SLElement or SLDataGateway. These missing threads could then lead to a number of symptoms like empty element data cards or not being able to swarm back elements.

#### Problem with incorrect virtual element states [ID 41705]

<!-- MR 10.4.0 [CU12] - FR 10.5.3 -->

In some rare cases, the element state of a DVE or Virtual Function element would end up incorrect in the SLNet cache, causing some caches to not be initialized correctly.

#### Service & Resource Management: Problem when a previously deleted booking was created again [ID 41718]

<!-- MR 10.4.0 [CU12] - FR 10.5.3 -->

When a previously deleted booking was created again with the same ID, up to now, that booking would incorrectly not be retrieved.

#### Uploading the same version of a DVE connector twice would incorrectly cause the production version of DVE child elements to be changed [ID 41798]

<!-- MR 10.4.0 [CU12] - FR 10.5.3 -->

When the same version of a DVE connector was uploaded twice, the production version of all DVE child elements using another version of that connector as production version would incorrectly have their production version set to the newly uploaded version.

#### SNMP managers would incorrectly receive some or all active alarms at DMA start-up [ID 41878]

<!-- MR 10.4.0 [CU12] - FR 10.5.3 -->

When a DataMiner Agent was started, in some cases, the configured SNMP managers would incorrectly receive some or all active alarms.

#### Alarms without focus value would not be correctly removed from alarm groups when the associated element was deleted, stopped or paused [ID 41950]

<!-- MR 10.4.0 [CU12] - FR 10.5.3 -->

In some cases, alarm groups containing alarms without a focus value (e.g. notices or errors) would not be correctly removed from the group when the element associated with the alarm was deleted, stopped or paused.
