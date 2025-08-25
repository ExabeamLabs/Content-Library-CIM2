# Content Package 2025.15.1

These release notes contain information about content package 2025.15.1, released on 23 Jul 2025.

## Enhancements
- Added support for Claroty new format logs.
- Updated conditions of a few OOTB parsers to parse broader category of Microsoft Defender logs
- Fixed the field parsing issues with microsoft-evadfs-xml-ds-object-delete-success-4929 parser.
- Updated netskope-webtx-json-network-traffic-ipsecnetworksecurity parser conditions to accommodate new format Netskope logs.
- Updated the field extraction for below parsers. List of parsers and field extraction mentioned below microsoft-evsecurity-json-endpoint-4624	time, event_id, result microsoft-evsecurity-json-endpoint-login-4776 time, host, result_code, event_id, result microsoft-evsecurity-mix-user-privilege-assign-success-4673  time, dest_host, host microsoft-evsecurity-mix-user-privilege-use-success-4674-1   src_ip, src_mac, host
- Added new parser for Monday.com logs
- Created the parser for OpenAI audit logs.
- Added support for Qualys new format logs.
- Developed new parser content for Github logs
- Added default content support for new vendor - Zyxel.

## Addressed Issues
- Added url field parsing support for fortinet-fortigate-kv-network-traffic-logid and several other Fortinet parsers.
- Fixed parsing for fields user , dest_user , and src_user in the pan-ngfw-mix-alert-trigger-success-threadvulnerability parser.
- Updated categories, web_domain field extractions for the parser: pan-ngfw-csv-http-session-9999.
- Fixed the result field parsing and appropriate event building issue with Azure parser.
- Updated severity field extractions for parser okta-amfa-mix-app-login-success-securitycontext
- Categorized result = LogonAttempt events to endpoint-notification:success instead of endpoint-login:fail .
- Updated regexes of following fields - correlation_id,object,resource,resource_id,tenant_id in parser microsoft-azuremon-sk4-app-activity-policy.
- Filter exact 19-digit strings from mapping to aws_user for amazon-awscloudtrail-json-app-activity-awsapicall parser
- Updated parser 'microsoft-o365-cef-app-file-success-displayname' to lower priority so that it does not interfere with the logs of other parsers.
- Fix the event builder syntax issue of CrowdStrike and Zscaler .
- Created new parser to support wiz unparsed logs .Parser Name : wiz-w-json-app-activity-success-fail-wiz.
- Update the parser 'microsoft-o365-sk4-file-app-userkey' with new field extraction and EB with 'usb-write'
- Updated src_user and target field extractions for parser - okta-amfa-mix-app-login-success-securitycontext
- Updated regex of process_name in parser - sentinelone-singularityp-json-alert-trigger-success-datasourcecategorysecurity by eliminating the .+? at the beginning.
- Updated the below parsers to extract event_code, event_name,host 'microsoft-evsecurity-json-ds-object-modify-success-5136' 'microsoft-evsecurity-mix-user-lock-success-4740' 'microsoft-evsecurity-kv-endpoint-login-4768-2' 'microsoft-evsecurity-kv-endpoint-login-4769-2' 'microsoft-evapp-json-endpoint-activity-success-catchall'
- Added support for Veeam new format logs
- Updated user field extractions for parsers: exabeam-aa-kv-rule-trigger-success-anomaly, exabeam-aa-kv-rule-trigger-success-anomaly-1.

## Code Changes
### Overview
- **Event Builder**: 66 changes
- **Parser**: 351 changes
- **ParserTemplate**: 11 changes

### ℹ️ How to Read This Document

Each item listed under **Code Changes** includes:

- **A link to a detailed change file**  
  Click the filename to see full table.

- **A search icon 🔍**  
  Click 🔍 to search in the [Exabeam Content Library](https://github.com/ExabeamLabs/Content-Library-CIM2).


<details>
<summary><strong id="event-builder">Event Builder (66)</strong></summary>


### Change Types
- [Added Event Builder](#added-event-builder)
- [Edit Conditions](#edit-conditions)
- [Removed Event Builder](#removed-event-builder)

#### Added Event Builder
<a id="added-event-builder"></a>
- [dl-qualys-q-app-logout-success](CodeChanges/dl-qualys-q-app-logout-success.md)
- [dl-sentinelone-linux-alert-trigger-success](CodeChanges/dl-sentinelone-linux-alert-trigger-success.md)
- [dl-sentinelone-macos-alert-trigger-success](CodeChanges/dl-sentinelone-macos-alert-trigger-success.md)
- [dl-zyxel-network-network-notification-success](CodeChanges/dl-zyxel-network-network-notification-success.md)
- [github-app-activity-success-3](CodeChanges/github-app-activity-success-3.md)
- [github-branch-create-success-1](CodeChanges/github-branch-create-success-1.md)
- [github-branch-modify-success-1](CodeChanges/github-branch-modify-success-1.md)
- [github-repository-member-add-success-1](CodeChanges/github-repository-member-add-success-1.md)
- [github-repository-member-remove-success](CodeChanges/github-repository-member-remove-success.md)
- [microsoft-365-app-activity-success-16](CodeChanges/microsoft-365-app-activity-success-16.md)
- [microsoft-365-file-create-success-1](CodeChanges/microsoft-365-file-create-success-1.md)
- [microsoft-365-user-password-modify-fail](CodeChanges/microsoft-365-user-password-modify-fail.md)
- [microsoft-365-user-password-modify-success-1](CodeChanges/microsoft-365-user-password-modify-success-1.md)
- [microsoft-azure-file-create-success](CodeChanges/microsoft-azure-file-create-success.md)
- [microsoft-azure-file-delete-success](CodeChanges/microsoft-azure-file-delete-success.md)
- [microsoft-azure-file-read-success-3](CodeChanges/microsoft-azure-file-read-success-3.md)
- [microsoft-azure-file-write-success-2](CodeChanges/microsoft-azure-file-write-success-2.md)
- [microsoft-azure-process-create-success](CodeChanges/microsoft-azure-process-create-success.md)
- [microsoft-azuread-group-member-add-success-1](CodeChanges/microsoft-azuread-group-member-add-success-1.md)
- [microsoft-windows-endpoint-notification-success-1](CodeChanges/microsoft-windows-endpoint-notification-success-1.md)
- [openai-oai-app-activity-success](CodeChanges/openai-oai-app-activity-success.md)
- [openai-oai-app-login-success](CodeChanges/openai-oai-app-login-success.md)
- [openai-oai-configuration-modify-success](CodeChanges/openai-oai-configuration-modify-success.md)
- [qualys-q-app-activity-success](CodeChanges/qualys-q-app-activity-success.md)
- [qualys-q-app-login-success](CodeChanges/qualys-q-app-login-success.md)
- [wiz-app-activity-fail](CodeChanges/wiz-app-activity-fail.md)
- [wiz-app-activity-success](CodeChanges/wiz-app-activity-success.md)
- [wiz-user-create-fail](CodeChanges/wiz-user-create-fail.md)
- [wiz-user-create-success](CodeChanges/wiz-user-create-success.md)
- [wiz-user-delete-fail](CodeChanges/wiz-user-delete-fail.md)
- [wiz-user-delete-success](CodeChanges/wiz-user-delete-success.md)
- [zyxel-network-network-session-fail](CodeChanges/zyxel-network-network-session-fail.md)
- [zyxel-network-network-traffic-success](CodeChanges/zyxel-network-network-traffic-success.md)
- [zyxel-usg-alert-trigger-success](CodeChanges/zyxel-usg-alert-trigger-success.md)

#### Edit Conditions
<a id="edit-conditions"></a>
- [crowdstrike-falcon-app-activity-fail-win-1](CodeChanges/crowdstrike-falcon-app-activity-fail-win-1.md)
- [github-repository-modify-success-1](CodeChanges/github-repository-modify-success-1.md)
- [microsoft-365-app-activity-fail](CodeChanges/microsoft-365-app-activity-fail.md)
- [microsoft-365-app-activity-success-2](CodeChanges/microsoft-365-app-activity-success-2.md)
- [microsoft-windows-endpoint-login-fail-5](CodeChanges/microsoft-windows-endpoint-login-fail-5.md)
- [zscaler-internetaccess-app-login-success](CodeChanges/zscaler-internetaccess-app-login-success.md)

#### Removed Event Builder
<a id="removed-event-builder"></a>
- [cisco-acs-endpoint-authentication-success](CodeChanges/cisco-acs-endpoint-authentication-success.md)
- [cisco-duo-endpoint-authentication-fail-2](CodeChanges/cisco-duo-endpoint-authentication-fail-2.md)
- [cisco-duo-endpoint-authentication-success-2](CodeChanges/cisco-duo-endpoint-authentication-success-2.md)
- [cisco-duoaccess-app-login-success](CodeChanges/cisco-duoaccess-app-login-success.md)
- [cisco-iam-vpn-logout-success-1](CodeChanges/cisco-iam-vpn-logout-success-1.md)
- [cisco-network-http-session-fail-12](CodeChanges/cisco-network-http-session-fail-12.md)
- [cisco-network-http-session-fail-3](CodeChanges/cisco-network-http-session-fail-3.md)
- [cisco-network-http-session-success-14](CodeChanges/cisco-network-http-session-success-14.md)
- [cisco-network-http-session-success-4](CodeChanges/cisco-network-http-session-success-4.md)
- [cisco-unifiedcm-app-activity-fail](CodeChanges/cisco-unifiedcm-app-activity-fail.md)
- [cisco-unifiedcm-app-activity-success](CodeChanges/cisco-unifiedcm-app-activity-success.md)
- [cisco-unix-process-create-success](CodeChanges/cisco-unix-process-create-success.md)
- [citrix-network-http-session-fail](CodeChanges/citrix-network-http-session-fail.md)
- [clearsense-app-activity-success](CodeChanges/clearsense-app-activity-success.md)
- [code42-peripheral-storage-activity-success](CodeChanges/code42-peripheral-storage-activity-success.md)
- [code42-peripheral-storage-insert-success](CodeChanges/code42-peripheral-storage-insert-success.md)
- [code42-windows-file-download-success](CodeChanges/code42-windows-file-download-success.md)
- [code42-windows-file-upload-success](CodeChanges/code42-windows-file-upload-success.md)
- [contrastsecurity-alert-trigger-success](CodeChanges/contrastsecurity-alert-trigger-success.md)
- [dl-cisco-unifiedcm-configuration-modify-success](CodeChanges/dl-cisco-unifiedcm-configuration-modify-success.md)
- [dl-cisco-unifiedcm-user-role-modify-success](CodeChanges/dl-cisco-unifiedcm-user-role-modify-success.md)
- [dl-citrix-gateway-app-activity-success-1](CodeChanges/dl-citrix-gateway-app-activity-success-1.md)
- [dl-citrix-network-app-authentication-success](CodeChanges/dl-citrix-network-app-authentication-success.md)
- [dl-citrix-network-network-notification-success](CodeChanges/dl-citrix-network-network-notification-success.md)
- [dl-cloudfare-network-http-request-success](CodeChanges/dl-cloudfare-network-http-request-success.md)
- [dl-contrastsecurity-alert-trigger-success](CodeChanges/dl-contrastsecurity-alert-trigger-success.md)

</details>

<details>
<summary><strong id="parser">Parser (351)</strong></summary>


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
- [wiz-w-json-app-activity-success-cloudaccountswithcomplianceanalytics](CodeChanges/wiz-w-json-app-activity-success-cloudaccountswithcomplianceanalytics.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20wiz-w-json-app-activity-success-cloudaccountswithcomplianceanalytics&type=code)
- [wiz-w-json-app-activity-success-createissuenote](CodeChanges/wiz-w-json-app-activity-success-createissuenote.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20wiz-w-json-app-activity-success-createissuenote&type=code)
- [wiz-w-json-app-activity-success-osbenchmarks](CodeChanges/wiz-w-json-app-activity-success-osbenchmarks.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20wiz-w-json-app-activity-success-osbenchmarks&type=code)
- [wiz-w-json-app-activity-success-systemactivities](CodeChanges/wiz-w-json-app-activity-success-systemactivities.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20wiz-w-json-app-activity-success-systemactivities&type=code)
- [wiz-w-json-app-activity-success-updateissue](CodeChanges/wiz-w-json-app-activity-success-updateissue.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20wiz-w-json-app-activity-success-updateissue&type=code)
- [wiz-w-json-app-activity-success-user](CodeChanges/wiz-w-json-app-activity-success-user.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20wiz-w-json-app-activity-success-user&type=code)
- [wiz-w-json-app-login-success-fail-login](CodeChanges/wiz-w-json-app-login-success-fail-login.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20wiz-w-json-app-login-success-fail-login&type=code)
- [wiz-w-json-app-scan-success-finalizecicdscan](CodeChanges/wiz-w-json-app-scan-success-finalizecicdscan.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20wiz-w-json-app-scan-success-finalizecicdscan&type=code)
- [wiz-w-json-app-scan-success-initiateiacscan](CodeChanges/wiz-w-json-app-scan-success-initiateiacscan.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20wiz-w-json-app-scan-success-initiateiacscan&type=code)
- [wiz-w-json-disk-scan-success-diskscan](CodeChanges/wiz-w-json-disk-scan-success-diskscan.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20wiz-w-json-disk-scan-success-diskscan&type=code)
- [wiz-w-json-disk-scan-success-initiatediskscancontainerimage](CodeChanges/wiz-w-json-disk-scan-success-initiatediskscancontainerimage.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20wiz-w-json-disk-scan-success-initiatediskscancontainerimage&type=code)
- [wiz-w-json-report-create-success-reportcreate](CodeChanges/wiz-w-json-report-create-success-reportcreate.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20wiz-w-json-report-create-success-reportcreate&type=code)
- [wiz-w-json-report-delete-success-deletereport](CodeChanges/wiz-w-json-report-delete-success-deletereport.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20wiz-w-json-report-delete-success-deletereport&type=code)
- [wiz-w-json-report-execute-success-report](CodeChanges/wiz-w-json-report-execute-success-report.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20wiz-w-json-report-execute-success-report&type=code)
- [wiz-w-json-report-execute-success-rerunreport](CodeChanges/wiz-w-json-report-execute-success-rerunreport.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20wiz-w-json-report-execute-success-rerunreport&type=code)
- [wiz-w-json-report-execute-success-updatereport](CodeChanges/wiz-w-json-report-execute-success-updatereport.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20wiz-w-json-report-execute-success-updatereport&type=code)

#### Added Parser
<a id="added-parser"></a>
- [github-g-json-app-activity-success-action](CodeChanges/github-g-json-app-activity-success-action.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20github-g-json-app-activity-success-action&type=code)
- [github-g-json-app-notification-success-catchall](CodeChanges/github-g-json-app-notification-success-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20github-g-json-app-notification-success-catchall&type=code)
- [microsoft-azure-cef-file-read-success-actiontype](CodeChanges/microsoft-azure-cef-file-read-success-actiontype.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-cef-file-read-success-actiontype&type=code)
- [microsoft-azure-csv-rdp-traffic-success-vmid](CodeChanges/microsoft-azure-csv-rdp-traffic-success-vmid.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-csv-rdp-traffic-success-vmid&type=code)
- [microsoft-azure-json-app-login-datetime](CodeChanges/microsoft-azure-json-app-login-datetime.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-json-app-login-datetime&type=code)
- [microsoft-azure-kv-file-success-vmid](CodeChanges/microsoft-azure-kv-file-success-vmid.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-kv-file-success-vmid&type=code)
- [microsoft-azure-kv-group-member-add-success-eventhubbeat](CodeChanges/microsoft-azure-kv-group-member-add-success-eventhubbeat.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-kv-group-member-add-success-eventhubbeat&type=code)
- [microsoft-azure-kv-group-member-remove-success-deviceevents](CodeChanges/microsoft-azure-kv-group-member-remove-success-deviceevents.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-kv-group-member-remove-success-deviceevents&type=code)
- [microsoft-azure-kv-process-create-success-powershellcommand](CodeChanges/microsoft-azure-kv-process-create-success-powershellcommand.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-kv-process-create-success-powershellcommand&type=code)
- [openai-oai-json-app-activity-success-apikeycreated](CodeChanges/openai-oai-json-app-activity-success-apikeycreated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20openai-oai-json-app-activity-success-apikeycreated&type=code)
- [openai-oai-json-app-activity-success-apikeydeleted](CodeChanges/openai-oai-json-app-activity-success-apikeydeleted.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20openai-oai-json-app-activity-success-apikeydeleted&type=code)
- [openai-oai-json-app-activity-success-projectcreated](CodeChanges/openai-oai-json-app-activity-success-projectcreated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20openai-oai-json-app-activity-success-projectcreated&type=code)
- [openai-oai-json-app-login-success-loginsucceeded](CodeChanges/openai-oai-json-app-login-success-loginsucceeded.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20openai-oai-json-app-login-success-loginsucceeded&type=code)
- [openai-oai-json-configuration-modify-success-organizationupdated](CodeChanges/openai-oai-json-configuration-modify-success-organizationupdated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20openai-oai-json-configuration-modify-success-organizationupdated&type=code)
- [qualys-q-json-app-activity-success-action](CodeChanges/qualys-q-json-app-activity-success-action.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20qualys-q-json-app-activity-success-action&type=code)
- [wiz-w-json-app-activity-success-fail-wiz](CodeChanges/wiz-w-json-app-activity-success-fail-wiz.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20wiz-w-json-app-activity-success-fail-wiz&type=code)
- [zyxel-usgflex-kv-alert-trigger-success-ips](CodeChanges/zyxel-usgflex-kv-alert-trigger-success-ips.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zyxel-usgflex-kv-alert-trigger-success-ips&type=code)
- [zyxel-usgflex-kv-network-notification-success-msg](CodeChanges/zyxel-usgflex-kv-network-notification-success-msg.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zyxel-usgflex-kv-network-notification-success-msg&type=code)
- [zyxel-usgflex-kv-network-session-fail-accessblock](CodeChanges/zyxel-usgflex-kv-network-session-fail-accessblock.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zyxel-usgflex-kv-network-session-fail-accessblock&type=code)
- [zyxel-usgflex-kv-network-session-fail-sessionlimit](CodeChanges/zyxel-usgflex-kv-network-session-fail-sessionlimit.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zyxel-usgflex-kv-network-session-fail-sessionlimit&type=code)
- [zyxel-usgflex-kv-network-traffic-success-trafficlog](CodeChanges/zyxel-usgflex-kv-network-traffic-success-trafficlog.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zyxel-usgflex-kv-network-traffic-success-trafficlog&type=code)

#### Changed
<a id="changed"></a>
- [claroty-c-cef-alert-trigger-success-alertaffecteddevice](CodeChanges/claroty-c-cef-alert-trigger-success-alertaffecteddevice.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20claroty-c-cef-alert-trigger-success-alertaffecteddevice&type=code)
- [claroty-c-cef-network-notification-success-commevent](CodeChanges/claroty-c-cef-network-notification-success-commevent.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20claroty-c-cef-network-notification-success-commevent&type=code)
- [microsoft-365defender-json-endpoint-activity-success-publish-identityinfo](CodeChanges/microsoft-365defender-json-endpoint-activity-success-publish-identityinfo.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-365defender-json-endpoint-activity-success-publish-identityinfo&type=code)
- [microsoft-defenderep-cef-endpoint-login-batch](CodeChanges/microsoft-defenderep-cef-endpoint-login-batch.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-cef-endpoint-login-batch&type=code)
- [microsoft-defenderep-cef-endpoint-login-interactive](CodeChanges/microsoft-defenderep-cef-endpoint-login-interactive.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-cef-endpoint-login-interactive&type=code)
- [microsoft-defenderep-cef-endpoint-login-network](CodeChanges/microsoft-defenderep-cef-endpoint-login-network.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-cef-endpoint-login-network&type=code)
- [microsoft-defenderep-cef-endpoint-login-remoteinteractive](CodeChanges/microsoft-defenderep-cef-endpoint-login-remoteinteractive.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-cef-endpoint-login-remoteinteractive&type=code)
- [microsoft-defenderep-cef-endpoint-login-service](CodeChanges/microsoft-defenderep-cef-endpoint-login-service.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-cef-endpoint-login-service&type=code)
- [microsoft-defenderep-json-endpoint-login-identitylogonevents](CodeChanges/microsoft-defenderep-json-endpoint-login-identitylogonevents.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-json-endpoint-login-identitylogonevents&type=code)
- [microsoft-defenderep-json-network-notification-advancedhunting](CodeChanges/microsoft-defenderep-json-network-notification-advancedhunting.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-json-network-notification-advancedhunting&type=code)
- [netskope-webtx-json-network-traffic-ipsecnetworksecurity](CodeChanges/netskope-webtx-json-network-traffic-ipsecnetworksecurity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20netskope-webtx-json-network-traffic-ipsecnetworksecurity&type=code)
- [veeam-v-json-app-activity-success-eventid](CodeChanges/veeam-v-json-app-activity-success-eventid.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20veeam-v-json-app-activity-success-eventid&type=code)

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
- [azure-azuread-json-app-activity-updateserviceprincipal](CodeChanges/azure-azuread-json-app-activity-updateserviceprincipal.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-app-activity-updateserviceprincipal&type=code)
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
- [fortinet-firewall-kv-network-traffic-notice](CodeChanges/fortinet-firewall-kv-network-traffic-notice.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20fortinet-firewall-kv-network-traffic-notice&type=code)
- [fortinet-fortigate-kv-network-traffic-logid](CodeChanges/fortinet-fortigate-kv-network-traffic-logid.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20fortinet-fortigate-kv-network-traffic-logid&type=code)
- [microsoft-azure-json-app-activity-addgroup-1](CodeChanges/microsoft-azure-json-app-activity-addgroup-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-json-app-activity-addgroup-1&type=code)
- [microsoft-azure-json-app-activity-adduser](CodeChanges/microsoft-azure-json-app-activity-adduser.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-json-app-activity-adduser&type=code)
- [microsoft-azure-json-app-activity-changeuserlicense](CodeChanges/microsoft-azure-json-app-activity-changeuserlicense.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-json-app-activity-changeuserlicense&type=code)
- [microsoft-azure-json-app-activity-deleteuser](CodeChanges/microsoft-azure-json-app-activity-deleteuser.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-json-app-activity-deleteuser&type=code)
- [microsoft-azure-json-app-activity-harddeletegroup](CodeChanges/microsoft-azure-json-app-activity-harddeletegroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-json-app-activity-harddeletegroup&type=code)
- [microsoft-azure-json-group-member-remove-success-removefromgroup](CodeChanges/microsoft-azure-json-group-member-remove-success-removefromgroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-json-group-member-remove-success-removefromgroup&type=code)
- [microsoft-azuread-json-user-disable-success-accountdisable-1](CodeChanges/microsoft-azuread-json-user-disable-success-accountdisable-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuread-json-user-disable-success-accountdisable-1&type=code)
- [microsoft-azuread-json-user-password-modify-success-changepassword](CodeChanges/microsoft-azuread-json-user-password-modify-success-changepassword.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuread-json-user-password-modify-success-changepassword&type=code)
- [microsoft-evadfs-xml-ds-object-delete-success-4929](CodeChanges/microsoft-evadfs-xml-ds-object-delete-success-4929.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evadfs-xml-ds-object-delete-success-4929&type=code)
- [microsoft-evapp-json-endpoint-activity-success-catchall](CodeChanges/microsoft-evapp-json-endpoint-activity-success-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-json-endpoint-activity-success-catchall&type=code)
- [microsoft-evsecurity-json-endpoint-4624](CodeChanges/microsoft-evsecurity-json-endpoint-4624.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-endpoint-4624&type=code)
- [microsoft-evsecurity-json-peripheral-storage-insert-success-6416](CodeChanges/microsoft-evsecurity-json-peripheral-storage-insert-success-6416.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-peripheral-storage-insert-success-6416&type=code)
- [microsoft-evsecurity-mix-user-privilege-use-success-4674-1](CodeChanges/microsoft-evsecurity-mix-user-privilege-use-success-4674-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-user-privilege-use-success-4674-1&type=code)
- [microsoft-o365-json-app-activity-success-groupmanagementaddowner](CodeChanges/microsoft-o365-json-app-activity-success-groupmanagementaddowner.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-json-app-activity-success-groupmanagementaddowner&type=code)
- [microsoft-o365-json-app-file-success-inviteexternaluser](CodeChanges/microsoft-o365-json-app-file-success-inviteexternaluser.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-json-app-file-success-inviteexternaluser&type=code)
- [microsoft-o365-json-app-file-success-restoreuser](CodeChanges/microsoft-o365-json-app-file-success-restoreuser.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-json-app-file-success-restoreuser&type=code)
- [microsoft-o365-sk4-file-app-userkey](CodeChanges/microsoft-o365-sk4-file-app-userkey.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-sk4-file-app-userkey&type=code)
- [okta-amfa-mix-app-login-success-securitycontext](CodeChanges/okta-amfa-mix-app-login-success-securitycontext.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20okta-amfa-mix-app-login-success-securitycontext&type=code)

#### Edit Attribute
<a id="edit-attribute"></a>
- [azure-azuread-json-user-password-modify-success-selfservice](CodeChanges/azure-azuread-json-user-password-modify-success-selfservice.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-user-password-modify-success-selfservice&type=code)
- [microsoft-defenderep-json-file-success-advancedhuntingdevicefileevents](CodeChanges/microsoft-defenderep-json-file-success-advancedhuntingdevicefileevents.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-json-file-success-advancedhuntingdevicefileevents&type=code)
- [microsoft-o365-cef-app-file-tabadded](CodeChanges/microsoft-o365-cef-app-file-tabadded.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-tabadded&type=code)
- [microsoft-o365-cef-app-file-teams](CodeChanges/microsoft-o365-cef-app-file-teams.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-teams&type=code)
- [microsoft-o365-cef-file-accessrequestapproved](CodeChanges/microsoft-o365-cef-file-accessrequestapproved.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-file-accessrequestapproved&type=code)
- [microsoft-o365-cef-file-addtogroup](CodeChanges/microsoft-o365-cef-file-addtogroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-file-addtogroup&type=code)
- [microsoft-o365-cef-file-read-success-accessrequest](CodeChanges/microsoft-o365-cef-file-read-success-accessrequest.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-file-read-success-accessrequest&type=code)
- [microsoft-o365-cef-file-read-success-channeladd](CodeChanges/microsoft-o365-cef-file-read-success-channeladd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-file-read-success-channeladd&type=code)
- [microsoft-o365-cef-file-read-success-dlprule](CodeChanges/microsoft-o365-cef-file-read-success-dlprule.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-file-read-success-dlprule&type=code)
- [microsoft-o365-cef-file-read-success-listcolumncreated](CodeChanges/microsoft-o365-cef-file-read-success-listcolumncreated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-file-read-success-listcolumncreated&type=code)
- [microsoft-o365-cef-file-read-success-listupdate](CodeChanges/microsoft-o365-cef-file-read-success-listupdate.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-file-read-success-listupdate&type=code)
- [microsoft-o365-cef-file-read-success-removedfromgroup](CodeChanges/microsoft-o365-cef-file-read-success-removedfromgroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-file-read-success-removedfromgroup&type=code)
- [microsoft-o365-cef-file-read-success-resultreturn](CodeChanges/microsoft-o365-cef-file-read-success-resultreturn.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-file-read-success-resultreturn&type=code)
- [microsoft-o365-cef-file-read-success-searchquery](CodeChanges/microsoft-o365-cef-file-read-success-searchquery.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-file-read-success-searchquery&type=code)
- [microsoft-o365-cef-file-read-success-sharepoint](CodeChanges/microsoft-o365-cef-file-read-success-sharepoint.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-file-read-success-sharepoint&type=code)
- [microsoft-o365-cef-file-read-success-tabupdated](CodeChanges/microsoft-o365-cef-file-read-success-tabupdated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-file-read-success-tabupdated&type=code)
- [microsoft-o365-cef-file-read-success-videorequest](CodeChanges/microsoft-o365-cef-file-read-success-videorequest.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-file-read-success-videorequest&type=code)
- [microsoft-o365-cef-file-write-success-companylink](CodeChanges/microsoft-o365-cef-file-write-success-companylink.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-file-write-success-companylink&type=code)
- [microsoft-o365-cef-file-write-success-microsoft](CodeChanges/microsoft-o365-cef-file-write-success-microsoft.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-file-write-success-microsoft&type=code)
- [microsoft-o365-cef-file-write-success-sharinginheritance](CodeChanges/microsoft-o365-cef-file-write-success-sharinginheritance.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-file-write-success-sharinginheritance&type=code)
- [microsoft-o365-cef-file-write-success-sharingrevoked](CodeChanges/microsoft-o365-cef-file-write-success-sharingrevoked.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-file-write-success-sharingrevoked&type=code)
- [microsoft-o365-cef-file-write-success-sharingset](CodeChanges/microsoft-o365-cef-file-write-success-sharingset.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-file-write-success-sharingset&type=code)
- [microsoft-o365-cef-file-write-success-wactoken](CodeChanges/microsoft-o365-cef-file-write-success-wactoken.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-file-write-success-wactoken&type=code)
- [microsoft-o365-json-app-activity-success-operation](CodeChanges/microsoft-o365-json-app-activity-success-operation.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-json-app-activity-success-operation&type=code)
- [microsoft-o365-json-app-activity-success-powerbi](CodeChanges/microsoft-o365-json-app-activity-success-powerbi.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-json-app-activity-success-powerbi&type=code)
- [microsoft-o365-mix-app-activity-success-microsoftteams](CodeChanges/microsoft-o365-mix-app-activity-success-microsoftteams.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-mix-app-activity-success-microsoftteams&type=code)
- [microsoft-o365-sk4-app-activity-success-create](CodeChanges/microsoft-o365-sk4-app-activity-success-create.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-sk4-app-activity-success-create&type=code)
- [microsoft-o365-sk4-app-addowner](CodeChanges/microsoft-o365-sk4-app-addowner.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-sk4-app-addowner&type=code)
- [microsoft-o365-sk4-app-file-move](CodeChanges/microsoft-o365-sk4-app-file-move.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-sk4-app-file-move&type=code)
- [microsoft-o365-sk4-app-file-operationworkload](CodeChanges/microsoft-o365-sk4-app-file-operationworkload.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-sk4-app-file-operationworkload&type=code)
- [microsoft-o365-sk4-app-file-send](CodeChanges/microsoft-o365-sk4-app-file-send.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-sk4-app-file-send&type=code)
- [microsoft-o365-sk4-app-file-setunifiedgroup](CodeChanges/microsoft-o365-sk4-app-file-setunifiedgroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-sk4-app-file-setunifiedgroup&type=code)
- [microsoft-o365-sk4-app-file-workload](CodeChanges/microsoft-o365-sk4-app-file-workload.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-sk4-app-file-workload&type=code)
- [microsoft-o365-sk4-file-app-userkey-1](CodeChanges/microsoft-o365-sk4-file-app-userkey-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-sk4-file-app-userkey-1&type=code)
- [microsoft-o365-xml-file-write-success-mailboxpermission](CodeChanges/microsoft-o365-xml-file-write-success-mailboxpermission.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-xml-file-write-success-mailboxpermission&type=code)
- [microsoft-windows-cef-endpoint-login-device](CodeChanges/microsoft-windows-cef-endpoint-login-device.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-windows-cef-endpoint-login-device&type=code)

#### Edit Regex Field
<a id="edit-regex-field"></a>
- [amazon-awscloudtrail-json-app-activity-awsapicall](CodeChanges/amazon-awscloudtrail-json-app-activity-awsapicall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-app-activity-awsapicall&type=code)
- [amazon-awscloudtrail-json-app-activity-getscreenshot](CodeChanges/amazon-awscloudtrail-json-app-activity-getscreenshot.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-app-activity-getscreenshot&type=code)
- [amazon-awscloudtrail-json-app-activity-loginprofile](CodeChanges/amazon-awscloudtrail-json-app-activity-loginprofile.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-app-activity-loginprofile&type=code)
- [amazon-awscloudtrail-json-app-activity-sendcommand](CodeChanges/amazon-awscloudtrail-json-app-activity-sendcommand.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-app-activity-sendcommand&type=code)
- [amazon-awscloudtrail-json-app-activity-success-awsconsoleaction](CodeChanges/amazon-awscloudtrail-json-app-activity-success-awsconsoleaction.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-app-activity-success-awsconsoleaction&type=code)
- [amazon-awscloudtrail-json-app-activity-updateprofile](CodeChanges/amazon-awscloudtrail-json-app-activity-updateprofile.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-app-activity-updateprofile&type=code)
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
- [amazon-awscloudtrail-json-role-assume-success-switchrole](CodeChanges/amazon-awscloudtrail-json-role-assume-success-switchrole.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-role-assume-success-switchrole&type=code)
- [amazon-awscloudtrail-json-role-create-success-createrole](CodeChanges/amazon-awscloudtrail-json-role-create-success-createrole.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-role-create-success-createrole&type=code)
- [amazon-awscloudtrail-json-role-policy-attach-success-attachrolepolicy](CodeChanges/amazon-awscloudtrail-json-role-policy-attach-success-attachrolepolicy.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-role-policy-attach-success-attachrolepolicy&type=code)
- [amazon-awscloudtrail-json-snapshot-create-awsapicall](CodeChanges/amazon-awscloudtrail-json-snapshot-create-awsapicall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-snapshot-create-awsapicall&type=code)
- [amazon-awscloudtrail-json-snapshot-modify-awsapicall](CodeChanges/amazon-awscloudtrail-json-snapshot-modify-awsapicall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-snapshot-modify-awsapicall&type=code)
- [amazon-awscloudtrail-json-user-create-awsapicall](CodeChanges/amazon-awscloudtrail-json-user-create-awsapicall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-user-create-awsapicall&type=code)
- [amazon-awscloudtrail-json-user-create-creategroup](CodeChanges/amazon-awscloudtrail-json-user-create-creategroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-user-create-creategroup&type=code)
- [amazon-awscloudtrail-json-user-key-create-createaccesskey](CodeChanges/amazon-awscloudtrail-json-user-key-create-createaccesskey.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-user-key-create-createaccesskey&type=code)
- [amazon-awscloudtrail-json-user-policy-attach-success-attachuserpolicy](CodeChanges/amazon-awscloudtrail-json-user-policy-attach-success-attachuserpolicy.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-user-policy-attach-success-attachuserpolicy&type=code)
- [amazon-awscloudtrail-sk4-app-activity-success-backupjobstarted](CodeChanges/amazon-awscloudtrail-sk4-app-activity-success-backupjobstarted.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-sk4-app-activity-success-backupjobstarted&type=code)
- [amazon-awscloudtrail-sk4-snapshot-create-success-sharedsnapshotvolumecreated](CodeChanges/amazon-awscloudtrail-sk4-snapshot-create-success-sharedsnapshotvolumecreated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-sk4-snapshot-create-success-sharedsnapshotvolumecreated&type=code)
- [amazon-awscloudtrail-sk4-user-token-create-success-tokenpost](CodeChanges/amazon-awscloudtrail-sk4-user-token-create-success-tokenpost.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-sk4-user-token-create-success-tokenpost&type=code)
- [exabeam-aa-kv-rule-trigger-success-anomaly](CodeChanges/exabeam-aa-kv-rule-trigger-success-anomaly.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20exabeam-aa-kv-rule-trigger-success-anomaly&type=code)
- [exabeam-aa-kv-rule-trigger-success-anomaly-1](CodeChanges/exabeam-aa-kv-rule-trigger-success-anomaly-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20exabeam-aa-kv-rule-trigger-success-anomaly-1&type=code)
- [fortinet-utm-kv-http-session-webfilter](CodeChanges/fortinet-utm-kv-http-session-webfilter.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20fortinet-utm-kv-http-session-webfilter&type=code)
- [ftp-f-str-file-delete-success-250](CodeChanges/ftp-f-str-file-delete-success-250.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20ftp-f-str-file-delete-success-250&type=code)
- [microsoft-azuremon-cef-app-activity-category](CodeChanges/microsoft-azuremon-cef-app-activity-category.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-cef-app-activity-category&type=code)
- [microsoft-azuremon-cef-network-start-fail-startconnectionfailed](CodeChanges/microsoft-azuremon-cef-network-start-fail-startconnectionfailed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-cef-network-start-fail-startconnectionfailed&type=code)
- [microsoft-azuremon-json-app-activity-administrative](CodeChanges/microsoft-azuremon-json-app-activity-administrative.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-json-app-activity-administrative&type=code)
- [microsoft-azuremon-json-app-activity-policy](CodeChanges/microsoft-azuremon-json-app-activity-policy.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-json-app-activity-policy&type=code)
- [microsoft-azuremon-json-app-activity-success-createeventhub](CodeChanges/microsoft-azuremon-json-app-activity-success-createeventhub.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-json-app-activity-success-createeventhub&type=code)
- [microsoft-azuremon-json-app-activity-success-microsoftinsightscatchall](CodeChanges/microsoft-azuremon-json-app-activity-success-microsoftinsightscatchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-json-app-activity-success-microsoftinsightscatchall&type=code)
- [microsoft-azuremon-json-app-activity-success-retrievenamespace](CodeChanges/microsoft-azuremon-json-app-activity-success-retrievenamespace.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-json-app-activity-success-retrievenamespace&type=code)
- [microsoft-azuremon-json-app-activity-success-retrievesubscription](CodeChanges/microsoft-azuremon-json-app-activity-success-retrievesubscription.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-json-app-activity-success-retrievesubscription&type=code)
- [microsoft-azuremon-json-app-activity-success-retrievetopic](CodeChanges/microsoft-azuremon-json-app-activity-success-retrievetopic.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-json-app-activity-success-retrievetopic&type=code)
- [microsoft-azuremon-json-app-activity-success-updatenamespace](CodeChanges/microsoft-azuremon-json-app-activity-success-updatenamespace.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-json-app-activity-success-updatenamespace&type=code)
- [microsoft-azuremon-mix-network-start-collection](CodeChanges/microsoft-azuremon-mix-network-start-collection.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-mix-network-start-collection&type=code)
- [microsoft-azuremon-sk4-app-activity-administrative](CodeChanges/microsoft-azuremon-sk4-app-activity-administrative.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-sk4-app-activity-administrative&type=code)
- [microsoft-azuremon-sk4-app-activity-alert](CodeChanges/microsoft-azuremon-sk4-app-activity-alert.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-sk4-app-activity-alert&type=code)
- [microsoft-azuremon-sk4-app-activity-appservicefileauditlogs](CodeChanges/microsoft-azuremon-sk4-app-activity-appservicefileauditlogs.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-sk4-app-activity-appservicefileauditlogs&type=code)
- [microsoft-azuremon-sk4-app-activity-azureservice](CodeChanges/microsoft-azuremon-sk4-app-activity-azureservice.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-sk4-app-activity-azureservice&type=code)
- [microsoft-azuremon-sk4-app-activity-bastionauditlogs](CodeChanges/microsoft-azuremon-sk4-app-activity-bastionauditlogs.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-sk4-app-activity-bastionauditlogs&type=code)
- [microsoft-azuremon-sk4-app-activity-eventhub](CodeChanges/microsoft-azuremon-sk4-app-activity-eventhub.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-sk4-app-activity-eventhub&type=code)
- [microsoft-azuremon-sk4-app-activity-microsoftinsights](CodeChanges/microsoft-azuremon-sk4-app-activity-microsoftinsights.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-sk4-app-activity-microsoftinsights&type=code)
- [microsoft-azuremon-sk4-app-activity-operationname](CodeChanges/microsoft-azuremon-sk4-app-activity-operationname.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-sk4-app-activity-operationname&type=code)
- [microsoft-azuremon-sk4-app-activity-policy](CodeChanges/microsoft-azuremon-sk4-app-activity-policy.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-sk4-app-activity-policy&type=code)
- [microsoft-azuremon-sk4-app-notification-performancelog](CodeChanges/microsoft-azuremon-sk4-app-notification-performancelog.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-sk4-app-notification-performancelog&type=code)
- [microsoft-azuremon-sk4-app-notification-resourcehealth-1](CodeChanges/microsoft-azuremon-sk4-app-notification-resourcehealth-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-sk4-app-notification-resourcehealth-1&type=code)
- [microsoft-azuremon-sk4-app-notification-servicehealth-1](CodeChanges/microsoft-azuremon-sk4-app-notification-servicehealth-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-sk4-app-notification-servicehealth-1&type=code)
- [microsoft-azuremon-sk4-database-modify-success-sql](CodeChanges/microsoft-azuremon-sk4-database-modify-success-sql.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-sk4-database-modify-success-sql&type=code)
- [microsoft-evsecurity-json-ds-object-modify-success-5136](CodeChanges/microsoft-evsecurity-json-ds-object-modify-success-5136.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-ds-object-modify-success-5136&type=code)
- [microsoft-evsecurity-json-endpoint-login-4776](CodeChanges/microsoft-evsecurity-json-endpoint-login-4776.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-endpoint-login-4776&type=code)
- [microsoft-evsecurity-json-group-modify-success-4755](CodeChanges/microsoft-evsecurity-json-group-modify-success-4755.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-group-modify-success-4755&type=code)
- [microsoft-evsecurity-kv-endpoint-create-created](CodeChanges/microsoft-evsecurity-kv-endpoint-create-created.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-create-created&type=code)
- [microsoft-evsecurity-kv-endpoint-login-4768-2](CodeChanges/microsoft-evsecurity-kv-endpoint-login-4768-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-4768-2&type=code)
- [microsoft-evsecurity-kv-endpoint-login-4769-2](CodeChanges/microsoft-evsecurity-kv-endpoint-login-4769-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-4769-2&type=code)
- [microsoft-evsecurity-mix-user-lock-success-4740](CodeChanges/microsoft-evsecurity-mix-user-lock-success-4740.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-user-lock-success-4740&type=code)
- [microsoft-evsecurity-mix-user-privilege-assign-success-4673](CodeChanges/microsoft-evsecurity-mix-user-privilege-assign-success-4673.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-user-privilege-assign-success-4673&type=code)
- [microsoft-evsecurity-xml-user-privilege-assign-success-4672](CodeChanges/microsoft-evsecurity-xml-user-privilege-assign-success-4672.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-user-privilege-assign-success-4672&type=code)
- [pan-gp-cef-app-activity-success-globalprotect](CodeChanges/pan-gp-cef-app-activity-success-globalprotect.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-gp-cef-app-activity-success-globalprotect&type=code)
- [pan-gp-csv-endpoint-authentication-success-authsuccess](CodeChanges/pan-gp-csv-endpoint-authentication-success-authsuccess.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-gp-csv-endpoint-authentication-success-authsuccess&type=code)
- [pan-gp-csv-vpn-login-fail-loginfailure](CodeChanges/pan-gp-csv-vpn-login-fail-loginfailure.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-gp-csv-vpn-login-fail-loginfailure&type=code)
- [pan-gp-csv-vpn-login-success-connected](CodeChanges/pan-gp-csv-vpn-login-success-connected.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-gp-csv-vpn-login-success-connected&type=code)
- [pan-gp-csv-vpn-login-success-generated](CodeChanges/pan-gp-csv-vpn-login-success-generated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-gp-csv-vpn-login-success-generated&type=code)
- [pan-gp-csv-vpn-login-success-login](CodeChanges/pan-gp-csv-vpn-login-success-login.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-gp-csv-vpn-login-success-login&type=code)
- [pan-gp-csv-vpn-login-success-loginsucceeded](CodeChanges/pan-gp-csv-vpn-login-success-loginsucceeded.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-gp-csv-vpn-login-success-loginsucceeded&type=code)
- [pan-gp-csv-vpn-logout-success-logout-2](CodeChanges/pan-gp-csv-vpn-logout-success-logout-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-gp-csv-vpn-logout-success-logout-2&type=code)
- [pan-gp-csv-vpn-logout-success-succeeded](CodeChanges/pan-gp-csv-vpn-logout-success-succeeded.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-gp-csv-vpn-logout-success-succeeded&type=code)
- [pan-gp-mix-vpn-login-success-authsucc](CodeChanges/pan-gp-mix-vpn-login-success-authsucc.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-gp-mix-vpn-login-success-authsucc&type=code)
- [pan-ngfw-csv-alert-trigger-success-data](CodeChanges/pan-ngfw-csv-alert-trigger-success-data.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-alert-trigger-success-data&type=code)
- [pan-ngfw-csv-alert-trigger-success-file](CodeChanges/pan-ngfw-csv-alert-trigger-success-file.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-alert-trigger-success-file&type=code)
- [pan-ngfw-csv-alert-trigger-success-flood](CodeChanges/pan-ngfw-csv-alert-trigger-success-flood.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-alert-trigger-success-flood&type=code)
- [pan-ngfw-csv-alert-trigger-success-scan](CodeChanges/pan-ngfw-csv-alert-trigger-success-scan.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-alert-trigger-success-scan&type=code)
- [pan-ngfw-csv-alert-trigger-success-url](CodeChanges/pan-ngfw-csv-alert-trigger-success-url.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-alert-trigger-success-url&type=code)
- [pan-ngfw-csv-app-activity-dnsproxy](CodeChanges/pan-ngfw-csv-app-activity-dnsproxy.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-app-activity-dnsproxy&type=code)
- [pan-ngfw-csv-app-activity-general](CodeChanges/pan-ngfw-csv-app-activity-general.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-app-activity-general&type=code)
- [pan-ngfw-csv-app-activity-globalprotect](CodeChanges/pan-ngfw-csv-app-activity-globalprotect.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-app-activity-globalprotect&type=code)
- [pan-ngfw-csv-app-activity-ha](CodeChanges/pan-ngfw-csv-app-activity-ha.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-app-activity-ha&type=code)
- [pan-ngfw-csv-app-activity-wildfire](CodeChanges/pan-ngfw-csv-app-activity-wildfire.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-app-activity-wildfire&type=code)
- [pan-ngfw-csv-app-notification-connstatus](CodeChanges/pan-ngfw-csv-app-notification-connstatus.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-app-notification-connstatus&type=code)
- [pan-ngfw-csv-app-notification-sdwan](CodeChanges/pan-ngfw-csv-app-notification-sdwan.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-app-notification-sdwan&type=code)
- [pan-ngfw-csv-app-notification-system](CodeChanges/pan-ngfw-csv-app-notification-system.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-app-notification-system&type=code)
- [pan-ngfw-csv-app-notification-urlfiltering](CodeChanges/pan-ngfw-csv-app-notification-urlfiltering.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-app-notification-urlfiltering&type=code)
- [pan-ngfw-csv-app-notification-userid](CodeChanges/pan-ngfw-csv-app-notification-userid.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-app-notification-userid&type=code)
- [pan-ngfw-csv-app-time-modify-ntpd](CodeChanges/pan-ngfw-csv-app-time-modify-ntpd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-app-time-modify-ntpd&type=code)
- [pan-ngfw-csv-configuration-load-ras](CodeChanges/pan-ngfw-csv-configuration-load-ras.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-configuration-load-ras&type=code)
- [pan-ngfw-csv-configuration-load-satd](CodeChanges/pan-ngfw-csv-configuration-load-satd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-configuration-load-satd&type=code)
- [pan-ngfw-csv-configuration-load-sslmgr](CodeChanges/pan-ngfw-csv-configuration-load-sslmgr.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-configuration-load-sslmgr&type=code)
- [pan-ngfw-csv-configuration-modify-success-config](CodeChanges/pan-ngfw-csv-configuration-modify-success-config.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-configuration-modify-success-config&type=code)
- [pan-ngfw-csv-configuration-modify-success-configfailed](CodeChanges/pan-ngfw-csv-configuration-modify-success-configfailed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-configuration-modify-success-configfailed&type=code)
- [pan-ngfw-csv-configuration-modify-success-configsucceded](CodeChanges/pan-ngfw-csv-configuration-modify-success-configsucceded.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-configuration-modify-success-configsucceded&type=code)
- [pan-ngfw-csv-configuration-modify-success-configunauthorized](CodeChanges/pan-ngfw-csv-configuration-modify-success-configunauthorized.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-configuration-modify-success-configunauthorized&type=code)
- [pan-ngfw-csv-configuration-routing-modify-success-routing](CodeChanges/pan-ngfw-csv-configuration-routing-modify-success-routing.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-configuration-routing-modify-success-routing&type=code)
- [pan-ngfw-csv-dhcp-traffic-generalinformational](CodeChanges/pan-ngfw-csv-dhcp-traffic-generalinformational.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-dhcp-traffic-generalinformational&type=code)
- [pan-ngfw-csv-endpoint-login-success-system](CodeChanges/pan-ngfw-csv-endpoint-login-success-system.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-endpoint-login-success-system&type=code)
- [pan-ngfw-csv-http-session-9999](CodeChanges/pan-ngfw-csv-http-session-9999.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-http-session-9999&type=code)
- [pan-ngfw-csv-http-session-webbrowsing](CodeChanges/pan-ngfw-csv-http-session-webbrowsing.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-http-session-webbrowsing&type=code)
- [pan-ngfw-csv-network-traffic-fail-drop](CodeChanges/pan-ngfw-csv-network-traffic-fail-drop.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-network-traffic-fail-drop&type=code)
- [pan-ngfw-csv-network-traffic-fail-panorama](CodeChanges/pan-ngfw-csv-network-traffic-fail-panorama.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-network-traffic-fail-panorama&type=code)
- [pan-ngfw-csv-network-traffic-fail-tcp](CodeChanges/pan-ngfw-csv-network-traffic-fail-tcp.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-network-traffic-fail-tcp&type=code)
- [pan-ngfw-csv-network-traffic-packet](CodeChanges/pan-ngfw-csv-network-traffic-packet.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-network-traffic-packet&type=code)
- [pan-ngfw-csv-network-traffic-success-allow](CodeChanges/pan-ngfw-csv-network-traffic-success-allow.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-network-traffic-success-allow&type=code)
- [pan-ngfw-csv-network-traffic-success-connection](CodeChanges/pan-ngfw-csv-network-traffic-success-connection.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-network-traffic-success-connection&type=code)
- [pan-ngfw-csv-network-traffic-success-end](CodeChanges/pan-ngfw-csv-network-traffic-success-end.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-network-traffic-success-end&type=code)
- [pan-ngfw-csv-vpn-authentication-systemvpn](CodeChanges/pan-ngfw-csv-vpn-authentication-systemvpn.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-vpn-authentication-systemvpn&type=code)
- [pan-ngfw-json-alert-trigger-success-vulnerability](CodeChanges/pan-ngfw-json-alert-trigger-success-vulnerability.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-json-alert-trigger-success-vulnerability&type=code)
- [pan-ngfw-mix-alert-trigger-success-spywarealert](CodeChanges/pan-ngfw-mix-alert-trigger-success-spywarealert.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-mix-alert-trigger-success-spywarealert&type=code)
- [pan-ngfw-mix-alert-trigger-success-threadvulnerability](CodeChanges/pan-ngfw-mix-alert-trigger-success-threadvulnerability.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-mix-alert-trigger-success-threadvulnerability&type=code)
- [pan-ngfw-mix-alert-trigger-success-virus](CodeChanges/pan-ngfw-mix-alert-trigger-success-virus.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-mix-alert-trigger-success-virus&type=code)
- [pan-wildfire-csv-alert-trigger-success-threadwildfire](CodeChanges/pan-wildfire-csv-alert-trigger-success-threadwildfire.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-wildfire-csv-alert-trigger-success-threadwildfire&type=code)
- [pan-wildfire-csv-alert-trigger-success-wildfirevirus](CodeChanges/pan-wildfire-csv-alert-trigger-success-wildfirevirus.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-wildfire-csv-alert-trigger-success-wildfirevirus&type=code)
- [proofpoint-pitm-json-alert-trigger-success](CodeChanges/proofpoint-pitm-json-alert-trigger-success.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20proofpoint-pitm-json-alert-trigger-success&type=code)
- [sentinelone-singularityp-json-alert-trigger-success-activitytype19](CodeChanges/sentinelone-singularityp-json-alert-trigger-success-activitytype19.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-singularityp-json-alert-trigger-success-activitytype19&type=code)
- [sentinelone-singularityp-json-alert-trigger-success-datasourcecategorysecurity](CodeChanges/sentinelone-singularityp-json-alert-trigger-success-datasourcecategorysecurity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-singularityp-json-alert-trigger-success-datasourcecategorysecurity&type=code)
- [sentinelone-singularityp-json-app-activity-success-30-catchall](CodeChanges/sentinelone-singularityp-json-app-activity-success-30-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-singularityp-json-app-activity-success-30-catchall&type=code)
- [sentinelone-singularityp-json-app-activity-success-activitytype2001](CodeChanges/sentinelone-singularityp-json-app-activity-success-activitytype2001.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-singularityp-json-app-activity-success-activitytype2001&type=code)
- [sentinelone-singularityp-json-app-activity-success-activitytype2004](CodeChanges/sentinelone-singularityp-json-app-activity-success-activitytype2004.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-singularityp-json-app-activity-success-activitytype2004&type=code)
- [sentinelone-singularityp-json-app-activity-success-activitytype4008](CodeChanges/sentinelone-singularityp-json-app-activity-success-activitytype4008.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-singularityp-json-app-activity-success-activitytype4008&type=code)
- [sentinelone-singularityp-json-app-login-fail-133](CodeChanges/sentinelone-singularityp-json-app-login-fail-133.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-singularityp-json-app-login-fail-133&type=code)
- [sentinelone-singularityp-json-app-login-success-27](CodeChanges/sentinelone-singularityp-json-app-login-success-27.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-singularityp-json-app-login-success-27&type=code)
- [sentinelone-singularityp-json-app-logout-success-33](CodeChanges/sentinelone-singularityp-json-app-logout-success-33.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-singularityp-json-app-logout-success-33&type=code)
- [sentinelone-singularityp-json-app-notification-success-catchall](CodeChanges/sentinelone-singularityp-json-app-notification-success-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-singularityp-json-app-notification-success-catchall&type=code)
- [sentinelone-singularityp-json-app-notification-success-disableagent](CodeChanges/sentinelone-singularityp-json-app-notification-success-disableagent.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-singularityp-json-app-notification-success-disableagent&type=code)
- [sentinelone-singularityp-json-file-delete-success-3103](CodeChanges/sentinelone-singularityp-json-file-delete-success-3103.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-singularityp-json-file-delete-success-3103&type=code)
- [sentinelone-singularityp-json-rule-create-success-3600](CodeChanges/sentinelone-singularityp-json-rule-create-success-3600.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-singularityp-json-rule-create-success-3600&type=code)
- [sentinelone-singularityp-json-rule-delete-success-3602](CodeChanges/sentinelone-singularityp-json-rule-delete-success-3602.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-singularityp-json-rule-delete-success-3602&type=code)
- [sentinelone-singularityp-json-user-password-modify-success-3711](CodeChanges/sentinelone-singularityp-json-user-password-modify-success-3711.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-singularityp-json-user-password-modify-success-3711&type=code)
- [sentinelone-singularityp-json-user-password-reset-success-3710](CodeChanges/sentinelone-singularityp-json-user-password-reset-success-3710.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-singularityp-json-user-password-reset-success-3710&type=code)
- [sentinelone-singularityp-json-user-role-assign-success-23](CodeChanges/sentinelone-singularityp-json-user-role-assign-success-23.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-singularityp-json-user-role-assign-success-23&type=code)
- [sentinelone-singularityp-json-user-role-assign-success-37](CodeChanges/sentinelone-singularityp-json-user-role-assign-success-37.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-singularityp-json-user-role-assign-success-37&type=code)
- [unix-sm-kv-email-send](CodeChanges/unix-sm-kv-email-send.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-sm-kv-email-send&type=code)

#### Removed Parser
<a id="removed-parser"></a>
- [cisco-acs-cef-endpoint-authentication-success-authsucceeded](CodeChanges/cisco-acs-cef-endpoint-authentication-success-authsucceeded.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-acs-cef-endpoint-authentication-success-authsucceeded&type=code)
- [cisco-acs-cef-endpoint-authentication-success-login](CodeChanges/cisco-acs-cef-endpoint-authentication-success-login.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-acs-cef-endpoint-authentication-success-login&type=code)
- [cisco-asa-cef-vpn-login-success-assignedprivateip](CodeChanges/cisco-asa-cef-vpn-login-success-assignedprivateip.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-cef-vpn-login-success-assignedprivateip&type=code)
- [cisco-asa-cef-vpn-login-success-authsuccess](CodeChanges/cisco-asa-cef-vpn-login-success-authsuccess.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-cef-vpn-login-success-authsuccess&type=code)
- [cisco-asa-cef-vpn-logout-success-sessionisbeingtorndown](CodeChanges/cisco-asa-cef-vpn-logout-success-sessionisbeingtorndown.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-cef-vpn-logout-success-sessionisbeingtorndown&type=code)
- [cisco-asa-kv-vpn-logout-success-28](CodeChanges/cisco-asa-kv-vpn-logout-success-28.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-kv-vpn-logout-success-28&type=code)
- [cisco-cucm-kv-app-activity-success-useraccess](CodeChanges/cisco-cucm-kv-app-activity-success-useraccess.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-cucm-kv-app-activity-success-useraccess&type=code)
- [cisco-duo-cef-app-login-fail-twofactorfail](CodeChanges/cisco-duo-cef-app-login-fail-twofactorfail.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-duo-cef-app-login-fail-twofactorfail&type=code)
- [cisco-duo-cef-app-login-success-success](CodeChanges/cisco-duo-cef-app-login-success-success.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-duo-cef-app-login-success-success&type=code)
- [cisco-duo-cef-app-login-success-twofactorsuccess](CodeChanges/cisco-duo-cef-app-login-success-twofactorsuccess.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-duo-cef-app-login-success-twofactorsuccess&type=code)
- [cisco-duo-cef-endpoint-authentication-mfaservice](CodeChanges/cisco-duo-cef-endpoint-authentication-mfaservice.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-duo-cef-endpoint-authentication-mfaservice&type=code)
- [cisco-duo-kv-app-login-success-adminlogin](CodeChanges/cisco-duo-kv-app-login-success-adminlogin.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-duo-kv-app-login-success-adminlogin&type=code)
- [cisco-duo-kv-endpoint-authentication-fail-failure](CodeChanges/cisco-duo-kv-endpoint-authentication-fail-failure.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-duo-kv-endpoint-authentication-fail-failure&type=code)
- [cisco-duo-kv-endpoint-authentication-success-success](CodeChanges/cisco-duo-kv-endpoint-authentication-success-success.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-duo-kv-endpoint-authentication-success-success&type=code)
- [cisco-fp-cef-network-traffic-connection-stats](CodeChanges/cisco-fp-cef-network-traffic-connection-stats.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-fp-cef-network-traffic-connection-stats&type=code)
- [cisco-iws-csv-http-session-tcp](CodeChanges/cisco-iws-csv-http-session-tcp.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-iws-csv-http-session-tcp&type=code)
- [cisco-iws-kv-http-session-info-1](CodeChanges/cisco-iws-kv-http-session-info-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-iws-kv-http-session-info-1&type=code)
- [cisco-iws-kv-http-session-none](CodeChanges/cisco-iws-kv-http-session-none.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-iws-kv-http-session-none&type=code)
- [cisco-iws-kv-http-session-nonessl](CodeChanges/cisco-iws-kv-http-session-nonessl.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-iws-kv-http-session-nonessl&type=code)
- [cisco-iws-kv-http-session-tcpclientrefreshmiss](CodeChanges/cisco-iws-kv-http-session-tcpclientrefreshmiss.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-iws-kv-http-session-tcpclientrefreshmiss&type=code)
- [cisco-iws-kv-http-session-tcpclientrefreshmissssl](CodeChanges/cisco-iws-kv-http-session-tcpclientrefreshmissssl.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-iws-kv-http-session-tcpclientrefreshmissssl&type=code)
- [cisco-iws-kv-http-session-tcpdenied](CodeChanges/cisco-iws-kv-http-session-tcpdenied.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-iws-kv-http-session-tcpdenied&type=code)
- [cisco-iws-kv-http-session-tcpdeniedssl](CodeChanges/cisco-iws-kv-http-session-tcpdeniedssl.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-iws-kv-http-session-tcpdeniedssl&type=code)
- [cisco-iws-kv-http-session-tcphit](CodeChanges/cisco-iws-kv-http-session-tcphit.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-iws-kv-http-session-tcphit&type=code)
- [cisco-iws-kv-http-session-tcpimshit](CodeChanges/cisco-iws-kv-http-session-tcpimshit.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-iws-kv-http-session-tcpimshit&type=code)
- [cisco-iws-kv-http-session-tcpmemhit](CodeChanges/cisco-iws-kv-http-session-tcpmemhit.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-iws-kv-http-session-tcpmemhit&type=code)
- [cisco-iws-kv-http-session-tcpmissssl](CodeChanges/cisco-iws-kv-http-session-tcpmissssl.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-iws-kv-http-session-tcpmissssl&type=code)
- [cisco-iws-kv-http-session-tcprefreshhit](CodeChanges/cisco-iws-kv-http-session-tcprefreshhit.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-iws-kv-http-session-tcprefreshhit&type=code)
- [cisco-iws-str-http-session-direct](CodeChanges/cisco-iws-str-http-session-direct.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-iws-str-http-session-direct&type=code)
- [cisco-securenwanalytics-str-alert-trigger-success-z](CodeChanges/cisco-securenwanalytics-str-alert-trigger-success-z.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-securenwanalytics-str-alert-trigger-success-z&type=code)
- [cisco-securewebapp-kv-http-session-accesslogs](CodeChanges/cisco-securewebapp-kv-http-session-accesslogs.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-securewebapp-kv-http-session-accesslogs&type=code)
- [cisco-tacacs-kv-process-create-success-tacacs](CodeChanges/cisco-tacacs-kv-process-create-success-tacacs.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-tacacs-kv-process-create-success-tacacs&type=code)
- [cisco-ucm-kv-configuration-modify-success-generalconfigurationupdate](CodeChanges/cisco-ucm-kv-configuration-modify-success-generalconfigurationupdate.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-ucm-kv-configuration-modify-success-generalconfigurationupdate&type=code)
- [cisco-ucm-kv-user-role-modify-success-userrolemembershipupdate](CodeChanges/cisco-ucm-kv-user-role-modify-success-userrolemembershipupdate.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-ucm-kv-user-role-modify-success-userrolemembershipupdate&type=code)
- [cisco-umbrella-json-dns-response-success-responsecode](CodeChanges/cisco-umbrella-json-dns-response-success-responsecode.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-umbrella-json-dns-response-success-responsecode&type=code)
- [cisco-umbrella-json-dns-response-success-tenantid](CodeChanges/cisco-umbrella-json-dns-response-success-tenantid.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-umbrella-json-dns-response-success-tenantid&type=code)
- [citrix-cgateway-cef-app-activity-79916606](CodeChanges/citrix-cgateway-cef-app-activity-79916606.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20citrix-cgateway-cef-app-activity-79916606&type=code)
- [citrix-cgateway-cef-http-session-success-httprequest](CodeChanges/citrix-cgateway-cef-http-session-success-httprequest.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20citrix-cgateway-cef-http-session-success-httprequest&type=code)
- [citrix-cgateway-cef-vpn-logout-success-netscaler](CodeChanges/citrix-cgateway-cef-vpn-logout-success-netscaler.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20citrix-cgateway-cef-vpn-logout-success-netscaler&type=code)
- [citrix-cgateway-str-app-authentication-message](CodeChanges/citrix-cgateway-str-app-authentication-message.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20citrix-cgateway-str-app-authentication-message&type=code)
- [citrix-cgateway-str-network-notification-below](CodeChanges/citrix-cgateway-str-network-notification-below.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20citrix-cgateway-str-network-notification-below&type=code)
- [citrix-weblogging-str-http-session-5991](CodeChanges/citrix-weblogging-str-http-session-5991.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20citrix-weblogging-str-http-session-5991&type=code)
- [clearsense-cs-sk4-app-activity-success-clearsenseaudit](CodeChanges/clearsense-cs-sk4-app-activity-success-clearsenseaudit.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20clearsense-cs-sk4-app-activity-success-clearsenseaudit&type=code)
- [cloudfare-waf-sk4-http-request-cloudflareaws](CodeChanges/cloudfare-waf-sk4-http-request-cloudflareaws.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cloudfare-waf-sk4-http-request-cloudflareaws&type=code)
- [cloudflare-waf-sk4-http-session-firewallmatchesactions](CodeChanges/cloudflare-waf-sk4-http-session-firewallmatchesactions.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cloudflare-waf-sk4-http-session-firewallmatchesactions&type=code)
- [code42-incydr-json-file-delete-success-deviceaddress](CodeChanges/code42-incydr-json-file-delete-success-deviceaddress.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20code42-incydr-json-file-delete-success-deviceaddress&type=code)
- [code42-incydr-json-peripheral-storage-activity-success-deviceaddress](CodeChanges/code42-incydr-json-peripheral-storage-activity-success-deviceaddress.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20code42-incydr-json-peripheral-storage-activity-success-deviceaddress&type=code)
- [code42-incydr-json-peripheral-storage-insert-success-deviceappeared](CodeChanges/code42-incydr-json-peripheral-storage-insert-success-deviceappeared.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20code42-incydr-json-peripheral-storage-insert-success-deviceappeared&type=code)
- [contrastsecurity-cs-cef-alert-trigger-success-security](CodeChanges/contrastsecurity-cs-cef-alert-trigger-success-security.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20contrastsecurity-cs-cef-alert-trigger-success-security&type=code)

</details>

<details>
<summary><strong id="parsertemplate">ParserTemplate (11)</strong></summary>


### Change Types
- [Could Not Compare](#could-not-compare)
- [Added Parser Template](#added-parser-template)
- [Changed Parsed Fields](#changed-parsed-fields)
- [Edit Regex Field](#edit-regex-field)

#### Could Not Compare
<a id="could-not-compare"></a>
- [wiz-w-json-audit-log](CodeChanges/wiz-w-json-audit-log.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20wiz-w-json-audit-log&type=code)

#### Added Parser Template
<a id="added-parser-template"></a>
- [openaievents](CodeChanges/openaievents.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20openaievents&type=code)
- [zyxel-network-events](CodeChanges/zyxel-network-events.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zyxel-network-events&type=code)

#### Changed Parsed Fields
<a id="changed-parsed-fields"></a>
- [microsoft-azuread-json-events](CodeChanges/microsoft-azuread-json-events.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuread-json-events&type=code)

#### Edit Regex Field
<a id="edit-regex-field"></a>
- [aws-cloudtrail-json](CodeChanges/aws-cloudtrail-json.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20aws-cloudtrail-json&type=code)
- [cef-microsoft-app-activity-3](CodeChanges/cef-microsoft-app-activity-3.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cef-microsoft-app-activity-3&type=code)
- [json-sentinelone-activitytype](CodeChanges/json-sentinelone-activitytype.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20json-sentinelone-activitytype&type=code)
- [paloalto-firewall](CodeChanges/paloalto-firewall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20paloalto-firewall&type=code)
- [pan-csv-threat](CodeChanges/pan-csv-threat.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-csv-threat&type=code)
- [pan-system-1](CodeChanges/pan-system-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-system-1&type=code)
- [raw-pan-vpn-event](CodeChanges/raw-pan-vpn-event.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20raw-pan-vpn-event&type=code)

</details>