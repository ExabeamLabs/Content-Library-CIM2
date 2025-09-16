# Content Package 2025.19.1

These release notes contain information about content package 2025.19.1, released on 11 Sep 2025.


## Enhancements
- Updated service_state field extractions for parsers with event code - 7036 and 7040.
- Updated Product for parser microsoft-wdac-str-endpoint-notification-success-3033 from Windows Defender Application Control to Event Viewer - CodeIntegrity
- Added new parser for  Proofpoint CASB Data Leakage logs.
- Added new field 'ioc' for parser infoblox-bddi-json-dns-query-success-response
- Added new parser tenable-t-json-endpoint-scan-scaninformation to support for new format Tenable logs.
- Updated activity type from endpoint-notification:success to dll-load:fail in parsers microsoft-wdac-xml-endpoint-notification-success-3033 & microsoft-wdac-str-endpoint-notification-success-3033
- Updated conditions for parser fireeye-networksecurity-json-http-session-success-http to cater to a broader set of Trellix Network Security (NX) logs.
- Updated cisco-ise-str-app-notification-alarm parser condition to support cisco unparsed logs .
- Updated product for parser microsoft-wdac-str-endpoint-notification-success-3033 from Windows Defender Application Control to Event Viewer - CodeIntegrity . Additionaly updated the event builders for parser microsoft-wdac-str-endpoint-notification-success-3033 & {{microsoft-wdac-xml-endpoint-notification-success-3033}}to create dll-load:fail events.
- Added parser akamai-guardicore-cef-alert-trigger-success-revealincident and updated akamai-guardicore-cef-app-activity-userauth
- updated the parser salesforce-sf-json-app-activity-success-loginhistory to match the broader category of Salesforce logs Added new fields as per the new logs. Added new eventbuilders for the parser salesforce-sf-json-app-activity-success-loginhistory
- Added new parser for humansecurity logs - humansecurity-botdefender-json-app-activity-botdefender parser .
- Updated the parser condition for OOTB parser thoughtspot-ts-json-app-activity-success-type to parse unparsed ThoughtSpot logs properly
- Updated file_type, group, action field extractions for parser template: Microsoft-CAS-Event-Category
- Updated file_type, group, action field extractions for parser template: Microsoft-CAS-Event-Category
- Added new parser for KnowBe4 logs - knowbe4-sat-json-app-activity-success-kmsat.
- Updated file_type, group, action field extractions for parser template: Microsoft-CAS-Event-Category
- Updated windows parsers to parse out all user values including considering system account.
- Added new parser apache-a-str-http-session-apacheaccess to support unparsed apache logs.
- Added new parsers - postgresql-p-str-database-activity-context,postgresql-p-str-database-activity-fatal,postgresql-p-str-database-activity-log,postgresql-p-str-database-activity-detail,postgresql-p-str-database-login-fail-password-doesnotmatch and updated parser - postgresql-p-str-database-login-fail-role-doesnt_exist to parse PostgreSQL logs.
- Updated parser:f5-asm-cef-alert-trigger-success-cookie conditions to parse broader category of F5 ASM logs Added new fields as per new logs Added a new parser for bot defense logs of F5 ASM
- Created parser for Google Agentspace logs
- Added new parsers for Ordr SCE.
- We re-added two parsers with VendorMatch=True, which had been removed earlier due to conflicts with Barracuda. microsoft-iis-str-http-session-getapi microsoft-iis-str-http-session-postapi
- Added new parser for F5 Big-IP TMM logs.
- Change subject and activity_type from peripheral_storage to peripheral_device
- added new parser 'f5-lbr-str-ssl-error'
- Added new parser for GitLab logs - gitlab-gl-json-app-activity-success-entity.
- Removed a deprecated template - dl-wazuh-windows-template and updated JSON regexes in template - microsoft-json-events.
- updated result field extractions for parser airlock-allowlisting-json-app-activity-success-task
- Fixed the regexes which were causing slow regex issue that resulted into large number of unparsed amazon logs.

## Addressed Issues
- Added support for JSON regex in parser - microsoft-o365-sk4-app-file-operationworkload. It is now a hybrid parser that supports both plain and JSON regex.
- Added method, url, user_agent, src_ip, dest_ip, http_response_code, additional_info, project_id, result and log_name fields for google-gcpca-sk4-app-activity-cloud parser .
- Updated src_ip field for vectra-cd-json-alert-trigger-success-detection-1 parser.
- Updated instance_profile_arn, alert_id field extractions for parser: amazon-awsguardduty-cef-alert-trigger-success-catsecurity
- Updated SequenceExpiryTime to five minutes in VariableMessageMultiEventTracker to merge logs for parser - f5-apm-str-vpn-success-01490005.
- Updated user_agent, dest_email_domain, src_ip and tenant_id field extractions for parser - azure-azuread-json-app-activity-useractivitydisplayname
- Updated alert_reason, alert_subject, severity field extractions for parser: okta-amfa-mix-app-login-success-securitycontext
- Updated rule field extraction for parser - pan-ngfw-json-alert-trigger-success-threat.
- Added user_agent field in microsoft-azuredevops-json-app-activity-success-devopsaudit parser.
- Added action field extraction for parsers - checkpoint-es-cef-alert-trigger-success-checkpoint and checkpoint-am-cef-alert-trigger-success-checkpointantimalware.
- Fixed threat_url, src_mac, connection_id and sensor field issues with vectra-cd-json-alert-trigger-success-detection parser.
- Updated the regex for 'Process Name' field for below parsers microsoft-evsecurity-kv-file-permission-modify-4670 microsoft-evsecurity-kv-group-list-membershipenumerated microsoft-evsecurity-kv-group-member-list-4799 Updated 'Process ID' field for the parser microsoft-evsecurity-kv-group-member-list-4799
- Fixed event types for parser cisco-mma-json-network-traffic-success-addressingvlans,cisco-netsec-json-network-traffic-success-categorytype
- Updated Regex for the 'user' field mapping for below parsers microsoft-evsecurity-kv-process-create-success-created-1 microsoft-evsecurity-kv-endpoint-login-fail-4625-2 microsoft-evsecurity-kv-handle-request-4656-2 microsoft-evsecurity-kv-user-privilege-use-success-4674-1 microsoft-evsecurity-mix-share-access-success-5140-1
- Added 'user' field for Auth0 parsers
- Updated parser - pan-gp-csv-vpn-login-useridlogin to create only success event.
- Updated user & account field extractions for Windows eventID 4740 parsers: microsoft-evsecurity-xml-user-lock-success-4740-1, microsoft-evsecurity-json-user-lock-success-4740
- Fixed the regexes which were causing slow regex issue for Amazon parsers.

## Code Changes
### ℹ️ How to Read This Document

Each item listed under **Code Changes** includes:

- **A link to a detailed change file**  
  Click the filename (e.g., `Carbon Black.md`) to open a full table showing what changed.

- **A search icon 🔍**  
  Click the 🔍 icon to search for this resource in the [Exabeam Content Library](https://github.com/ExabeamLabs/Content-Library-CIM2).


<details>
<summary><strong id="event-builder">Event Builder (105)</strong></summary>


### Change Types
- [Added Event Builder](#added-event-builder)
- [Edit Conditions](#edit-conditions)
- [Removed Event Builder](#removed-event-builder)

#### Added Event Builder
<a id="added-event-builder"></a>
- [akamai-guardicore-alert-trigger-success](CodeChanges/akamai-guardicore-alert-trigger-success.md)
- [assetview-windows-peripheral_device-insert-success](CodeChanges/assetview-windows-peripheral_device-insert-success.md)
- [code42-incydr-peripheral_device-activity-success](CodeChanges/code42-incydr-peripheral_device-activity-success.md)
- [crowdstrike-falcon-peripheral-device-insert-success](CodeChanges/crowdstrike-falcon-peripheral-device-insert-success.md)
- [crowdstrike-falcon-peripheral-device-insert-success-lin](CodeChanges/crowdstrike-falcon-peripheral-device-insert-success-lin.md)
- [crowdstrike-falcon-peripheral-device-insert-success-win](CodeChanges/crowdstrike-falcon-peripheral-device-insert-success-win.md)
- [crowdstrike-macos-peripheral-device-activity-success](CodeChanges/crowdstrike-macos-peripheral-device-activity-success.md)
- [crowdstrike-unix-peripheral-device-activity-success](CodeChanges/crowdstrike-unix-peripheral-device-activity-success.md)
- [crowdstrike-windows-peripheral-device-activity-success](CodeChanges/crowdstrike-windows-peripheral-device-activity-success.md)
- [dl-akamai-guardicore-app-activity-success](CodeChanges/dl-akamai-guardicore-app-activity-success.md)
- [dl-akamai-guardicore-app-activity-success-1](CodeChanges/dl-akamai-guardicore-app-activity-success-1.md)
- [dl-cisco-meraki-configuration-modify-success](CodeChanges/dl-cisco-meraki-configuration-modify-success.md)
- [dl-cisco-meraki-network-alert-success](CodeChanges/dl-cisco-meraki-network-alert-success.md)
- [dl-crowdstrike-falcon-peripheral-device-activity-success](CodeChanges/dl-crowdstrike-falcon-peripheral-device-activity-success.md)
- [dl-crowdstrike-falcon-peripheral-device-activity-success-1](CodeChanges/dl-crowdstrike-falcon-peripheral-device-activity-success-1.md)
- [dl-crowdstrike-falcon-peripheral-device-activity-success-2](CodeChanges/dl-crowdstrike-falcon-peripheral-device-activity-success-2.md)
- [dl-crowdstrike-falcon-peripheral-device-activity-success-lin](CodeChanges/dl-crowdstrike-falcon-peripheral-device-activity-success-lin.md)
- [dl-crowdstrike-falcon-peripheral-device-activity-success-win](CodeChanges/dl-crowdstrike-falcon-peripheral-device-activity-success-win.md)
- [dl-crowdstrike-falcon-peripheral-device-insert-success](CodeChanges/dl-crowdstrike-falcon-peripheral-device-insert-success.md)
- [dl-f5-asm-csv-network-traffic-success-passed](CodeChanges/dl-f5-asm-csv-network-traffic-success-passed.md)
- [dl-f5-bigip-network-notification-success](CodeChanges/dl-f5-bigip-network-notification-success.md)
- [dl-f5-lbr-app-notification-success](CodeChanges/dl-f5-lbr-app-notification-success.md)
- [dl-google-agentspace-json-app-activity-success](CodeChanges/dl-google-agentspace-json-app-activity-success.md)
- [dl-microsoft-windows-app-activity-success-2](CodeChanges/dl-microsoft-windows-app-activity-success-2.md)
- [dl-microsoft-windows-dll-load-fail](CodeChanges/dl-microsoft-windows-dll-load-fail.md)
- [dl-microsoft-windows-peripheral-device-remove-success](CodeChanges/dl-microsoft-windows-peripheral-device-remove-success.md)
- [dl-ordr-network-alert-trigger-success](CodeChanges/dl-ordr-network-alert-trigger-success.md)
- [dl-postgresql-database-activity-success](CodeChanges/dl-postgresql-database-activity-success.md)
- [dl-proofpoint-casb-alert-trigger-success](CodeChanges/dl-proofpoint-casb-alert-trigger-success.md)
- [dl-salesforce-app-logout-success](CodeChanges/dl-salesforce-app-logout-success.md)
- [dl-tenable-io-endpoint-scan-success](CodeChanges/dl-tenable-io-endpoint-scan-success.md)
- [dl-thoughtspot-ts-app-logout-success](CodeChanges/dl-thoughtspot-ts-app-logout-success.md)
- [dl-thoughtspot-ts-group-create-success](CodeChanges/dl-thoughtspot-ts-group-create-success.md)
- [f5-asm-alert-trigger-success-3](CodeChanges/f5-asm-alert-trigger-success-3.md)
- [f5-lbr-certificate-expire-success](CodeChanges/f5-lbr-certificate-expire-success.md)
- [f5-lbr-certificate-validate-fail](CodeChanges/f5-lbr-certificate-validate-fail.md)
- [gitlab-gl-app-activity-success](CodeChanges/gitlab-gl-app-activity-success.md)
- [humansecurity-botdefender-app-activity-fail](CodeChanges/humansecurity-botdefender-app-activity-fail.md)
- [humansecurity-botdefender-app-activity-success](CodeChanges/humansecurity-botdefender-app-activity-success.md)
- [knowbe4-sat-app-activity-success](CodeChanges/knowbe4-sat-app-activity-success.md)
- [lanscope-cat-peripheral-device-activity-fail](CodeChanges/lanscope-cat-peripheral-device-activity-fail.md)
- [lanscope-cat-peripheral-device-activity-success](CodeChanges/lanscope-cat-peripheral-device-activity-success.md)
- [lumension-peripheral-device-insert-success](CodeChanges/lumension-peripheral-device-insert-success.md)
- [mcafee-es-peripheral-device-activity-success](CodeChanges/mcafee-es-peripheral-device-activity-success.md)
- [mcafee-es-peripheral-device-insert-success](CodeChanges/mcafee-es-peripheral-device-insert-success.md)
- [microsoft-windows-peripheral-device-activity-success](CodeChanges/microsoft-windows-peripheral-device-activity-success.md)
- [microsoft-windows-peripheral-device-insert-success](CodeChanges/microsoft-windows-peripheral-device-insert-success.md)
- [ordr-network-alert-trigger-success](CodeChanges/ordr-network-alert-trigger-success.md)
- [ordr-sce-endpoint-activity-success](CodeChanges/ordr-sce-endpoint-activity-success.md)
- [proofpoint-casb-alert-trigger-success](CodeChanges/proofpoint-casb-alert-trigger-success.md)
- [salesforce-app-activity-success-2](CodeChanges/salesforce-app-activity-success-2.md)
- [salesforce-http-request-fail](CodeChanges/salesforce-http-request-fail.md)
- [salesforce-http-request-success](CodeChanges/salesforce-http-request-success.md)
- [skysea-clientview-peripheral-device-activity-success](CodeChanges/skysea-clientview-peripheral-device-activity-success.md)
- [sophos-endpointprotection-peripheral-device-insert-success-1](CodeChanges/sophos-endpointprotection-peripheral-device-insert-success-1.md)
- [sophos-ep-peripheral-device-insert-success](CodeChanges/sophos-ep-peripheral-device-insert-success.md)
- [symantec-dlp-peripheral-device-insert-success](CodeChanges/symantec-dlp-peripheral-device-insert-success.md)
- [symantec-endpointprotection-peripheral-device-activity-fail](CodeChanges/symantec-endpointprotection-peripheral-device-activity-fail.md)
- [symantec-endpointprotection-peripheral-device-activity-success](CodeChanges/symantec-endpointprotection-peripheral-device-activity-success.md)
- [thoughtspot-ts-app-login-fail](CodeChanges/thoughtspot-ts-app-login-fail.md)
- [thoughtspot-ts-app-login-success](CodeChanges/thoughtspot-ts-app-login-success.md)
- [thoughtspot-ts-group-modify-success](CodeChanges/thoughtspot-ts-group-modify-success.md)
- [thoughtspot-ts-user-create-success](CodeChanges/thoughtspot-ts-user-create-success.md)
- [thoughtspot-ts-user-delete-success](CodeChanges/thoughtspot-ts-user-delete-success.md)
- [thoughtspot-ts-user-modify-success](CodeChanges/thoughtspot-ts-user-modify-success.md)
- [thoughtspot-ts-user-password-modify-success](CodeChanges/thoughtspot-ts-user-password-modify-success.md)
- [vmware-cbappcontrol-peripheral-device-insert-success](CodeChanges/vmware-cbappcontrol-peripheral-device-insert-success.md)

#### Edit Conditions
<a id="edit-conditions"></a>
- [akamai-guardicore-app-activity-success](CodeChanges/akamai-guardicore-app-activity-success.md)
- [akamai-guardicore-app-authentication-fail](CodeChanges/akamai-guardicore-app-authentication-fail.md)
- [akamai-guardicore-app-authentication-success](CodeChanges/akamai-guardicore-app-authentication-success.md)
- [dl-microsoft-windows-file-write-success-1](CodeChanges/dl-microsoft-windows-file-write-success-1.md)
- [dl-pan-ngfw-app-login-success](CodeChanges/dl-pan-ngfw-app-login-success.md)
- [salesforce-app-login-fail](CodeChanges/salesforce-app-login-fail.md)
- [salesforce-app-login-success](CodeChanges/salesforce-app-login-success.md)
- [thoughtspot-ts-app-activity-success](CodeChanges/thoughtspot-ts-app-activity-success.md)

#### Removed Event Builder
<a id="removed-event-builder"></a>
- [assetview-windows-peripheral_storage-insert-success](CodeChanges/assetview-windows-peripheral_storage-insert-success.md)
- [code42-incydr-peripheral_storage-activity-success](CodeChanges/code42-incydr-peripheral_storage-activity-success.md)
- [crowdstrike-falcon-peripheral-storage-insert-success](CodeChanges/crowdstrike-falcon-peripheral-storage-insert-success.md)
- [crowdstrike-falcon-peripheral-storage-insert-success-lin](CodeChanges/crowdstrike-falcon-peripheral-storage-insert-success-lin.md)
- [crowdstrike-falcon-peripheral-storage-insert-success-win](CodeChanges/crowdstrike-falcon-peripheral-storage-insert-success-win.md)
- [crowdstrike-macos-peripheral-storage-activity-success](CodeChanges/crowdstrike-macos-peripheral-storage-activity-success.md)
- [crowdstrike-unix-peripheral-storage-activity-success](CodeChanges/crowdstrike-unix-peripheral-storage-activity-success.md)
- [crowdstrike-windows-peripheral-storage-activity-success](CodeChanges/crowdstrike-windows-peripheral-storage-activity-success.md)
- [dl-crowdstrike-falcon-peripheral-storage-activity-success](CodeChanges/dl-crowdstrike-falcon-peripheral-storage-activity-success.md)
- [dl-crowdstrike-falcon-peripheral-storage-activity-success-1](CodeChanges/dl-crowdstrike-falcon-peripheral-storage-activity-success-1.md)
- [dl-crowdstrike-falcon-peripheral-storage-activity-success-2](CodeChanges/dl-crowdstrike-falcon-peripheral-storage-activity-success-2.md)
- [dl-crowdstrike-falcon-peripheral-storage-activity-success-lin](CodeChanges/dl-crowdstrike-falcon-peripheral-storage-activity-success-lin.md)
- [dl-crowdstrike-falcon-peripheral-storage-activity-success-win](CodeChanges/dl-crowdstrike-falcon-peripheral-storage-activity-success-win.md)
- [dl-crowdstrike-falcon-peripheral-storage-insert-success](CodeChanges/dl-crowdstrike-falcon-peripheral-storage-insert-success.md)
- [dl-microsoft-windows-peripheral-storage-remove-success](CodeChanges/dl-microsoft-windows-peripheral-storage-remove-success.md)
- [dl-pan-ngfw-app-login-fail](CodeChanges/dl-pan-ngfw-app-login-fail.md)
- [lanscope-cat-peripheral-storage-activity-fail](CodeChanges/lanscope-cat-peripheral-storage-activity-fail.md)
- [lanscope-cat-peripheral-storage-activity-success](CodeChanges/lanscope-cat-peripheral-storage-activity-success.md)
- [lumension-peripheral-storage-insert-success](CodeChanges/lumension-peripheral-storage-insert-success.md)
- [mcafee-es-peripheral-storage-activity-success](CodeChanges/mcafee-es-peripheral-storage-activity-success.md)
- [mcafee-es-peripheral-storage-insert-success](CodeChanges/mcafee-es-peripheral-storage-insert-success.md)
- [microsoft-windows-peripheral-storage-activity-success](CodeChanges/microsoft-windows-peripheral-storage-activity-success.md)
- [microsoft-windows-peripheral-storage-insert-success](CodeChanges/microsoft-windows-peripheral-storage-insert-success.md)
- [skysea-clientview-peripheral-storage-activity-success](CodeChanges/skysea-clientview-peripheral-storage-activity-success.md)
- [sophos-endpointprotection-peripheral-storage-insert-success-1](CodeChanges/sophos-endpointprotection-peripheral-storage-insert-success-1.md)
- [sophos-ep-peripheral-storage-insert-success](CodeChanges/sophos-ep-peripheral-storage-insert-success.md)
- [symantec-dlp-peripheral-storage-insert-success](CodeChanges/symantec-dlp-peripheral-storage-insert-success.md)
- [symantec-endpointprotection-peripheral-storage-activity-fail](CodeChanges/symantec-endpointprotection-peripheral-storage-activity-fail.md)
- [symantec-endpointprotection-peripheral-storage-activity-success](CodeChanges/symantec-endpointprotection-peripheral-storage-activity-success.md)
- [vmware-cbappcontrol-peripheral-storage-insert-success](CodeChanges/vmware-cbappcontrol-peripheral-storage-insert-success.md)

</details>

<details>
<summary><strong id="parser">Parser (272)</strong></summary>


### Change Types
- [Could Not Compare](#could-not-compare)
- [Added Parser](#added-parser)
- [Changed](#changed)
- [Changed Parsed Fields](#changed-parsed-fields)
- [Edit Attribute](#edit-attribute)
- [Edit Regex Field](#edit-regex-field)
- [Removed Parser](#removed-parser)

#### Could Not Compare
<a id="could-not-compare"></a>
- [amazon-awscloudtrail-cef-app-activity-awsapicall](CodeChanges/amazon-awscloudtrail-cef-app-activity-awsapicall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-cef-app-activity-awsapicall&type=code)
- [snowflake-s-json-database-activity-success-querytext](CodeChanges/snowflake-s-json-database-activity-success-querytext.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20snowflake-s-json-database-activity-success-querytext&type=code)

#### Added Parser
<a id="added-parser"></a>
- [akamai-guardicore-cef-alert-trigger-success-revealincident](CodeChanges/akamai-guardicore-cef-alert-trigger-success-revealincident.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20akamai-guardicore-cef-alert-trigger-success-revealincident&type=code)
- [apache-a-str-http-session-apacheaccess](CodeChanges/apache-a-str-http-session-apacheaccess.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20apache-a-str-http-session-apacheaccess&type=code)
- [f5-asm-csv-network-traffic-success-passed](CodeChanges/f5-asm-csv-network-traffic-success-passed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20f5-asm-csv-network-traffic-success-passed&type=code)
- [f5-asm-kv-alert-trigger-success-botdefense](CodeChanges/f5-asm-kv-alert-trigger-success-botdefense.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20f5-asm-kv-alert-trigger-success-botdefense&type=code)
- [f5-bigip-str-network-notification-success](CodeChanges/f5-bigip-str-network-notification-success.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20f5-bigip-str-network-notification-success&type=code)
- [f5-lbr-str-ssl-error](CodeChanges/f5-lbr-str-ssl-error.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20f5-lbr-str-ssl-error&type=code)
- [gitlab-gl-json-app-activity-success-entity](CodeChanges/gitlab-gl-json-app-activity-success-entity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20gitlab-gl-json-app-activity-success-entity&type=code)
- [google-agentspace-json-app-activity-success-agentspace](CodeChanges/google-agentspace-json-app-activity-success-agentspace.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20google-agentspace-json-app-activity-success-agentspace&type=code)
- [humansecurity-botdefender-json-app-activity-botdefender](CodeChanges/humansecurity-botdefender-json-app-activity-botdefender.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20humansecurity-botdefender-json-app-activity-botdefender&type=code)
- [knowbe4-sat-json-app-activity-success-kmsat](CodeChanges/knowbe4-sat-json-app-activity-success-kmsat.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20knowbe4-sat-json-app-activity-success-kmsat&type=code)
- [microsoft-iis-str-http-session-getapi](CodeChanges/microsoft-iis-str-http-session-getapi.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-iis-str-http-session-getapi&type=code)
- [microsoft-iis-str-http-session-postapi](CodeChanges/microsoft-iis-str-http-session-postapi.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-iis-str-http-session-postapi&type=code)
- [ordr-sce-json-alert-trigger-success-warning](CodeChanges/ordr-sce-json-alert-trigger-success-warning.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20ordr-sce-json-alert-trigger-success-warning&type=code)
- [ordr-sce-kv-endpoint-activity-success-deviceevents](CodeChanges/ordr-sce-kv-endpoint-activity-success-deviceevents.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20ordr-sce-kv-endpoint-activity-success-deviceevents&type=code)
- [postgresql-p-str-database-activity-context](CodeChanges/postgresql-p-str-database-activity-context.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20postgresql-p-str-database-activity-context&type=code)
- [postgresql-p-str-database-activity-detail](CodeChanges/postgresql-p-str-database-activity-detail.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20postgresql-p-str-database-activity-detail&type=code)
- [postgresql-p-str-database-activity-fatal](CodeChanges/postgresql-p-str-database-activity-fatal.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20postgresql-p-str-database-activity-fatal&type=code)
- [postgresql-p-str-database-activity-log](CodeChanges/postgresql-p-str-database-activity-log.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20postgresql-p-str-database-activity-log&type=code)
- [postgresql-p-str-database-login-fail-password-doesnotmatch](CodeChanges/postgresql-p-str-database-login-fail-password-doesnotmatch.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20postgresql-p-str-database-login-fail-password-doesnotmatch&type=code)
- [proofpoint-casb-json-alert-trigger-success-dataleakage](CodeChanges/proofpoint-casb-json-alert-trigger-success-dataleakage.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20proofpoint-casb-json-alert-trigger-success-dataleakage&type=code)
- [tenable-t-json-endpoint-scan-scaninformation](CodeChanges/tenable-t-json-endpoint-scan-scaninformation.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20tenable-t-json-endpoint-scan-scaninformation&type=code)
- [thoughtspot-ts-json-app-activity-success-type](CodeChanges/thoughtspot-ts-json-app-activity-success-type.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20thoughtspot-ts-json-app-activity-success-type&type=code)

#### Changed
<a id="changed"></a>
- [akamai-guardicore-cef-app-activity-userauth](CodeChanges/akamai-guardicore-cef-app-activity-userauth.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20akamai-guardicore-cef-app-activity-userauth&type=code)
- [cisco-ise-str-app-notification-alarm](CodeChanges/cisco-ise-str-app-notification-alarm.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-ise-str-app-notification-alarm&type=code)
- [fireeye-networksecurity-json-http-session-success-http](CodeChanges/fireeye-networksecurity-json-http-session-success-http.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20fireeye-networksecurity-json-http-session-success-http&type=code)
- [postgresql-p-str-database-login-fail-role-doesnt_exist](CodeChanges/postgresql-p-str-database-login-fail-role-doesnt_exist.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20postgresql-p-str-database-login-fail-role-doesnt_exist&type=code)
- [salesforce-sf-json-app-activity-success-loginhistory](CodeChanges/salesforce-sf-json-app-activity-success-loginhistory.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20salesforce-sf-json-app-activity-success-loginhistory&type=code)

#### Changed Parsed Fields
<a id="changed-parsed-fields"></a>
- [azure-azuread-json-app-activity-addapplication](CodeChanges/azure-azuread-json-app-activity-addapplication.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-app-activity-addapplication&type=code)
- [azure-azuread-json-app-activity-addownertoapplication](CodeChanges/azure-azuread-json-app-activity-addownertoapplication.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-app-activity-addownertoapplication&type=code)
- [azure-azuread-json-app-activity-deletedevice](CodeChanges/azure-azuread-json-app-activity-deletedevice.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-app-activity-deletedevice&type=code)
- [azure-azuread-json-app-activity-export](CodeChanges/azure-azuread-json-app-activity-export.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-app-activity-export&type=code)
- [azure-azuread-json-app-activity-removeownerfromgroup](CodeChanges/azure-azuread-json-app-activity-removeownerfromgroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-app-activity-removeownerfromgroup&type=code)
- [azure-azuread-json-app-activity-success-other](CodeChanges/azure-azuread-json-app-activity-success-other.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-app-activity-success-other&type=code)
- [azure-azuread-json-app-activity-success-other-1](CodeChanges/azure-azuread-json-app-activity-success-other-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-app-activity-success-other-1&type=code)
- [azure-azuread-json-app-activity-success-updatedevice](CodeChanges/azure-azuread-json-app-activity-success-updatedevice.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-app-activity-success-updatedevice&type=code)
- [azure-azuread-json-app-activity-updateuser](CodeChanges/azure-azuread-json-app-activity-updateuser.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-app-activity-updateuser&type=code)
- [azure-azuread-json-app-activity-useractivitydisplayname](CodeChanges/azure-azuread-json-app-activity-useractivitydisplayname.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-app-activity-useractivitydisplayname&type=code)
- [azure-azuread-json-app-activity-useractivitydisplayname-1](CodeChanges/azure-azuread-json-app-activity-useractivitydisplayname-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-app-activity-useractivitydisplayname-1&type=code)
- [azure-azuread-json-app-authentication-updatestsrefreshtokenvalidfromtimestamp](CodeChanges/azure-azuread-json-app-authentication-updatestsrefreshtokenvalidfromtimestamp.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-app-authentication-updatestsrefreshtokenvalidfromtimestamp&type=code)
- [azure-azuread-json-app-authentication-userregisteredsecurityinfo](CodeChanges/azure-azuread-json-app-authentication-userregisteredsecurityinfo.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-app-authentication-userregisteredsecurityinfo&type=code)
- [azure-azuread-json-app-authentication-userstartedsecurityinforegistration](CodeChanges/azure-azuread-json-app-authentication-userstartedsecurityinforegistration.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-app-authentication-userstartedsecurityinforegistration&type=code)
- [azure-azuread-json-app-notification-activitydisplayname](CodeChanges/azure-azuread-json-app-notification-activitydisplayname.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-app-notification-activitydisplayname&type=code)
- [azure-azuread-json-group-member-add-success-addmembertogroup](CodeChanges/azure-azuread-json-group-member-add-success-addmembertogroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-group-member-add-success-addmembertogroup&type=code)
- [azure-azuread-json-group-modify-success-updategroup](CodeChanges/azure-azuread-json-group-modify-success-updategroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-group-modify-success-updategroup&type=code)
- [azure-azuread-json-key-create-success-bitlocker](CodeChanges/azure-azuread-json-key-create-success-bitlocker.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-key-create-success-bitlocker&type=code)
- [azure-azuread-json-key-delete-deletebitlockerkey](CodeChanges/azure-azuread-json-key-delete-deletebitlockerkey.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-key-delete-deletebitlockerkey&type=code)
- [azure-azuread-json-key-read-success-bitlocker](CodeChanges/azure-azuread-json-key-read-success-bitlocker.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-key-read-success-bitlocker&type=code)
- [azure-azuread-json-user-enable-success-enableaccount](CodeChanges/azure-azuread-json-user-enable-success-enableaccount.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-user-enable-success-enableaccount&type=code)
- [azure-azuread-json-user-password-modify-success-changepassword](CodeChanges/azure-azuread-json-user-password-modify-success-changepassword.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-user-password-modify-success-changepassword&type=code)
- [azure-azuread-json-user-password-modify-success-selfservice-1](CodeChanges/azure-azuread-json-user-password-modify-success-selfservice-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-user-password-modify-success-selfservice-1&type=code)
- [azure-azuread-json-user-password-reset-success-resetpassword](CodeChanges/azure-azuread-json-user-password-reset-success-resetpassword.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-user-password-reset-success-resetpassword&type=code)
- [azure-azuread-json-user-password-reset-success-resetpasswordself](CodeChanges/azure-azuread-json-user-password-reset-success-resetpasswordself.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-user-password-reset-success-resetpasswordself&type=code)
- [checkpoint-am-cef-alert-trigger-success-checkpointantimalware](CodeChanges/checkpoint-am-cef-alert-trigger-success-checkpointantimalware.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-am-cef-alert-trigger-success-checkpointantimalware&type=code)
- [checkpoint-es-cef-alert-trigger-success-checkpoint](CodeChanges/checkpoint-es-cef-alert-trigger-success-checkpoint.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-es-cef-alert-trigger-success-checkpoint&type=code)
- [f5-asm-cef-alert-trigger-success-cookie](CodeChanges/f5-asm-cef-alert-trigger-success-cookie.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20f5-asm-cef-alert-trigger-success-cookie&type=code)
- [google-gcpca-sk4-app-activity-cloud](CodeChanges/google-gcpca-sk4-app-activity-cloud.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20google-gcpca-sk4-app-activity-cloud&type=code)
- [microsoft-azure-json-app-activity-addgroup-1](CodeChanges/microsoft-azure-json-app-activity-addgroup-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-json-app-activity-addgroup-1&type=code)
- [microsoft-azure-json-app-activity-adduser](CodeChanges/microsoft-azure-json-app-activity-adduser.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-json-app-activity-adduser&type=code)
- [microsoft-azure-json-app-activity-changeuserlicense](CodeChanges/microsoft-azure-json-app-activity-changeuserlicense.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-json-app-activity-changeuserlicense&type=code)
- [microsoft-azure-json-app-activity-deleteuser](CodeChanges/microsoft-azure-json-app-activity-deleteuser.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-json-app-activity-deleteuser&type=code)
- [microsoft-azure-json-app-activity-harddeletegroup](CodeChanges/microsoft-azure-json-app-activity-harddeletegroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-json-app-activity-harddeletegroup&type=code)
- [microsoft-azure-json-group-member-remove-success-removefromgroup](CodeChanges/microsoft-azure-json-group-member-remove-success-removefromgroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-json-group-member-remove-success-removefromgroup&type=code)
- [microsoft-azuread-json-user-disable-success-accountdisable-1](CodeChanges/microsoft-azuread-json-user-disable-success-accountdisable-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuread-json-user-disable-success-accountdisable-1&type=code)
- [microsoft-azuread-json-user-password-modify-success-changepassword](CodeChanges/microsoft-azuread-json-user-password-modify-success-changepassword.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuread-json-user-password-modify-success-changepassword&type=code)
- [microsoft-evapp-json-certificate-expire-64](CodeChanges/microsoft-evapp-json-certificate-expire-64.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-json-certificate-expire-64&type=code)
- [microsoft-evapp-json-configuration-modify-16028](CodeChanges/microsoft-evapp-json-configuration-modify-16028.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-json-configuration-modify-16028&type=code)
- [microsoft-evapp-json-endpoint-activity-fail-5605](CodeChanges/microsoft-evapp-json-endpoint-activity-fail-5605.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-json-endpoint-activity-fail-5605&type=code)
- [microsoft-evapp-json-endpoint-activity-success-catchall](CodeChanges/microsoft-evapp-json-endpoint-activity-success-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-json-endpoint-activity-success-catchall&type=code)
- [microsoft-evapp-json-endpoint-notification-1000](CodeChanges/microsoft-evapp-json-endpoint-notification-1000.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-json-endpoint-notification-1000&type=code)
- [microsoft-evapp-json-file-close-success-327](CodeChanges/microsoft-evapp-json-file-close-success-327.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-json-file-close-success-327&type=code)
- [microsoft-evapp-json-file-read-success-326](CodeChanges/microsoft-evapp-json-file-read-success-326.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-json-file-read-success-326&type=code)
- [microsoft-evapp-json-script-execute-fail-4100](CodeChanges/microsoft-evapp-json-script-execute-fail-4100.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-json-script-execute-fail-4100&type=code)
- [microsoft-evsecurity-json-driver-load-fail-5038](CodeChanges/microsoft-evsecurity-json-driver-load-fail-5038.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-driver-load-fail-5038&type=code)
- [microsoft-evsecurity-json-policy-modify-4946-1](CodeChanges/microsoft-evsecurity-json-policy-modify-4946-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-policy-modify-4946-1&type=code)
- [microsoft-evsecurity-json-policy-modify-4948-1](CodeChanges/microsoft-evsecurity-json-policy-modify-4948-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-policy-modify-4948-1&type=code)
- [microsoft-evsecurity-json-policy-modify-success-4947](CodeChanges/microsoft-evsecurity-json-policy-modify-success-4947.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-policy-modify-success-4947&type=code)
- [microsoft-evsecurity-json-user-lock-success-4740](CodeChanges/microsoft-evsecurity-json-user-lock-success-4740.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-user-lock-success-4740&type=code)
- [microsoft-evsecurity-xml-user-lock-success-4740](CodeChanges/microsoft-evsecurity-xml-user-lock-success-4740.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-user-lock-success-4740&type=code)
- [microsoft-evsecurity-xml-user-lock-success-4740-1](CodeChanges/microsoft-evsecurity-xml-user-lock-success-4740-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-user-lock-success-4740-1&type=code)
- [microsoft-evsystem-json-endpoint-activity-success-catchall](CodeChanges/microsoft-evsystem-json-endpoint-activity-success-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-json-endpoint-activity-success-catchall&type=code)
- [microsoft-evsystem-json-policy-apply-fail-1030](CodeChanges/microsoft-evsystem-json-policy-apply-fail-1030.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-json-policy-apply-fail-1030&type=code)
- [microsoft-evsystem-json-policy-apply-success-1502](CodeChanges/microsoft-evsystem-json-policy-apply-success-1502.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-json-policy-apply-success-1502&type=code)
- [microsoft-evsystem-json-service-state-modify-7036](CodeChanges/microsoft-evsystem-json-service-state-modify-7036.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-json-service-state-modify-7036&type=code)
- [microsoft-evsystem-json-service-state-modify-7040](CodeChanges/microsoft-evsystem-json-service-state-modify-7040.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-json-service-state-modify-7040&type=code)
- [microsoft-evsystem-json-service-state-modify-7040-1](CodeChanges/microsoft-evsystem-json-service-state-modify-7040-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-json-service-state-modify-7040-1&type=code)
- [microsoft-evsystem-json-ssl-start-fail-36874](CodeChanges/microsoft-evsystem-json-ssl-start-fail-36874.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-json-ssl-start-fail-36874&type=code)
- [microsoft-evsystem-kv-service-state-modify-7040](CodeChanges/microsoft-evsystem-kv-service-state-modify-7040.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-kv-service-state-modify-7040&type=code)
- [microsoft-evsystem-str-service-state-modify-7036](CodeChanges/microsoft-evsystem-str-service-state-modify-7036.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-str-service-state-modify-7036&type=code)
- [microsoft-evsystem-str-service-state-modify-7036-1](CodeChanges/microsoft-evsystem-str-service-state-modify-7036-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-str-service-state-modify-7036-1&type=code)
- [microsoft-evsystem-str-service-state-modify-7036-2](CodeChanges/microsoft-evsystem-str-service-state-modify-7036-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-str-service-state-modify-7036-2&type=code)
- [microsoft-evsystem-str-service-state-modify-7036-3](CodeChanges/microsoft-evsystem-str-service-state-modify-7036-3.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-str-service-state-modify-7036-3&type=code)
- [microsoft-evsystem-str-service-state-modify-7036-4](CodeChanges/microsoft-evsystem-str-service-state-modify-7036-4.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-str-service-state-modify-7036-4&type=code)
- [microsoft-evsystem-str-service-state-modify-7040](CodeChanges/microsoft-evsystem-str-service-state-modify-7040.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-str-service-state-modify-7040&type=code)
- [microsoft-evsystem-xml-service-state-modify-7036](CodeChanges/microsoft-evsystem-xml-service-state-modify-7036.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-xml-service-state-modify-7036&type=code)
- [microsoft-evsystem-xml-service-state-modify-7036-1](CodeChanges/microsoft-evsystem-xml-service-state-modify-7036-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-xml-service-state-modify-7036-1&type=code)
- [microsoft-mcas-cef-app-activity-success-catchall](CodeChanges/microsoft-mcas-cef-app-activity-success-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-mcas-cef-app-activity-success-catchall&type=code)
- [microsoft-o365-json-app-activity-success-groupmanagementaddowner](CodeChanges/microsoft-o365-json-app-activity-success-groupmanagementaddowner.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-json-app-activity-success-groupmanagementaddowner&type=code)
- [microsoft-o365-json-app-file-success-inviteexternaluser](CodeChanges/microsoft-o365-json-app-file-success-inviteexternaluser.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-json-app-file-success-inviteexternaluser&type=code)
- [microsoft-o365-json-app-file-success-restoreuser](CodeChanges/microsoft-o365-json-app-file-success-restoreuser.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-json-app-file-success-restoreuser&type=code)
- [okta-amfa-mix-app-login-success-securitycontext](CodeChanges/okta-amfa-mix-app-login-success-securitycontext.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20okta-amfa-mix-app-login-success-securitycontext&type=code)
- [vectra-cd-json-alert-trigger-success-detection](CodeChanges/vectra-cd-json-alert-trigger-success-detection.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vectra-cd-json-alert-trigger-success-detection&type=code)
- [vectra-cd-json-alert-trigger-success-detection-1](CodeChanges/vectra-cd-json-alert-trigger-success-detection-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vectra-cd-json-alert-trigger-success-detection-1&type=code)

#### Edit Attribute
<a id="edit-attribute"></a>
- [assetview-av-csv-peripheral-storage-insert-success-15031](CodeChanges/assetview-av-csv-peripheral-storage-insert-success-15031.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20assetview-av-csv-peripheral-storage-insert-success-15031&type=code)
- [cisco-mma-json-network-traffic-success-addressingvlans](CodeChanges/cisco-mma-json-network-traffic-success-addressingvlans.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-mma-json-network-traffic-success-addressingvlans&type=code)
- [cisco-netsec-json-network-traffic-success-categorytype](CodeChanges/cisco-netsec-json-network-traffic-success-categorytype.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-netsec-json-network-traffic-success-categorytype&type=code)
- [code42-incydr-json-file-succes-file](CodeChanges/code42-incydr-json-file-succes-file.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20code42-incydr-json-file-succes-file&type=code)
- [crowdstrike-falcon-cef-peripheral-storage-activity-success-dcusbdevicedisconnected](CodeChanges/crowdstrike-falcon-cef-peripheral-storage-activity-success-dcusbdevicedisconnected.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-cef-peripheral-storage-activity-success-dcusbdevicedisconnected&type=code)
- [crowdstrike-falcon-cef-peripheral-storage-insert-success-dcusbdeviceconnected](CodeChanges/crowdstrike-falcon-cef-peripheral-storage-insert-success-dcusbdeviceconnected.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-cef-peripheral-storage-insert-success-dcusbdeviceconnected&type=code)
- [crowdstrike-falcon-mix-peripheral-storage-insert-success-removablemediavolumemounted](CodeChanges/crowdstrike-falcon-mix-peripheral-storage-insert-success-removablemediavolumemounted.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-mix-peripheral-storage-insert-success-removablemediavolumemounted&type=code)
- [crowdstrike-falcon-sk4-peripheral-storage-activity-dcusb](CodeChanges/crowdstrike-falcon-sk4-peripheral-storage-activity-dcusb.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-sk4-peripheral-storage-activity-dcusb&type=code)
- [lanscope-cat-kv-peripheral-storage-activity-windowtitle](CodeChanges/lanscope-cat-kv-peripheral-storage-activity-windowtitle.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20lanscope-cat-kv-peripheral-storage-activity-windowtitle&type=code)
- [lumension-l-kv-peripheral-storage-insert-success-mediuminserted](CodeChanges/lumension-l-kv-peripheral-storage-insert-success-mediuminserted.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20lumension-l-kv-peripheral-storage-insert-success-mediuminserted&type=code)
- [mcafee-es-xml-peripheral-storage-activity-success-20504](CodeChanges/mcafee-es-xml-peripheral-storage-activity-success-20504.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20mcafee-es-xml-peripheral-storage-activity-success-20504&type=code)
- [mcafee-es-xml-peripheral-storage-activity-success-20508](CodeChanges/mcafee-es-xml-peripheral-storage-activity-success-20508.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20mcafee-es-xml-peripheral-storage-activity-success-20508&type=code)
- [mcafee-es-xml-peripheral-storage-insert-success-20500](CodeChanges/mcafee-es-xml-peripheral-storage-insert-success-20500.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20mcafee-es-xml-peripheral-storage-insert-success-20500&type=code)
- [mcafee-es-xml-peripheral-storage-insert-success-20507](CodeChanges/mcafee-es-xml-peripheral-storage-insert-success-20507.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20mcafee-es-xml-peripheral-storage-insert-success-20507&type=code)
- [microsoft-defenderep-json-endpoint-notification-pnpdeviceconnected](CodeChanges/microsoft-defenderep-json-endpoint-notification-pnpdeviceconnected.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-json-endpoint-notification-pnpdeviceconnected&type=code)
- [microsoft-defenderep-json-peripheral_storage-insert-success-usbdrivemounted](CodeChanges/microsoft-defenderep-json-peripheral_storage-insert-success-usbdrivemounted.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-json-peripheral_storage-insert-success-usbdrivemounted&type=code)
- [microsoft-defenderep-json-peripheral_storage-remove-success-usbdriveunmounted](CodeChanges/microsoft-defenderep-json-peripheral_storage-remove-success-usbdriveunmounted.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-json-peripheral_storage-remove-success-usbdriveunmounted&type=code)
- [microsoft-evsecurity-cef-peripheral-storage-insert-success-6416](CodeChanges/microsoft-evsecurity-cef-peripheral-storage-insert-success-6416.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-peripheral-storage-insert-success-6416&type=code)
- [microsoft-evsecurity-cef-peripheral-storage-insert-success-6422](CodeChanges/microsoft-evsecurity-cef-peripheral-storage-insert-success-6422.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-peripheral-storage-insert-success-6422&type=code)
- [microsoft-evsecurity-json-peripheral-storage-insert-success-6416](CodeChanges/microsoft-evsecurity-json-peripheral-storage-insert-success-6416.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-peripheral-storage-insert-success-6416&type=code)
- [microsoft-evsecurity-kv-file-fileoperation](CodeChanges/microsoft-evsecurity-kv-file-fileoperation.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-file-fileoperation&type=code)
- [microsoft-evsecurity-kv-peripheralstorage-insert-success-6416](CodeChanges/microsoft-evsecurity-kv-peripheralstorage-insert-success-6416.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-peripheralstorage-insert-success-6416&type=code)
- [microsoft-evsecurity-sk4-peripheral_storage-insert-success-6416](CodeChanges/microsoft-evsecurity-sk4-peripheral_storage-insert-success-6416.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-sk4-peripheral_storage-insert-success-6416&type=code)
- [microsoft-evsecurity-xml-peripheral-storage-insert-success-6416](CodeChanges/microsoft-evsecurity-xml-peripheral-storage-insert-success-6416.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-peripheral-storage-insert-success-6416&type=code)
- [microsoft-evsecurity-xml-peripheral-storage-insert-success-6422](CodeChanges/microsoft-evsecurity-xml-peripheral-storage-insert-success-6422.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-peripheral-storage-insert-success-6422&type=code)
- [microsoft-evsecurity-xml-peripheral-storage-insert-success-devicewasrecognized](CodeChanges/microsoft-evsecurity-xml-peripheral-storage-insert-success-devicewasrecognized.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-peripheral-storage-insert-success-devicewasrecognized&type=code)
- [microsoft-evsecurity-xml-peripheral-storage-insert-success-enabledevice](CodeChanges/microsoft-evsecurity-xml-peripheral-storage-insert-success-enabledevice.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-peripheral-storage-insert-success-enabledevice&type=code)
- [microsoft-o365-sk4-app-activity-success-forward](CodeChanges/microsoft-o365-sk4-app-activity-success-forward.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-sk4-app-activity-success-forward&type=code)
- [microsoft-o365-sk4-app-activity-success-forwardto](CodeChanges/microsoft-o365-sk4-app-activity-success-forwardto.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-sk4-app-activity-success-forwardto&type=code)
- [microsoft-wdac-str-endpoint-notification-success-3033](CodeChanges/microsoft-wdac-str-endpoint-notification-success-3033.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-wdac-str-endpoint-notification-success-3033&type=code)
- [microsoft-wdac-xml-endpoint-notification-success-3033](CodeChanges/microsoft-wdac-xml-endpoint-notification-success-3033.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-wdac-xml-endpoint-notification-success-3033&type=code)
- [microsoft-windows-cef-peripheral-storage-activity-success-6421](CodeChanges/microsoft-windows-cef-peripheral-storage-activity-success-6421.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-windows-cef-peripheral-storage-activity-success-6421&type=code)
- [microsoft-windows-xml-peripheral-storage-activity-success-devicewasdisable](CodeChanges/microsoft-windows-xml-peripheral-storage-activity-success-devicewasdisable.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-windows-xml-peripheral-storage-activity-success-devicewasdisable&type=code)
- [microsoft-windows-xml-peripheral-storage-activity-success-disable](CodeChanges/microsoft-windows-xml-peripheral-storage-activity-success-disable.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-windows-xml-peripheral-storage-activity-success-disable&type=code)
- [microsoft-windows-xml-peripheral-storage-activity-success-enableadevice](CodeChanges/microsoft-windows-xml-peripheral-storage-activity-success-enableadevice.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-windows-xml-peripheral-storage-activity-success-enableadevice&type=code)
- [pan-gp-csv-vpn-login-useridlogin](CodeChanges/pan-gp-csv-vpn-login-useridlogin.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-gp-csv-vpn-login-useridlogin&type=code)
- [skysea-cv-csv-peripheral-storage-activity-success-usbactivity](CodeChanges/skysea-cv-csv-peripheral-storage-activity-success-usbactivity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20skysea-cv-csv-peripheral-storage-activity-success-usbactivity&type=code)
- [sophos-ep-cef-peripheral-storage-insert-success-alertedonly](CodeChanges/sophos-ep-cef-peripheral-storage-insert-success-alertedonly.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sophos-ep-cef-peripheral-storage-insert-success-alertedonly&type=code)
- [sophos-ep-cef-peripheral-storage-insert-success-peripherals](CodeChanges/sophos-ep-cef-peripheral-storage-insert-success-peripherals.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sophos-ep-cef-peripheral-storage-insert-success-peripherals&type=code)
- [sophos-ep-json-peripheral-storage-insert-success-peripheral](CodeChanges/sophos-ep-json-peripheral-storage-insert-success-peripheral.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sophos-ep-json-peripheral-storage-insert-success-peripheral&type=code)
- [symantec-dlp-kv-peripheral-storage-insert-success-allowedthedevice](CodeChanges/symantec-dlp-kv-peripheral-storage-insert-success-allowedthedevice.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20symantec-dlp-kv-peripheral-storage-insert-success-allowedthedevice&type=code)
- [symantec-dlp-kv-peripheral-storage-insert-success-devicewas](CodeChanges/symantec-dlp-kv-peripheral-storage-insert-success-devicewas.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20symantec-dlp-kv-peripheral-storage-insert-success-devicewas&type=code)
- [symantec-endpointprotection-csv-peripheral-storage-activity-fail-blocked](CodeChanges/symantec-endpointprotection-csv-peripheral-storage-activity-fail-blocked.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20symantec-endpointprotection-csv-peripheral-storage-activity-fail-blocked&type=code)
- [symantec-endpointprotection-json-peripheral_storage-insert-fail-blockautoruninf](CodeChanges/symantec-endpointprotection-json-peripheral_storage-insert-fail-blockautoruninf.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20symantec-endpointprotection-json-peripheral_storage-insert-fail-blockautoruninf&type=code)
- [vmware-carbonblackappctrl-kv-peripheral-storage-insert-success-deviceattached](CodeChanges/vmware-carbonblackappctrl-kv-peripheral-storage-insert-success-deviceattached.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-carbonblackappctrl-kv-peripheral-storage-insert-success-deviceattached&type=code)
- [vmware-carbonblackappctrl-kv-peripheral-storage-insert-success-devicedetached](CodeChanges/vmware-carbonblackappctrl-kv-peripheral-storage-insert-success-devicedetached.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-carbonblackappctrl-kv-peripheral-storage-insert-success-devicedetached&type=code)

#### Edit Regex Field
<a id="edit-regex-field"></a>
- [airlock-allowlisting-json-app-activity-success-task](CodeChanges/airlock-allowlisting-json-app-activity-success-task.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20airlock-allowlisting-json-app-activity-success-task&type=code)
- [amazon-awscloudtrail-json-app-activity-awsapicall](CodeChanges/amazon-awscloudtrail-json-app-activity-awsapicall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-app-activity-awsapicall&type=code)
- [amazon-awscloudtrail-json-app-activity-getscreenshot](CodeChanges/amazon-awscloudtrail-json-app-activity-getscreenshot.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-app-activity-getscreenshot&type=code)
- [amazon-awscloudtrail-json-app-activity-loginprofile](CodeChanges/amazon-awscloudtrail-json-app-activity-loginprofile.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-app-activity-loginprofile&type=code)
- [amazon-awscloudtrail-json-app-activity-sendcommand](CodeChanges/amazon-awscloudtrail-json-app-activity-sendcommand.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-app-activity-sendcommand&type=code)
- [amazon-awscloudtrail-json-app-activity-success-awsconsoleaction](CodeChanges/amazon-awscloudtrail-json-app-activity-success-awsconsoleaction.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-app-activity-success-awsconsoleaction&type=code)
- [amazon-awscloudtrail-json-app-activity-updateprofile](CodeChanges/amazon-awscloudtrail-json-app-activity-updateprofile.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-app-activity-updateprofile&type=code)
- [amazon-awscloudtrail-json-app-login-awsconsolesignin](CodeChanges/amazon-awscloudtrail-json-app-login-awsconsolesignin.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-app-login-awsconsolesignin&type=code)
- [amazon-awscloudtrail-json-aws-login-consolelogin](CodeChanges/amazon-awscloudtrail-json-aws-login-consolelogin.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-aws-login-consolelogin&type=code)
- [amazon-awscloudtrail-json-bucket-accessblock-modify-awsapicall](CodeChanges/amazon-awscloudtrail-json-bucket-accessblock-modify-awsapicall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-bucket-accessblock-modify-awsapicall&type=code)
- [amazon-awscloudtrail-json-bucket-create-awsapicall](CodeChanges/amazon-awscloudtrail-json-bucket-create-awsapicall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-bucket-create-awsapicall&type=code)
- [amazon-awscloudtrail-json-bucket-list-success-listbucket](CodeChanges/amazon-awscloudtrail-json-bucket-list-success-listbucket.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-bucket-list-success-listbucket&type=code)
- [amazon-awscloudtrail-json-bucket-permission-modify-putbucketacl](CodeChanges/amazon-awscloudtrail-json-bucket-permission-modify-putbucketacl.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-bucket-permission-modify-putbucketacl&type=code)
- [amazon-awscloudtrail-json-bucket-permission-modify-putbucketcors](CodeChanges/amazon-awscloudtrail-json-bucket-permission-modify-putbucketcors.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-bucket-permission-modify-putbucketcors&type=code)
- [amazon-awscloudtrail-json-bucket-permission-modify-putobjectacl](CodeChanges/amazon-awscloudtrail-json-bucket-permission-modify-putobjectacl.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-bucket-permission-modify-putobjectacl&type=code)
- [amazon-awscloudtrail-json-bucket-policy-modify-putbucketpolicy](CodeChanges/amazon-awscloudtrail-json-bucket-policy-modify-putbucketpolicy.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-bucket-policy-modify-putbucketpolicy&type=code)
- [amazon-awscloudtrail-json-configuration-modify-success-putcomplianceitems](CodeChanges/amazon-awscloudtrail-json-configuration-modify-success-putcomplianceitems.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-configuration-modify-success-putcomplianceitems&type=code)
- [amazon-awscloudtrail-json-configuration-modify-success-putinventory](CodeChanges/amazon-awscloudtrail-json-configuration-modify-success-putinventory.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-configuration-modify-success-putinventory&type=code)
- [amazon-awscloudtrail-json-configuration-modify-success-updateinstanceassociationstatus](CodeChanges/amazon-awscloudtrail-json-configuration-modify-success-updateinstanceassociationstatus.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-configuration-modify-success-updateinstanceassociationstatus&type=code)
- [amazon-awscloudtrail-json-configuration-modify-success-updatestack](CodeChanges/amazon-awscloudtrail-json-configuration-modify-success-updatestack.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-configuration-modify-success-updatestack&type=code)
- [amazon-awscloudtrail-json-disk-attach-attachvolume](CodeChanges/amazon-awscloudtrail-json-disk-attach-attachvolume.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-disk-attach-attachvolume&type=code)
- [amazon-awscloudtrail-json-disk-create-createvolume](CodeChanges/amazon-awscloudtrail-json-disk-create-createvolume.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-disk-create-createvolume&type=code)
- [amazon-awscloudtrail-json-disk-modify-modifyvolume](CodeChanges/amazon-awscloudtrail-json-disk-modify-modifyvolume.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-disk-modify-modifyvolume&type=code)
- [amazon-awscloudtrail-json-endpoint-create-runinstances](CodeChanges/amazon-awscloudtrail-json-endpoint-create-runinstances.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-endpoint-create-runinstances&type=code)
- [amazon-awscloudtrail-json-endpoint-login-sendsshkey](CodeChanges/amazon-awscloudtrail-json-endpoint-login-sendsshkey.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-endpoint-login-sendsshkey&type=code)
- [amazon-awscloudtrail-json-endpoint-modify-instanceattribute](CodeChanges/amazon-awscloudtrail-json-endpoint-modify-instanceattribute.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-endpoint-modify-instanceattribute&type=code)
- [amazon-awscloudtrail-json-file-copy-copyobject](CodeChanges/amazon-awscloudtrail-json-file-copy-copyobject.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-file-copy-copyobject&type=code)
- [amazon-awscloudtrail-json-file-read-getobject](CodeChanges/amazon-awscloudtrail-json-file-read-getobject.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-file-read-getobject&type=code)
- [amazon-awscloudtrail-json-file-write-putobject](CodeChanges/amazon-awscloudtrail-json-file-write-putobject.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-file-write-putobject&type=code)
- [amazon-awscloudtrail-json-function-write-createfunction](CodeChanges/amazon-awscloudtrail-json-function-write-createfunction.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-function-write-createfunction&type=code)
- [amazon-awscloudtrail-json-function-write-updateconfiguration](CodeChanges/amazon-awscloudtrail-json-function-write-updateconfiguration.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-function-write-updateconfiguration&type=code)
- [amazon-awscloudtrail-json-function-write-updatefunction](CodeChanges/amazon-awscloudtrail-json-function-write-updatefunction.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-function-write-updatefunction&type=code)
- [amazon-awscloudtrail-json-group-member-add-addusertogroup](CodeChanges/amazon-awscloudtrail-json-group-member-add-addusertogroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-group-member-add-addusertogroup&type=code)
- [amazon-awscloudtrail-json-group-policy-attach-success-attachgrouppolicy](CodeChanges/amazon-awscloudtrail-json-group-policy-attach-success-attachgrouppolicy.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-group-policy-attach-success-attachgrouppolicy&type=code)
- [amazon-awscloudtrail-json-image-create-awsapicall](CodeChanges/amazon-awscloudtrail-json-image-create-awsapicall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-image-create-awsapicall&type=code)
- [amazon-awscloudtrail-json-image-modify-imageattribute](CodeChanges/amazon-awscloudtrail-json-image-modify-imageattribute.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-image-modify-imageattribute&type=code)
- [amazon-awscloudtrail-json-key-read-getpassword](CodeChanges/amazon-awscloudtrail-json-key-read-getpassword.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-key-read-getpassword&type=code)
- [amazon-awscloudtrail-json-key-write-createkeypair](CodeChanges/amazon-awscloudtrail-json-key-write-createkeypair.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-key-write-createkeypair&type=code)
- [amazon-awscloudtrail-json-policy-create-success-createpolicy](CodeChanges/amazon-awscloudtrail-json-policy-create-success-createpolicy.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-policy-create-success-createpolicy&type=code)
- [amazon-awscloudtrail-json-policy-create-success-putgrouppolicy](CodeChanges/amazon-awscloudtrail-json-policy-create-success-putgrouppolicy.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-policy-create-success-putgrouppolicy&type=code)
- [amazon-awscloudtrail-json-policy-create-success-putrolepolicy](CodeChanges/amazon-awscloudtrail-json-policy-create-success-putrolepolicy.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-policy-create-success-putrolepolicy&type=code)
- [amazon-awscloudtrail-json-policy-create-success-putuserpolicy](CodeChanges/amazon-awscloudtrail-json-policy-create-success-putuserpolicy.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-policy-create-success-putuserpolicy&type=code)
- [amazon-awscloudtrail-json-policy-list-success-grouppolicies](CodeChanges/amazon-awscloudtrail-json-policy-list-success-grouppolicies.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-policy-list-success-grouppolicies&type=code)
- [amazon-awscloudtrail-json-policy-list-success-listgrouppolicies](CodeChanges/amazon-awscloudtrail-json-policy-list-success-listgrouppolicies.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-policy-list-success-listgrouppolicies&type=code)
- [amazon-awscloudtrail-json-policy-list-success-listrolepolicies](CodeChanges/amazon-awscloudtrail-json-policy-list-success-listrolepolicies.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-policy-list-success-listrolepolicies&type=code)
- [amazon-awscloudtrail-json-policy-list-success-listuserpolicies](CodeChanges/amazon-awscloudtrail-json-policy-list-success-listuserpolicies.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-policy-list-success-listuserpolicies&type=code)
- [amazon-awscloudtrail-json-policy-list-success-rolepolicies](CodeChanges/amazon-awscloudtrail-json-policy-list-success-rolepolicies.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-policy-list-success-rolepolicies&type=code)
- [amazon-awscloudtrail-json-policy-list-success-userpolicies](CodeChanges/amazon-awscloudtrail-json-policy-list-success-userpolicies.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-policy-list-success-userpolicies&type=code)
- [amazon-awscloudtrail-json-policy-modify-success-createpolicyversion](CodeChanges/amazon-awscloudtrail-json-policy-modify-success-createpolicyversion.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-policy-modify-success-createpolicyversion&type=code)
- [amazon-awscloudtrail-json-policy-modify-success-setpolicyversion](CodeChanges/amazon-awscloudtrail-json-policy-modify-success-setpolicyversion.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-policy-modify-success-setpolicyversion&type=code)
- [amazon-awscloudtrail-json-policy-modify-success-updateassumerolepolicy](CodeChanges/amazon-awscloudtrail-json-policy-modify-success-updateassumerolepolicy.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-policy-modify-success-updateassumerolepolicy&type=code)
- [amazon-awscloudtrail-json-role-assume-renewrole](CodeChanges/amazon-awscloudtrail-json-role-assume-renewrole.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-role-assume-renewrole&type=code)
- [amazon-awscloudtrail-json-role-assume-success-assumerole](CodeChanges/amazon-awscloudtrail-json-role-assume-success-assumerole.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-role-assume-success-assumerole&type=code)
- [amazon-awscloudtrail-json-role-assume-success-switchrole](CodeChanges/amazon-awscloudtrail-json-role-assume-success-switchrole.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-role-assume-success-switchrole&type=code)
- [amazon-awscloudtrail-json-role-create-success-createrole](CodeChanges/amazon-awscloudtrail-json-role-create-success-createrole.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-role-create-success-createrole&type=code)
- [amazon-awscloudtrail-json-role-policy-attach-success-attachrolepolicy](CodeChanges/amazon-awscloudtrail-json-role-policy-attach-success-attachrolepolicy.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-role-policy-attach-success-attachrolepolicy&type=code)
- [amazon-awscloudtrail-json-snapshot-create-awsapicall](CodeChanges/amazon-awscloudtrail-json-snapshot-create-awsapicall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-snapshot-create-awsapicall&type=code)
- [amazon-awscloudtrail-json-snapshot-modify-awsapicall](CodeChanges/amazon-awscloudtrail-json-snapshot-modify-awsapicall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-snapshot-modify-awsapicall&type=code)
- [amazon-awscloudtrail-json-user-create-awsapicall](CodeChanges/amazon-awscloudtrail-json-user-create-awsapicall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-user-create-awsapicall&type=code)
- [amazon-awscloudtrail-json-user-create-creategroup](CodeChanges/amazon-awscloudtrail-json-user-create-creategroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-user-create-creategroup&type=code)
- [amazon-awscloudtrail-json-user-key-create-createaccesskey](CodeChanges/amazon-awscloudtrail-json-user-key-create-createaccesskey.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-user-key-create-createaccesskey&type=code)
- [amazon-awscloudtrail-json-user-policy-attach-success-attachuserpolicy](CodeChanges/amazon-awscloudtrail-json-user-policy-attach-success-attachuserpolicy.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-user-policy-attach-success-attachuserpolicy&type=code)
- [amazon-awscloudtrail-sk4-app-activity-aws](CodeChanges/amazon-awscloudtrail-sk4-app-activity-aws.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-sk4-app-activity-aws&type=code)
- [amazon-awscloudtrail-sk4-app-activity-success-backupjobstarted](CodeChanges/amazon-awscloudtrail-sk4-app-activity-success-backupjobstarted.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-sk4-app-activity-success-backupjobstarted&type=code)
- [amazon-awscloudtrail-sk4-app-activity-success-redshift](CodeChanges/amazon-awscloudtrail-sk4-app-activity-success-redshift.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-sk4-app-activity-success-redshift&type=code)
- [amazon-awscloudtrail-sk4-snapshot-create-success-sharedsnapshotvolumecreated](CodeChanges/amazon-awscloudtrail-sk4-snapshot-create-success-sharedsnapshotvolumecreated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-sk4-snapshot-create-success-sharedsnapshotvolumecreated&type=code)
- [amazon-awscloudtrail-sk4-user-token-create-success-tokenpost](CodeChanges/amazon-awscloudtrail-sk4-user-token-create-success-tokenpost.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-sk4-user-token-create-success-tokenpost&type=code)
- [amazon-awsguardduty-cef-alert-trigger-success-catsecurity](CodeChanges/amazon-awsguardduty-cef-alert-trigger-success-catsecurity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awsguardduty-cef-alert-trigger-success-catsecurity&type=code)
- [amazon-awsguardduty-json-alert-trigger-success-catchall](CodeChanges/amazon-awsguardduty-json-alert-trigger-success-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awsguardduty-json-alert-trigger-success-catchall&type=code)
- [amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod](CodeChanges/amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod&type=code)
- [amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport](CodeChanges/amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport&type=code)
- [amazon-awsguardduty-json-alert-trigger-success-sshbruteforce](CodeChanges/amazon-awsguardduty-json-alert-trigger-success-sshbruteforce.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awsguardduty-json-alert-trigger-success-sshbruteforce&type=code)
- [amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin](CodeChanges/amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin&type=code)
- [amazon-awsguardduty-json-database-login-success-rdssuccessfullogin](CodeChanges/amazon-awsguardduty-json-database-login-success-rdssuccessfullogin.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awsguardduty-json-database-login-success-rdssuccessfullogin&type=code)
- [amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior](CodeChanges/amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior&type=code)
- [amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled](CodeChanges/amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled&type=code)
- [amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1](CodeChanges/amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1&type=code)
- [amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2](CodeChanges/amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2&type=code)
- [amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage](CodeChanges/amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage&type=code)
- [amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1](CodeChanges/amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1&type=code)
- [amazon-awsguardduty-sk4-alert-trigger-success-toripcaller](CodeChanges/amazon-awsguardduty-sk4-alert-trigger-success-toripcaller.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awsguardduty-sk4-alert-trigger-success-toripcaller&type=code)
- [auth0-a-json-app-activity-success-catchall](CodeChanges/auth0-a-json-app-activity-success-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-app-activity-success-catchall&type=code)
- [auth0-a-json-app-authentication-fail-gd_auth_failed](CodeChanges/auth0-a-json-app-authentication-fail-gd_auth_failed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-app-authentication-fail-gd_auth_failed&type=code)
- [auth0-a-json-app-authentication-fail-warning](CodeChanges/auth0-a-json-app-authentication-fail-warning.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-app-authentication-fail-warning&type=code)
- [auth0-a-json-app-authentication-success-gd_auth_succeed](CodeChanges/auth0-a-json-app-authentication-success-gd_auth_succeed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-app-authentication-success-gd_auth_succeed&type=code)
- [auth0-a-json-app-authentication-success-startauth](CodeChanges/auth0-a-json-app-authentication-success-startauth.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-app-authentication-success-startauth&type=code)
- [auth0-a-json-app-login-fail-apilimit](CodeChanges/auth0-a-json-app-login-fail-apilimit.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-app-login-fail-apilimit&type=code)
- [auth0-a-json-app-login-fail-fcpr](CodeChanges/auth0-a-json-app-login-fail-fcpr.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-app-login-fail-fcpr&type=code)
- [auth0-a-json-app-login-fail-fu](CodeChanges/auth0-a-json-app-login-fail-fu.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-app-login-fail-fu&type=code)
- [auth0-a-json-app-login-fail-limitwc](CodeChanges/auth0-a-json-app-login-fail-limitwc.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-app-login-fail-limitwc&type=code)
- [auth0-a-json-app-login-success-changeemail](CodeChanges/auth0-a-json-app-login-success-changeemail.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-app-login-success-changeemail&type=code)
- [auth0-a-json-app-login-success-s](CodeChanges/auth0-a-json-app-login-success-s.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-app-login-success-s&type=code)
- [auth0-a-json-app-login-success-seacft](CodeChanges/auth0-a-json-app-login-success-seacft.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-app-login-success-seacft&type=code)
- [auth0-a-json-app-login-success-seccft](CodeChanges/auth0-a-json-app-login-success-seccft.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-app-login-success-seccft&type=code)
- [auth0-a-json-app-login-success-ss](CodeChanges/auth0-a-json-app-login-success-ss.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-app-login-success-ss&type=code)
- [auth0-a-json-app-login-success-ssa](CodeChanges/auth0-a-json-app-login-success-ssa.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-app-login-success-ssa&type=code)
- [auth0-a-json-app-logout-fail-flo](CodeChanges/auth0-a-json-app-logout-fail-flo.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-app-logout-fail-flo&type=code)
- [auth0-a-json-app-logout-success-slo](CodeChanges/auth0-a-json-app-logout-success-slo.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-app-logout-success-slo&type=code)
- [auth0-a-json-configuration-modify-success-gd_tenant_update](CodeChanges/auth0-a-json-configuration-modify-success-gd_tenant_update.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-configuration-modify-success-gd_tenant_update&type=code)
- [auth0-a-json-endpoint-login-success-exchange](CodeChanges/auth0-a-json-endpoint-login-success-exchange.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-endpoint-login-success-exchange&type=code)
- [auth0-a-json-endpoint-login-success-verification](CodeChanges/auth0-a-json-endpoint-login-success-verification.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-endpoint-login-success-verification&type=code)
- [auth0-a-json-http-session-success-mgmt_api_read](CodeChanges/auth0-a-json-http-session-success-mgmt_api_read.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-http-session-success-mgmt_api_read&type=code)
- [auth0-a-json-http-session-success-sapi](CodeChanges/auth0-a-json-http-session-success-sapi.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-http-session-success-sapi&type=code)
- [auth0-a-json-user-delete-success-userdeletion](CodeChanges/auth0-a-json-user-delete-success-userdeletion.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-user-delete-success-userdeletion&type=code)
- [auth0-a-json-user-password-modify-fail-fcp](CodeChanges/auth0-a-json-user-password-modify-fail-fcp.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-user-password-modify-fail-fcp&type=code)
- [auth0-a-json-user-password-modify-success-changepassword](CodeChanges/auth0-a-json-user-password-modify-success-changepassword.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-user-password-modify-success-changepassword&type=code)
- [azure-azuread-json-app-activity-updateserviceprincipal](CodeChanges/azure-azuread-json-app-activity-updateserviceprincipal.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-app-activity-updateserviceprincipal&type=code)
- [google-cloudplatform-json-http-session-httploadbalancer](CodeChanges/google-cloudplatform-json-http-session-httploadbalancer.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20google-cloudplatform-json-http-session-httploadbalancer&type=code)
- [microsoft-evsecurity-json-audit-policy-modify-success-5449](CodeChanges/microsoft-evsecurity-json-audit-policy-modify-success-5449.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-audit-policy-modify-success-5449&type=code)
- [microsoft-evsecurity-json-endpoint-activity-success-4691](CodeChanges/microsoft-evsecurity-json-endpoint-activity-success-4691.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-endpoint-activity-success-4691&type=code)
- [microsoft-evsecurity-json-endpoint-activity-success-catchall](CodeChanges/microsoft-evsecurity-json-endpoint-activity-success-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-endpoint-activity-success-catchall&type=code)
- [microsoft-evsecurity-json-share-modify-success-5143](CodeChanges/microsoft-evsecurity-json-share-modify-success-5143.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-share-modify-success-5143&type=code)
- [microsoft-evsecurity-kv-endpoint-login-fail-4625-2](CodeChanges/microsoft-evsecurity-kv-endpoint-login-fail-4625-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-fail-4625-2&type=code)
- [microsoft-evsecurity-kv-file-permission-modify-4670](CodeChanges/microsoft-evsecurity-kv-file-permission-modify-4670.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-file-permission-modify-4670&type=code)
- [microsoft-evsecurity-kv-group-list-membershipenumerated](CodeChanges/microsoft-evsecurity-kv-group-list-membershipenumerated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-group-list-membershipenumerated&type=code)
- [microsoft-evsecurity-kv-group-member-list-4799](CodeChanges/microsoft-evsecurity-kv-group-member-list-4799.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-group-member-list-4799&type=code)
- [microsoft-evsecurity-kv-handle-request-4656-2](CodeChanges/microsoft-evsecurity-kv-handle-request-4656-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-handle-request-4656-2&type=code)
- [microsoft-evsecurity-kv-process-create-success-created-1](CodeChanges/microsoft-evsecurity-kv-process-create-success-created-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-process-create-success-created-1&type=code)
- [microsoft-evsecurity-kv-user-privilege-use-success-4674-1](CodeChanges/microsoft-evsecurity-kv-user-privilege-use-success-4674-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-user-privilege-use-success-4674-1&type=code)
- [microsoft-evsecurity-mix-share-access-success-5140-1](CodeChanges/microsoft-evsecurity-mix-share-access-success-5140-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-share-access-success-5140-1&type=code)
- [microsoft-o365-sk4-app-file-operationworkload](CodeChanges/microsoft-o365-sk4-app-file-operationworkload.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-sk4-app-file-operationworkload&type=code)

#### Removed Parser
<a id="removed-parser"></a>
- [thoughtspot-ts-json-app-activity-success-answer](CodeChanges/thoughtspot-ts-json-app-activity-success-answer.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20thoughtspot-ts-json-app-activity-success-answer&type=code)

</details>

<details>
<summary><strong id="parsertemplate">ParserTemplate (9)</strong></summary>


### Change Types
- [Added Parser Template](#added-parser-template)
- [Changed Parsed Fields](#changed-parsed-fields)
- [Edit Regex Field](#edit-regex-field)
- [Removed Parser Template](#removed-parser-template)

#### Added Parser Template
<a id="added-parser-template"></a>
- [postgresql-parser-str-1](CodeChanges/postgresql-parser-str-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20postgresql-parser-str-1&type=code)

#### Changed Parsed Fields
<a id="changed-parsed-fields"></a>
- [Microsoft-CAS-Event-Category](CodeChanges/Microsoft-CAS-Event-Category.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20Microsoft-CAS-Event-Category&type=code)
- [microsoft-azuread-json-events](CodeChanges/microsoft-azuread-json-events.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuread-json-events&type=code)
- [microsoft-json-events](CodeChanges/microsoft-json-events.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-json-events&type=code)

#### Edit Regex Field
<a id="edit-regex-field"></a>
- [auth0-authentication-template](CodeChanges/auth0-authentication-template.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-authentication-template&type=code)
- [aws-cloudtrail-json](CodeChanges/aws-cloudtrail-json.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20aws-cloudtrail-json&type=code)
- [aws-cloudtrail-user-template](CodeChanges/aws-cloudtrail-user-template.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20aws-cloudtrail-user-template&type=code)
- [json-aws-guardduty-security-alert-template](CodeChanges/json-aws-guardduty-security-alert-template.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20json-aws-guardduty-security-alert-template&type=code)

#### Removed Parser Template
<a id="removed-parser-template"></a>
- [dl-wazuh-windows-template](CodeChanges/dl-wazuh-windows-template.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20dl-wazuh-windows-template&type=code)

</details>