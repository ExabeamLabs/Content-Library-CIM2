# Content Package 2025.26.1

These release notes contain information about content package 2025.26.1, released on 18 Dec 2025.


## Enhancements
- Parse email and appID from principalSubject and resourceName, respectively
- Created new parser checkpoint-tp-kv-alert-trigger-success-actionprevent for logs with action 'Prevent'. Adjusted the parser conditions for parser checkpoint-ngfw-kv-app-activity-newantivirus to match broader category of logs, also enhanced the field mapping.
- New Palo Alto parsers added for System & Config logs.
- Created new parser for json format logs of beyondtrust for type:process and type: User Logon beyondtrust-b-json-process-create-success-ecs beyondtrust-b-json-user-logon-success-ecs
- Updated activity_type from : http-session to http-request for below parsers pan-ngfw-leef-http-session-threat pan-ngfw-csv-http-session-9999 pan-ngfw-csv-http-session-webbrowsing pan-ngfw-csv-network-traffic-success-connection pan-ngfw-cef-http-session-url pan-ngfw-json-http-session-webbrowsing pan-ngfw-json-alert-trigger-success-threat pan-ngfw-cef-http-session-url-1 pan-prismaaccess-leef-http-session-threat
- Added new parsers for Ermes Browser Security Platform logs: ermes-ebsp-json-alert-trigger-success-blockedrequests, ermes-ebsp-json-alert-trigger-success-extensionsthreat, ermes-ebsp-json-app-login-success-detectedtracebusinessaccountlogin, ermes-ebsp-json-app-success-dashboardauth, ermes-ebsp-json-app-activity-success-dashboardaudit

## Addressed Issues
- Added src_port field extraction for parser - microsoft-evsecurity-xml-endpoint-login-4768.
- Updated dest_email_address field extraction for parser: mimecast-seg-cef-email-url. Updated email_address, email_domain, src_ip, service_name field extraction for parser: mimecast-seg-cef-app-login-success-audittype. Updated email_address, email_domain, src_ip, failure_reason, app field extraction for parser: mimecast-seg-cef-app-login-fail-logonauthfailed. Updated dest_email_address field extraction for parser: mimecast-seg-json-email-eventtype.
- Updated time, protocol, method, web_domain, dest_port, uri_path, http_response_code, bytes, policy_id, protocol field extractions for parser: akamai-siem-json-http-session-httpmessage.
- Corrected TimeFormats for the following parsers:- microsoft-evpowershell-xml-network-listen-53504, microsoft-evpowershell-xml-script-execute-success-4104, microsoft-evpowershell-xml-endpoint-notification-40962.
- Updated dest_ip and dest_host field extractions for parser: trendmicro-officescan-kv-alert-trigger-success-deepsecuritymanager.
- Count of Beam Features Modified: 1 # Feature ID Field Modified Old Value New Value 1 NumDCP-PCHEnum-TC-U-HEnum _beam_feature.query (source_user_entity_id = '${trigger.scope_value}') AND (activity_type = 'process-create') AND (process_name IN 'System Enumeration Processes') OR (process_name= 'net.exe' AND (process_command_line = (WLDi(' config '), WLDi(' share '), WLDi(' start '), WLDi(' time '), WLDi(' use '), WLDi(' view ')))) OR (process_name= 'powershell.exe' AND (process_command_line = WLDi(' adrecon.ps1 '))) AND NOT (product = 'NG Analytics' AND activity_type = 'rule-trigger' AND vendor = 'Exabeam') (source_user_entity_id = '${trigger.scope_value}') AND (activity_type =  'process-create') AND ((process_name IN 'System Enumeration Processes') OR (process_name= 'net.exe' AND (process_command_line = (WLDi(' config '), WLDi(' share '), WLDi(' start '), WLDi(' time '), WLDi(' use '), WLDi(' view ')))) OR (process_name= ('powershell.exe','pwsh.exe') AND (process_command_line = WLDi(' adrecon.ps1 ')))) AND NOT (product = 'NG Analytics' AND activity_type = 'rule-trigger' AND vendor = 'Exabeam')
- Updated src_ip field extraction for parser: postgresql-p-str-database-query-success-logaudit
- Updated user, domain regex of parser microsoft-evsecurity-xml-process-close-4689

## Code Changes
### ℹ️ How to Read This Document

Each item listed under **Code Changes** includes:

- **A link to a detailed change file**  
  Click the filename (e.g., `Carbon Black.md`) to open a full table showing what changed.

- **A search icon 🔍**  
  Click the 🔍 icon to search for this resource in the [Exabeam Content Library](https://github.com/ExabeamLabs/Content-Library-CIM2).


<details>
<summary><strong id="event-builder">Event Builder (9)</strong></summary>


### Change Types
- [Added Event Builder](#added-event-builder)

#### Added Event Builder
<a id="added-event-builder"></a>
- [beyondtrust-ecs-endpoint-login-success](CodeChanges/beyondtrust-ecs-endpoint-login-success.md)
- [dl-ermes-ebsp-alert-trigger-success](CodeChanges/dl-ermes-ebsp-alert-trigger-success.md)
- [dl-ermes-ebsp-app-logout-success](CodeChanges/dl-ermes-ebsp-app-logout-success.md)
- [dl-f5-big-ip-configuration-modify-fail](CodeChanges/dl-f5-big-ip-configuration-modify-fail.md)
- [dl-windows-file-delete-success](CodeChanges/dl-windows-file-delete-success.md)
- [ermes-ebsp-app-activity-success](CodeChanges/ermes-ebsp-app-activity-success.md)
- [ermes-ebsp-app-login-success](CodeChanges/ermes-ebsp-app-login-success.md)
- [humansecurity-botdefender-http-request-fail](CodeChanges/humansecurity-botdefender-http-request-fail.md)
- [humansecurity-botdefender-http-request-success](CodeChanges/humansecurity-botdefender-http-request-success.md)

</details>

<details>
<summary><strong id="parser">Parser (34)</strong></summary>


### Change Types
- [Could Not Compare](#could-not-compare)
- [Added Parser](#added-parser)
- [Changed Parsed Fields](#changed-parsed-fields)
- [Edit Attribute](#edit-attribute)
- [Edit Regex Field](#edit-regex-field)

#### Could Not Compare
<a id="could-not-compare"></a>
- [microsoft-evpowershell-xml-endpoint-notification-40962](CodeChanges/microsoft-evpowershell-xml-endpoint-notification-40962.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evpowershell-xml-endpoint-notification-40962&type=code)
- [microsoft-evpowershell-xml-network-listen-53504](CodeChanges/microsoft-evpowershell-xml-network-listen-53504.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evpowershell-xml-network-listen-53504&type=code)
- [microsoft-evpowershell-xml-script-execute-success-4104](CodeChanges/microsoft-evpowershell-xml-script-execute-success-4104.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evpowershell-xml-script-execute-success-4104&type=code)

#### Added Parser
<a id="added-parser"></a>
- [beyondtrust-b-json-process-create-success-ecs](CodeChanges/beyondtrust-b-json-process-create-success-ecs.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20beyondtrust-b-json-process-create-success-ecs&type=code)
- [beyondtrust-b-json-user-logon-success-ecs](CodeChanges/beyondtrust-b-json-user-logon-success-ecs.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20beyondtrust-b-json-user-logon-success-ecs&type=code)
- [checkpoint-tp-kv-alert-trigger-success-actionprevent](CodeChanges/checkpoint-tp-kv-alert-trigger-success-actionprevent.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-tp-kv-alert-trigger-success-actionprevent&type=code)
- [ermes-ebsp-json-alert-trigger-success-blockedrequests](CodeChanges/ermes-ebsp-json-alert-trigger-success-blockedrequests.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20ermes-ebsp-json-alert-trigger-success-blockedrequests&type=code)
- [ermes-ebsp-json-alert-trigger-success-extensionsthreat](CodeChanges/ermes-ebsp-json-alert-trigger-success-extensionsthreat.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20ermes-ebsp-json-alert-trigger-success-extensionsthreat&type=code)
- [ermes-ebsp-json-app-activity-success-dashboardaudit](CodeChanges/ermes-ebsp-json-app-activity-success-dashboardaudit.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20ermes-ebsp-json-app-activity-success-dashboardaudit&type=code)
- [ermes-ebsp-json-app-login-success-detectedtracebusinessaccountlogin](CodeChanges/ermes-ebsp-json-app-login-success-detectedtracebusinessaccountlogin.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20ermes-ebsp-json-app-login-success-detectedtracebusinessaccountlogin&type=code)
- [ermes-ebsp-json-app-success-dashboardauth](CodeChanges/ermes-ebsp-json-app-success-dashboardauth.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20ermes-ebsp-json-app-success-dashboardauth&type=code)
- [f5-bigip-kv-configuration-modify-audit-1](CodeChanges/f5-bigip-kv-configuration-modify-audit-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20f5-bigip-kv-configuration-modify-audit-1&type=code)
- [humansecurity-botdefender-json-app-notification-webactivity](CodeChanges/humansecurity-botdefender-json-app-notification-webactivity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20humansecurity-botdefender-json-app-notification-webactivity&type=code)
- [microsoft-sysmon-xml-file-delete-success-23](CodeChanges/microsoft-sysmon-xml-file-delete-success-23.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-sysmon-xml-file-delete-success-23&type=code)
- [microsoft-sysmon-xml-file-delete-success-26](CodeChanges/microsoft-sysmon-xml-file-delete-success-26.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-sysmon-xml-file-delete-success-26&type=code)
- [pan-ngfw-json-app-notification-success-config-catchall](CodeChanges/pan-ngfw-json-app-notification-success-config-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-json-app-notification-success-config-catchall&type=code)
- [pan-ngfw-json-app-notification-success-system-catchall](CodeChanges/pan-ngfw-json-app-notification-success-system-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-json-app-notification-success-system-catchall&type=code)

#### Changed Parsed Fields
<a id="changed-parsed-fields"></a>
- [checkpoint-ngfw-kv-app-activity-newantivirus](CodeChanges/checkpoint-ngfw-kv-app-activity-newantivirus.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-ngfw-kv-app-activity-newantivirus&type=code)
- [google-geminient-json-ai_agent-request-discoveryengine](CodeChanges/google-geminient-json-ai_agent-request-discoveryengine.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20google-geminient-json-ai_agent-request-discoveryengine&type=code)
- [google-geminient-json-ai_agent-request-modelarmor](CodeChanges/google-geminient-json-ai_agent-request-modelarmor.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20google-geminient-json-ai_agent-request-modelarmor&type=code)
- [mimecast-seg-cef-app-login-fail-logonauthfailed](CodeChanges/mimecast-seg-cef-app-login-fail-logonauthfailed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20mimecast-seg-cef-app-login-fail-logonauthfailed&type=code)
- [mimecast-seg-cef-email-url](CodeChanges/mimecast-seg-cef-email-url.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20mimecast-seg-cef-email-url&type=code)
- [vectra-cs-kv-ssh-traffic-success-metadatassh](CodeChanges/vectra-cs-kv-ssh-traffic-success-metadatassh.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vectra-cs-kv-ssh-traffic-success-metadatassh&type=code)
- [zeek-z-str-ssh-traffic-success-sshlog](CodeChanges/zeek-z-str-ssh-traffic-success-sshlog.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zeek-z-str-ssh-traffic-success-sshlog&type=code)

#### Edit Attribute
<a id="edit-attribute"></a>
- [f5-bigip-kv-configuration-modify-audit](CodeChanges/f5-bigip-kv-configuration-modify-audit.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20f5-bigip-kv-configuration-modify-audit&type=code)

#### Edit Regex Field
<a id="edit-regex-field"></a>
- [menlo-ms-json-http-session-security](CodeChanges/menlo-ms-json-http-session-security.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20menlo-ms-json-http-session-security&type=code)
- [microsoft-evsecurity-xml-endpoint-login-4768](CodeChanges/microsoft-evsecurity-xml-endpoint-login-4768.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-login-4768&type=code)
- [microsoft-evsecurity-xml-process-close-4689](CodeChanges/microsoft-evsecurity-xml-process-close-4689.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-process-close-4689&type=code)
- [mimecast-seg-cef-app-login-success-audittype](CodeChanges/mimecast-seg-cef-app-login-success-audittype.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20mimecast-seg-cef-app-login-success-audittype&type=code)
- [mimecast-seg-json-email-eventtype](CodeChanges/mimecast-seg-json-email-eventtype.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20mimecast-seg-json-email-eventtype&type=code)
- [mimecast-seg-sk4-app-activity-success-auditevents](CodeChanges/mimecast-seg-sk4-app-activity-success-auditevents.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20mimecast-seg-sk4-app-activity-success-auditevents&type=code)
- [postgresql-p-str-database-query-success-logaudit](CodeChanges/postgresql-p-str-database-query-success-logaudit.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20postgresql-p-str-database-query-success-logaudit&type=code)
- [trendmicro-officescan-kv-alert-trigger-success-deepsecuritymanager](CodeChanges/trendmicro-officescan-kv-alert-trigger-success-deepsecuritymanager.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20trendmicro-officescan-kv-alert-trigger-success-deepsecuritymanager&type=code)
- [unix-unix-str-endpoint-activity-sshd](CodeChanges/unix-unix-str-endpoint-activity-sshd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-activity-sshd&type=code)

</details>

<details>
<summary><strong id="parsertemplate">ParserTemplate (2)</strong></summary>


### Change Types
- [Added Parser Template](#added-parser-template)
- [Edit Regex Field](#edit-regex-field)

#### Added Parser Template
<a id="added-parser-template"></a>
- [json-ermes-app-activity](CodeChanges/json-ermes-app-activity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20json-ermes-app-activity&type=code)

#### Edit Regex Field
<a id="edit-regex-field"></a>
- [trendmicro-security-alert](CodeChanges/trendmicro-security-alert.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20trendmicro-security-alert&type=code)

</details>