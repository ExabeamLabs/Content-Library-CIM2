# Content Package 2025.25.1

These release notes contain information about content package 2025.25.1, released on 04 Dec 2025.


## Enhancements
- Increase the sequenceExpiryTime for Gemini Enterprise event builders.
- Fixed condition of parser checkpoint-ia-kv-endpoint-login-success-iaevents & checkpoint-ia-kv-vpn-logout-success-logout
- Added new parser radware-waf-json-alert-trigger-security-eaaf for Radware waf
- Updated result_reason regex for google-geminient-json-ai_agent-request-modelarmor parser.
- Updated wiz-w-json-alert-trigger-success-virtualmachine conditions to parse broader category of Wiz logs.
- created new parser jamf-jamfpro-json-security-alerts-jamfprotect for JAMF alerts logs.
- Updated url and web_domain field extractions for microsoft-azuremon-sk4-http-request-success-azurefirewallapplicationrule parser.
- Updated event builder platform to Cisco Network Security for EB - dl-cisco-network-app-notification-success.
- Add a new parser informatica-infocloud-json-app-activity-success-auditlogentry for the Informatica Cloud.
- Added new regex to parse src_host from targetusername in parser microsoft-evsecurity-xml-endpoint-login-success-4624-1
- Added new parsers canon-iradv-csv-endpoint-activity-3001-catchall, canon-iradv-csv-endpoint-activity-8198-catchall & canon-iradv-csv-endpoint-activity-8200-catchall for vendor Canon
- Added new parser workday-wd-json-app-authentication-activesession for vendor Workday
- Removed account field extractions for parser - microsoft-defenderep-cef-endpoint-login-network
- Added new parser fortinet-fortiweb-cef-alert-trigger-success-attack to support unparsed logs.
- Updated dest_ip field extraction for parser - crowdstrike-falcon-mix-dns-request-success-dnsrequest.
- Updated enricher conditions
- Added host, session_id,db_user, result , server_name ,db_query, action , response and src_ip fields for  microsoft-azuremon-sk4-app-activity-loganalyticsomsworkspace parser.
- Added new parser to support unparsed logs .Parser Name - infoblox-bddi-json-alert-trigger-success-alert.
- Adjusted the event builder conditions for the parsers with the Windows EventIds 4779,4720,4724,4768,4663,4769,4743,4740,4722,4672,4674,5145,5142,5144,5143,4673,4742,4726,4624,4625,4778,4776,4657,1102,6272,8004,6273,6278,1009,1149,2000,4780,4654,4981,1200,1202,1203,1201,4957,8002,8001,4738,4105,1000,1530,1030,4653,2887,4658,5379,4655,5447,5152,5061,1001,4100

## Addressed Issues
- Added new parser for Gmail BigQuery collector logs and added JSON field extractions for parser - google-workspace-cef-email-receive.
- Updated host field extraction for parser - pan-ngfw-csv-alert-trigger-success-file.
- Updated  wiz-w-json-alert-trigger-success-virtualmachine parser to include additional fields for parsing Wiz threat and detection logs
- Updated the auth0 parsers to extract user/email_address values only from user_name and removed the regexes extracting user/email from user_id
- Added user_id field for auth0-a-json-endpoint-login-fail-fp parser
- Updated url field extractions for parsers - microsoft-o365-cef-app-file-success-fileupload, microsoft-o365-cef-app-file-success-filemodified, microsoft-o365-cef-app-file-success-filesyncuploadedfull, microsoft-o365-sk4-file-delete-success-filedeleted, microsoft-o365-cef-app-file-success-filedeleted, microsoft-o365-cef-app-file-success-filerenamed, microsoft-o365-cef-app-file-success-filemoved.
- Parsed user as ZPA System User into parser zscaler-pa-json-app-activity-success-update
- Fixed src/dest IP in parser extrahop-revealx-json-dns-request-success-dnsquery
- Updated user regex for parser - cisco-asa-kv-vpn-login-fail-113005.
- Updated the product value to 'Event Viewer  Security' for the Windows Event ID 4735 parsers. Parsers: microsoft-evsecurity-xml-group-modify-success-4735-2 and microsoft-evsecurity-kv-group-modify-success-4735
- Updated process_name,process_dir and process_path regex for microsoft-evsecurity-xml-group-memberlist-4799-1 , microsoft-evsecurity-xml-group-list-4798-1 parser .
- Updated email_address extraction for parser auth0-a-json-app-login-success-s.
- Updated time, host, host_ip field extractions for parser: unix-unix-str-endpoint-activity-sshd
- Updated src_ip, dest_ip, protocol, direction, action, result_code, packets_out,  bytes_out, packets_in, bytes_in fields extraction for parser: microsoft-networkwatcher-json-network-traffic-flowlogevent
- Updated exists condition in the enricher.
- Added new regex to parse src_host from targetusername in parser microsoft-evsecurity-xml-endpoint-login-success-4624-1
- Updated TimeFormat for parsing 7 fractional-second digits in parser - microsoft-evsecurity-xml-user-password-read-success-5382.
- Updated product of cisco-duo-json-endpoint-authentication-result-1 parser and parsed src_ip .

## Code Changes
### ℹ️ How to Read This Document

Each item listed under **Code Changes** includes:

- **A link to a detailed change file**  
  Click the filename (e.g., `Carbon Black.md`) to open a full table showing what changed.

- **A search icon 🔍**  
  Click the 🔍 icon to search for this resource in the [Exabeam Content Library](https://github.com/ExabeamLabs/Content-Library-CIM2).


<details>
<summary><strong id="event-builder">Event Builder (66)</strong></summary>


### Change Types
- [Added Event Builder](#added-event-builder)
- [Edit Conditions](#edit-conditions)
- [Removed Event Builder](#removed-event-builder)

#### Added Event Builder
<a id="added-event-builder"></a>
- [citrix-network-http-request-success-1](CodeChanges/citrix-network-http-request-success-1.md)
- [dl-canon-iradv-endpoint-activity-success-1](CodeChanges/dl-canon-iradv-endpoint-activity-success-1.md)
- [dl-infoblox-bloxoneddi-alert-trigger-success](CodeChanges/dl-infoblox-bloxoneddi-alert-trigger-success.md)
- [dl-informatica-cloud-app-activity-success](CodeChanges/dl-informatica-cloud-app-activity-success.md)
- [dl-jamf-jamfpro-security-alert-success](CodeChanges/dl-jamf-jamfpro-security-alert-success.md)
- [dl-microsoft-ad-endpoint-authentication-fail](CodeChanges/dl-microsoft-ad-endpoint-authentication-fail.md)
- [dl-microsoft-windows-endpoint-activity-success-7](CodeChanges/dl-microsoft-windows-endpoint-activity-success-7.md)
- [dl-microsoft-windows-endpoint-activity-success-8](CodeChanges/dl-microsoft-windows-endpoint-activity-success-8.md)
- [google-workspace-app-activity-fail](CodeChanges/google-workspace-app-activity-fail.md)
- [google-workspace-app-activity-success-4](CodeChanges/google-workspace-app-activity-success-4.md)
- [jamf-jamfpro-security-alert-success](CodeChanges/jamf-jamfpro-security-alert-success.md)
- [microsoft-ad-endpoint-delete-success-2](CodeChanges/microsoft-ad-endpoint-delete-success-2.md)
- [microsoft-windows-endpoint-authentication-fail-3](CodeChanges/microsoft-windows-endpoint-authentication-fail-3.md)
- [microsoft-windows-endpoint-authentication-fail-6](CodeChanges/microsoft-windows-endpoint-authentication-fail-6.md)
- [microsoft-windows-endpoint-authentication-success-6](CodeChanges/microsoft-windows-endpoint-authentication-success-6.md)
- [microsoft-windows-endpoint-authentication-success-7](CodeChanges/microsoft-windows-endpoint-authentication-success-7.md)
- [microsoft-windows-share-access-fail-4](CodeChanges/microsoft-windows-share-access-fail-4.md)
- [microsoft-windows-share-access-success-4](CodeChanges/microsoft-windows-share-access-success-4.md)
- [microsoft-windows-share-access-success-5](CodeChanges/microsoft-windows-share-access-success-5.md)
- [microsoft-windows-vpn-login-fail-1](CodeChanges/microsoft-windows-vpn-login-fail-1.md)
- [radware-waf-alert-trigger-success](CodeChanges/radware-waf-alert-trigger-success.md)
- [workday-wd-app-authentication-successful-1](CodeChanges/workday-wd-app-authentication-successful-1.md)

#### Edit Conditions
<a id="edit-conditions"></a>
- [cisco-network-network-traffic-fail-5](CodeChanges/cisco-network-network-traffic-fail-5.md)
- [cisco-network-network-traffic-success-3](CodeChanges/cisco-network-network-traffic-success-3.md)
- [dl-wiz-alert-trigger-success-1](CodeChanges/dl-wiz-alert-trigger-success-1.md)
- [microsoft-ad-endpoint-authentication-fail-3](CodeChanges/microsoft-ad-endpoint-authentication-fail-3.md)
- [microsoft-windows-endpoint-authentication-success](CodeChanges/microsoft-windows-endpoint-authentication-success.md)
- [microsoft-windows-endpoint-logout-success-1](CodeChanges/microsoft-windows-endpoint-logout-success-1.md)
- [microsoft-windows-registry-create-success](CodeChanges/microsoft-windows-registry-create-success.md)
- [microsoft-windows-share-access-fail-2](CodeChanges/microsoft-windows-share-access-fail-2.md)
- [microsoft-windows-share-access-fail-3](CodeChanges/microsoft-windows-share-access-fail-3.md)
- [microsoft-windows-share-access-success-3](CodeChanges/microsoft-windows-share-access-success-3.md)
- [microsoft-windows-share-delete-success](CodeChanges/microsoft-windows-share-delete-success.md)
- [microsoft-windows-share-modify-success](CodeChanges/microsoft-windows-share-modify-success.md)
- [wiz-alert-trigger-success-1](CodeChanges/wiz-alert-trigger-success-1.md)

#### Removed Event Builder
<a id="removed-event-builder"></a>
- [citrix-network-http-session-success-1](CodeChanges/citrix-network-http-session-success-1.md)
- [dl-manageengine-windows-app-authentication-success](CodeChanges/dl-manageengine-windows-app-authentication-success.md)
- [dl-microsoft-network-network-session-fail-1](CodeChanges/dl-microsoft-network-network-session-fail-1.md)
- [dl-microsoft-network-network-session-success-1](CodeChanges/dl-microsoft-network-network-session-success-1.md)
- [dl-microsoft-windows-app-activity-success-1](CodeChanges/dl-microsoft-windows-app-activity-success-1.md)
- [dl-microsoft-windows-network-traffic-success](CodeChanges/dl-microsoft-windows-network-traffic-success.md)
- [dl-microsoft-windows-user-modify-success-1](CodeChanges/dl-microsoft-windows-user-modify-success-1.md)
- [dl-microsoft-windows-user-password-read-success](CodeChanges/dl-microsoft-windows-user-password-read-success.md)
- [micosoft-windows-rdp-traffic-success](CodeChanges/micosoft-windows-rdp-traffic-success.md)
- [microsoft-ad-user-delete-fail](CodeChanges/microsoft-ad-user-delete-fail.md)
- [microsoft-ad-user-delete-success](CodeChanges/microsoft-ad-user-delete-success.md)
- [microsoft-ad-user-delete-success-1](CodeChanges/microsoft-ad-user-delete-success-1.md)
- [microsoft-networkpolicyserver-endpoint-login-success](CodeChanges/microsoft-networkpolicyserver-endpoint-login-success.md)
- [microsoft-nps-endpoint-authentication-success](CodeChanges/microsoft-nps-endpoint-authentication-success.md)
- [microsoft-windows-endpoint-login-fail-3](CodeChanges/microsoft-windows-endpoint-login-fail-3.md)
- [microsoft-windows-endpoint-login-success-1](CodeChanges/microsoft-windows-endpoint-login-success-1.md)
- [microsoft-windows-endpoint-login-success-7](CodeChanges/microsoft-windows-endpoint-login-success-7.md)
- [microsoft-windows-radius-traffic-success-1](CodeChanges/microsoft-windows-radius-traffic-success-1.md)
- [microsoft-windows-rdp-traffic-success-1](CodeChanges/microsoft-windows-rdp-traffic-success-1.md)
- [microsoft-windows-rdp-traffic-success-3](CodeChanges/microsoft-windows-rdp-traffic-success-3.md)
- [microsoft-windows-share-access-fail-1](CodeChanges/microsoft-windows-share-access-fail-1.md)
- [microsoft-windows-share-access-success-1](CodeChanges/microsoft-windows-share-access-success-1.md)
- [microsoft-windows-share-access-success-2](CodeChanges/microsoft-windows-share-access-success-2.md)
- [microsoft-windows-share-create-success-1](CodeChanges/microsoft-windows-share-create-success-1.md)
- [microsoft-windows-share-delete-success-1](CodeChanges/microsoft-windows-share-delete-success-1.md)
- [microsoft-windows-share-modify-success-1](CodeChanges/microsoft-windows-share-modify-success-1.md)
- [microsoft-windows-user-create-success-1](CodeChanges/microsoft-windows-user-create-success-1.md)
- [microsoft-windows-user-enable-success-1](CodeChanges/microsoft-windows-user-enable-success-1.md)
- [microsoft-windows-user-privilege-modify-fail](CodeChanges/microsoft-windows-user-privilege-modify-fail.md)
- [microsoft-windows-user-privilege-modify-success](CodeChanges/microsoft-windows-user-privilege-modify-success.md)
- [microsoft-windows-user-privilege-use-success-3](CodeChanges/microsoft-windows-user-privilege-use-success-3.md)

</details>

<details>
<summary><strong id="parser">Parser (384)</strong></summary>


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
- [dell-emcisilon-str-file-rename-smb](CodeChanges/dell-emcisilon-str-file-rename-smb.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20dell-emcisilon-str-file-rename-smb&type=code)
- [dell-isilon-str-file-permission-modify-set_security](CodeChanges/dell-isilon-str-file-permission-modify-set_security.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20dell-isilon-str-file-permission-modify-set_security&type=code)
- [microsoft-evsecurity-xml-user-password-read-success-5382](CodeChanges/microsoft-evsecurity-xml-user-password-read-success-5382.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-user-password-read-success-5382&type=code)
- [wiz-w-json-alert-trigger-success-virtualmachine](CodeChanges/wiz-w-json-alert-trigger-success-virtualmachine.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20wiz-w-json-alert-trigger-success-virtualmachine&type=code)

#### Added Parser
<a id="added-parser"></a>
- [canon-iradv-csv-endpoint-activity-3001-catchall](CodeChanges/canon-iradv-csv-endpoint-activity-3001-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20canon-iradv-csv-endpoint-activity-3001-catchall&type=code)
- [canon-iradv-csv-endpoint-activity-8198-catchall](CodeChanges/canon-iradv-csv-endpoint-activity-8198-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20canon-iradv-csv-endpoint-activity-8198-catchall&type=code)
- [canon-iradv-csv-endpoint-activity-8200-catchall](CodeChanges/canon-iradv-csv-endpoint-activity-8200-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20canon-iradv-csv-endpoint-activity-8200-catchall&type=code)
- [citrix-cgateway-str-http-request-success-sslvpn](CodeChanges/citrix-cgateway-str-http-request-success-sslvpn.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20citrix-cgateway-str-http-request-success-sslvpn&type=code)
- [fortinet-fortiweb-cef-alert-trigger-success-attack](CodeChanges/fortinet-fortiweb-cef-alert-trigger-success-attack.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20fortinet-fortiweb-cef-alert-trigger-success-attack&type=code)
- [google-workspace-json-app-activity-eventinfo](CodeChanges/google-workspace-json-app-activity-eventinfo.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20google-workspace-json-app-activity-eventinfo&type=code)
- [infoblox-bddi-json-alert-trigger-success-alert](CodeChanges/infoblox-bddi-json-alert-trigger-success-alert.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-json-alert-trigger-success-alert&type=code)
- [informatica-infocloud-json-app-activity-success-auditlogentry](CodeChanges/informatica-infocloud-json-app-activity-success-auditlogentry.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20informatica-infocloud-json-app-activity-success-auditlogentry&type=code)
- [jamf-jamfpro-json-security-alerts-jamfprotect](CodeChanges/jamf-jamfpro-json-security-alerts-jamfprotect.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20jamf-jamfpro-json-security-alerts-jamfprotect&type=code)
- [microsoft-365defender-json-alert-trigger-success-behaviorentities](CodeChanges/microsoft-365defender-json-alert-trigger-success-behaviorentities.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-365defender-json-alert-trigger-success-behaviorentities&type=code)
- [microsoft-365defender-json-alert-trigger-success-behaviorinfo](CodeChanges/microsoft-365defender-json-alert-trigger-success-behaviorinfo.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-365defender-json-alert-trigger-success-behaviorinfo&type=code)
- [radware-waf-json-alert-trigger-security-eaaf](CodeChanges/radware-waf-json-alert-trigger-security-eaaf.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20radware-waf-json-alert-trigger-security-eaaf&type=code)
- [workday-wd-json-app-authentication-activesession](CodeChanges/workday-wd-json-app-authentication-activesession.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20workday-wd-json-app-authentication-activesession&type=code)

#### Changed
<a id="changed"></a>
- [checkpoint-ia-kv-endpoint-login-success-iaevents](CodeChanges/checkpoint-ia-kv-endpoint-login-success-iaevents.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-ia-kv-endpoint-login-success-iaevents&type=code)
- [checkpoint-ia-kv-vpn-logout-success-logout](CodeChanges/checkpoint-ia-kv-vpn-logout-success-logout.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-ia-kv-vpn-logout-success-logout&type=code)

#### Changed Parsed Fields
<a id="changed-parsed-fields"></a>
- [cisco-duo-json-endpoint-authentication-result-1](CodeChanges/cisco-duo-json-endpoint-authentication-result-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-duo-json-endpoint-authentication-result-1&type=code)
- [crowdstrike-falcon-json-network-traffic-success-connectip](CodeChanges/crowdstrike-falcon-json-network-traffic-success-connectip.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-network-traffic-success-connectip&type=code)
- [google-geminient-json-ai_agent-request-modelarmor](CodeChanges/google-geminient-json-ai_agent-request-modelarmor.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20google-geminient-json-ai_agent-request-modelarmor&type=code)
- [microsoft-365defender-json-alert-trigger-success-publish](CodeChanges/microsoft-365defender-json-alert-trigger-success-publish.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-365defender-json-alert-trigger-success-publish&type=code)
- [microsoft-365defender-json-alert-trigger-success-publish-1](CodeChanges/microsoft-365defender-json-alert-trigger-success-publish-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-365defender-json-alert-trigger-success-publish-1&type=code)
- [microsoft-azure-sk4-app-file-success-keybackup](CodeChanges/microsoft-azure-sk4-app-file-success-keybackup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-sk4-app-file-success-keybackup&type=code)
- [microsoft-azure-sk4-app-file-success-secretget](CodeChanges/microsoft-azure-sk4-app-file-success-secretget.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-sk4-app-file-success-secretget&type=code)
- [microsoft-azuremon-sk4-http-request-success-azurefirewallapplicationrule](CodeChanges/microsoft-azuremon-sk4-http-request-success-azurefirewallapplicationrule.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-sk4-http-request-success-azurefirewallapplicationrule&type=code)
- [microsoft-defenderep-cef-endpoint-login-batch](CodeChanges/microsoft-defenderep-cef-endpoint-login-batch.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-cef-endpoint-login-batch&type=code)
- [microsoft-defenderep-cef-endpoint-login-interactive](CodeChanges/microsoft-defenderep-cef-endpoint-login-interactive.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-cef-endpoint-login-interactive&type=code)
- [microsoft-defenderep-cef-endpoint-login-network](CodeChanges/microsoft-defenderep-cef-endpoint-login-network.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-cef-endpoint-login-network&type=code)
- [microsoft-defenderep-cef-endpoint-login-service](CodeChanges/microsoft-defenderep-cef-endpoint-login-service.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-cef-endpoint-login-service&type=code)
- [microsoft-evsecurity-kv-share-access-success-5145](CodeChanges/microsoft-evsecurity-kv-share-access-success-5145.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-share-access-success-5145&type=code)
- [microsoft-o365-cef-app-file-success-addapplication](CodeChanges/microsoft-o365-cef-app-file-success-addapplication.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-addapplication&type=code)
- [microsoft-o365-cef-app-file-success-addgroup](CodeChanges/microsoft-o365-cef-app-file-success-addgroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-addgroup&type=code)
- [microsoft-o365-cef-app-file-success-addmembertorole](CodeChanges/microsoft-o365-cef-app-file-success-addmembertorole.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-addmembertorole&type=code)
- [microsoft-o365-cef-app-file-success-addownertogroup](CodeChanges/microsoft-o365-cef-app-file-success-addownertogroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-addownertogroup&type=code)
- [microsoft-o365-cef-app-file-success-addtogroup](CodeChanges/microsoft-o365-cef-app-file-success-addtogroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-addtogroup&type=code)
- [microsoft-o365-cef-app-file-success-adduser](CodeChanges/microsoft-o365-cef-app-file-success-adduser.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-adduser&type=code)
- [microsoft-o365-cef-app-file-success-channeladded](CodeChanges/microsoft-o365-cef-app-file-success-channeladded.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-channeladded&type=code)
- [microsoft-o365-cef-app-file-success-channeldeleted](CodeChanges/microsoft-o365-cef-app-file-success-channeldeleted.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-channeldeleted&type=code)
- [microsoft-o365-cef-app-file-success-crmdefaultactivity](CodeChanges/microsoft-o365-cef-app-file-success-crmdefaultactivity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-crmdefaultactivity&type=code)
- [microsoft-o365-cef-app-file-success-deletegroup](CodeChanges/microsoft-o365-cef-app-file-success-deletegroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-deletegroup&type=code)
- [microsoft-o365-cef-app-file-success-deleteuser](CodeChanges/microsoft-o365-cef-app-file-success-deleteuser.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-deleteuser&type=code)
- [microsoft-o365-cef-app-file-success-displayname](CodeChanges/microsoft-o365-cef-app-file-success-displayname.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-displayname&type=code)
- [microsoft-o365-cef-app-file-success-downloadreport](CodeChanges/microsoft-o365-cef-app-file-success-downloadreport.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-downloadreport&type=code)
- [microsoft-o365-cef-app-file-success-filedeleted](CodeChanges/microsoft-o365-cef-app-file-success-filedeleted.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-filedeleted&type=code)
- [microsoft-o365-cef-app-file-success-filemodified](CodeChanges/microsoft-o365-cef-app-file-success-filemodified.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-filemodified&type=code)
- [microsoft-o365-cef-app-file-success-filemoved](CodeChanges/microsoft-o365-cef-app-file-success-filemoved.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-filemoved&type=code)
- [microsoft-o365-cef-app-file-success-filerenamed](CodeChanges/microsoft-o365-cef-app-file-success-filerenamed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-filerenamed&type=code)
- [microsoft-o365-cef-app-file-success-filesyncuploadedfull](CodeChanges/microsoft-o365-cef-app-file-success-filesyncuploadedfull.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-filesyncuploadedfull&type=code)
- [microsoft-o365-cef-app-file-success-fileupload](CodeChanges/microsoft-o365-cef-app-file-success-fileupload.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-fileupload&type=code)
- [microsoft-o365-cef-app-file-success-foldercreated](CodeChanges/microsoft-o365-cef-app-file-success-foldercreated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-foldercreated&type=code)
- [microsoft-o365-cef-app-file-success-groupupload](CodeChanges/microsoft-o365-cef-app-file-success-groupupload.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-groupupload&type=code)
- [microsoft-o365-cef-app-file-success-harddelete](CodeChanges/microsoft-o365-cef-app-file-success-harddelete.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-harddelete&type=code)
- [microsoft-o365-cef-app-file-success-memberadded](CodeChanges/microsoft-o365-cef-app-file-success-memberadded.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-memberadded&type=code)
- [microsoft-o365-cef-app-file-success-memberremoved](CodeChanges/microsoft-o365-cef-app-file-success-memberremoved.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-memberremoved&type=code)
- [microsoft-o365-cef-app-file-success-modifiedproperties](CodeChanges/microsoft-o365-cef-app-file-success-modifiedproperties.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-modifiedproperties&type=code)
- [microsoft-o365-cef-app-file-success-movetodeleteditems](CodeChanges/microsoft-o365-cef-app-file-success-movetodeleteditems.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-movetodeleteditems&type=code)
- [microsoft-o365-cef-app-file-success-refreshdataset](CodeChanges/microsoft-o365-cef-app-file-success-refreshdataset.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-refreshdataset&type=code)
- [microsoft-o365-cef-app-file-success-removememberfromgroup](CodeChanges/microsoft-o365-cef-app-file-success-removememberfromgroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-removememberfromgroup&type=code)
- [microsoft-o365-cef-app-file-success-restoreuser](CodeChanges/microsoft-o365-cef-app-file-success-restoreuser.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-restoreuser&type=code)
- [microsoft-o365-cef-app-file-success-rolechanged](CodeChanges/microsoft-o365-cef-app-file-success-rolechanged.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-rolechanged&type=code)
- [microsoft-o365-cef-app-file-success-serviceprincipal](CodeChanges/microsoft-o365-cef-app-file-success-serviceprincipal.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-serviceprincipal&type=code)
- [microsoft-o365-cef-app-file-success-storageanalyticsevents](CodeChanges/microsoft-o365-cef-app-file-success-storageanalyticsevents.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-storageanalyticsevents&type=code)
- [microsoft-o365-cef-app-file-success-tabadded](CodeChanges/microsoft-o365-cef-app-file-success-tabadded.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-tabadded&type=code)
- [microsoft-o365-cef-app-file-success-tabupdated](CodeChanges/microsoft-o365-cef-app-file-success-tabupdated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-tabupdated&type=code)
- [microsoft-o365-cef-app-file-success-updatedevice](CodeChanges/microsoft-o365-cef-app-file-success-updatedevice.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-updatedevice&type=code)
- [microsoft-o365-cef-app-file-success-updateuser](CodeChanges/microsoft-o365-cef-app-file-success-updateuser.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-updateuser&type=code)
- [microsoft-o365-cef-app-file-success-viewdashboard](CodeChanges/microsoft-o365-cef-app-file-success-viewdashboard.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-viewdashboard&type=code)
- [microsoft-o365-cef-app-file-success-viewreport](CodeChanges/microsoft-o365-cef-app-file-success-viewreport.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-viewreport&type=code)
- [microsoft-o365-cef-user-password-reset-selfservice](CodeChanges/microsoft-o365-cef-user-password-reset-selfservice.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-user-password-reset-selfservice&type=code)
- [microsoft-o365-sk4-app-activity-success-addedtogroup](CodeChanges/microsoft-o365-sk4-app-activity-success-addedtogroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-sk4-app-activity-success-addedtogroup&type=code)
- [microsoft-o365-sk4-app-file-success-viewdashboard](CodeChanges/microsoft-o365-sk4-app-file-success-viewdashboard.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-sk4-app-file-success-viewdashboard&type=code)
- [microsoft-o365-sk4-file-delete-success-filedeleted](CodeChanges/microsoft-o365-sk4-file-delete-success-filedeleted.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-sk4-file-delete-success-filedeleted&type=code)
- [microsoft-windows-sk4-group-list-success-4798](CodeChanges/microsoft-windows-sk4-group-list-success-4798.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-windows-sk4-group-list-success-4798&type=code)
- [zyxel-usgflex-kv-alert-trigger-success-ips](CodeChanges/zyxel-usgflex-kv-alert-trigger-success-ips.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zyxel-usgflex-kv-alert-trigger-success-ips&type=code)
- [zyxel-usgflex-kv-network-notification-success-msg](CodeChanges/zyxel-usgflex-kv-network-notification-success-msg.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zyxel-usgflex-kv-network-notification-success-msg&type=code)
- [zyxel-usgflex-kv-network-session-fail-accessblock](CodeChanges/zyxel-usgflex-kv-network-session-fail-accessblock.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zyxel-usgflex-kv-network-session-fail-accessblock&type=code)
- [zyxel-usgflex-kv-network-session-fail-sessionlimit](CodeChanges/zyxel-usgflex-kv-network-session-fail-sessionlimit.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zyxel-usgflex-kv-network-session-fail-sessionlimit&type=code)

#### Edit Attribute
<a id="edit-attribute"></a>
- [cisco-asa-str-alert-trigger-ethport3](CodeChanges/cisco-asa-str-alert-trigger-ethport3.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-alert-trigger-ethport3&type=code)
- [cisco-asa-str-app-notification-110002](CodeChanges/cisco-asa-str-app-notification-110002.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-110002&type=code)
- [cisco-asa-str-app-notification-3](CodeChanges/cisco-asa-str-app-notification-3.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-3&type=code)
- [cisco-asa-str-app-notification-5](CodeChanges/cisco-asa-str-app-notification-5.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-5&type=code)
- [cisco-asa-str-app-notification-7398](CodeChanges/cisco-asa-str-app-notification-7398.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-7398&type=code)
- [cisco-asa-str-app-notification-coresavefailed](CodeChanges/cisco-asa-str-app-notification-coresavefailed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-coresavefailed&type=code)
- [cisco-asa-str-app-notification-iftxflowcontrol](CodeChanges/cisco-asa-str-app-notification-iftxflowcontrol.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-iftxflowcontrol&type=code)
- [cisco-asa-str-app-notification-lineproto](CodeChanges/cisco-asa-str-app-notification-lineproto.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-lineproto&type=code)
- [cisco-asa-str-app-notification-success-1240](CodeChanges/cisco-asa-str-app-notification-success-1240.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-1240&type=code)
- [cisco-asa-str-app-notification-success-basictrace](CodeChanges/cisco-asa-str-app-notification-success-basictrace.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-basictrace&type=code)
- [cisco-asa-str-app-notification-success-cdp](CodeChanges/cisco-asa-str-app-notification-success-cdp.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-cdp&type=code)
- [cisco-asa-str-app-notification-success-cslu](CodeChanges/cisco-asa-str-app-notification-success-cslu.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-cslu&type=code)
- [cisco-asa-str-app-notification-success-dual](CodeChanges/cisco-asa-str-app-notification-success-dual.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-dual&type=code)
- [cisco-asa-str-app-notification-success-ethport](CodeChanges/cisco-asa-str-app-notification-success-ethport.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-ethport&type=code)
- [cisco-asa-str-app-notification-success-ethport-1](CodeChanges/cisco-asa-str-app-notification-success-ethport-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-ethport-1&type=code)
- [cisco-asa-str-app-notification-success-hsrp](CodeChanges/cisco-asa-str-app-notification-success-hsrp.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-hsrp&type=code)
- [cisco-asa-str-app-notification-success-l2fm](CodeChanges/cisco-asa-str-app-notification-success-l2fm.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-l2fm&type=code)
- [cisco-asa-str-app-notification-success-pdt](CodeChanges/cisco-asa-str-app-notification-success-pdt.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-pdt&type=code)
- [cisco-asa-str-app-notification-success-platform](CodeChanges/cisco-asa-str-app-notification-success-platform.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-platform&type=code)
- [cisco-asa-str-app-notification-success-sfpwarning](CodeChanges/cisco-asa-str-app-notification-success-sfpwarning.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-sfpwarning&type=code)
- [cisco-asa-str-app-notification-success-sip](CodeChanges/cisco-asa-str-app-notification-success-sip.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-sip&type=code)
- [cisco-asa-str-app-notification-success-swmatm](CodeChanges/cisco-asa-str-app-notification-success-swmatm.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-swmatm&type=code)
- [cisco-asa-str-app-notification-success-sys](CodeChanges/cisco-asa-str-app-notification-success-sys.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-sys&type=code)
- [cisco-asa-str-app-notification-success-timeshift](CodeChanges/cisco-asa-str-app-notification-success-timeshift.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-timeshift&type=code)
- [cisco-asa-str-app-notification-success-track](CodeChanges/cisco-asa-str-app-notification-success-track.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-track&type=code)
- [cisco-asa-str-app-notification-success-ttyexpire](CodeChanges/cisco-asa-str-app-notification-success-ttyexpire.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-ttyexpire&type=code)
- [cisco-asa-str-app-notification-success-ucsm](CodeChanges/cisco-asa-str-app-notification-success-ucsm.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-ucsm&type=code)
- [cisco-asa-str-app-notification-thresholdviolation](CodeChanges/cisco-asa-str-app-notification-thresholdviolation.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-thresholdviolation&type=code)
- [cisco-fp-kv-app-notification-success-752003](CodeChanges/cisco-fp-kv-app-notification-success-752003.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-fp-kv-app-notification-success-752003&type=code)
- [cisco-fp-str-app-notification-success-722010](CodeChanges/cisco-fp-str-app-notification-success-722010.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-fp-str-app-notification-success-722010&type=code)
- [manageengine-adauditplus-kv-app-authentication-2887](CodeChanges/manageengine-adauditplus-kv-app-authentication-2887.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20manageengine-adauditplus-kv-app-authentication-2887&type=code)
- [microsoft-evadfs-kv-endpoint-login-fail-1201](CodeChanges/microsoft-evadfs-kv-endpoint-login-fail-1201.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evadfs-kv-endpoint-login-fail-1201&type=code)
- [microsoft-evadfs-kv-endpoint-login-fail-1203](CodeChanges/microsoft-evadfs-kv-endpoint-login-fail-1203.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evadfs-kv-endpoint-login-fail-1203&type=code)
- [microsoft-evadfs-kv-endpoint-login-success-1149](CodeChanges/microsoft-evadfs-kv-endpoint-login-success-1149.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evadfs-kv-endpoint-login-success-1149&type=code)
- [microsoft-evadfs-kv-log-clear-success-1102](CodeChanges/microsoft-evadfs-kv-log-clear-success-1102.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evadfs-kv-log-clear-success-1102&type=code)
- [microsoft-evadfs-xml-rdp-traffic-success-1149](CodeChanges/microsoft-evadfs-xml-rdp-traffic-success-1149.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evadfs-xml-rdp-traffic-success-1149&type=code)
- [microsoft-evapp-kv-endpoint-activity-success-1530](CodeChanges/microsoft-evapp-kv-endpoint-activity-success-1530.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-kv-endpoint-activity-success-1530&type=code)
- [microsoft-evapp-str-endpoint-notification-1202](CodeChanges/microsoft-evapp-str-endpoint-notification-1202.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-str-endpoint-notification-1202&type=code)
- [microsoft-evapplocker-cef-endpoint-notification-8002](CodeChanges/microsoft-evapplocker-cef-endpoint-notification-8002.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapplocker-cef-endpoint-notification-8002&type=code)
- [microsoft-evnps-kv-endpoint-login-success-6272](CodeChanges/microsoft-evnps-kv-endpoint-login-success-6272.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evnps-kv-endpoint-login-success-6272&type=code)
- [microsoft-evnps-kv-radius-traffic-fail-6273](CodeChanges/microsoft-evnps-kv-radius-traffic-fail-6273.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evnps-kv-radius-traffic-fail-6273&type=code)
- [microsoft-evnps-xml-radius-traffic-success-6272](CodeChanges/microsoft-evnps-xml-radius-traffic-success-6272.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evnps-xml-radius-traffic-success-6272&type=code)
- [microsoft-evntlm-kv-endpoint-login-fail-8004](CodeChanges/microsoft-evntlm-kv-endpoint-login-fail-8004.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evntlm-kv-endpoint-login-fail-8004&type=code)
- [microsoft-evntlm-str-app-authentication-fail-8004](CodeChanges/microsoft-evntlm-str-app-authentication-fail-8004.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evntlm-str-app-authentication-fail-8004&type=code)
- [microsoft-evntlm-xml-endpoint-login-fail-8004](CodeChanges/microsoft-evntlm-xml-endpoint-login-fail-8004.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evntlm-xml-endpoint-login-fail-8004&type=code)
- [microsoft-evntlm-xml-endpoint-login-success-8001](CodeChanges/microsoft-evntlm-xml-endpoint-login-success-8001.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evntlm-xml-endpoint-login-success-8001&type=code)
- [microsoft-evntlm-xml-endpoint-login-success-8002](CodeChanges/microsoft-evntlm-xml-endpoint-login-success-8002.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evntlm-xml-endpoint-login-success-8002&type=code)
- [microsoft-evsecurity-cef-app-notification-5061](CodeChanges/microsoft-evsecurity-cef-app-notification-5061.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-app-notification-5061&type=code)
- [microsoft-evsecurity-cef-ds-object-activity-success-4742](CodeChanges/microsoft-evsecurity-cef-ds-object-activity-success-4742.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-ds-object-activity-success-4742&type=code)
- [microsoft-evsecurity-cef-endpoint-authentication-success-4658](CodeChanges/microsoft-evsecurity-cef-endpoint-authentication-success-4658.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-endpoint-authentication-success-4658&type=code)
- [microsoft-evsecurity-cef-endpoint-authentication-success-4769](CodeChanges/microsoft-evsecurity-cef-endpoint-authentication-success-4769.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-endpoint-authentication-success-4769&type=code)
- [microsoft-evsecurity-cef-endpoint-login-4769-1](CodeChanges/microsoft-evsecurity-cef-endpoint-login-4769-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-endpoint-login-4769-1&type=code)
- [microsoft-evsecurity-cef-endpoint-login-4769-7](CodeChanges/microsoft-evsecurity-cef-endpoint-login-4769-7.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-endpoint-login-4769-7&type=code)
- [microsoft-evsecurity-cef-endpoint-notification-success-4654](CodeChanges/microsoft-evsecurity-cef-endpoint-notification-success-4654.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-endpoint-notification-success-4654&type=code)
- [microsoft-evsecurity-cef-network-session-fail-4653](CodeChanges/microsoft-evsecurity-cef-network-session-fail-4653.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-network-session-fail-4653&type=code)
- [microsoft-evsecurity-cef-network-traffic-success-5152](CodeChanges/microsoft-evsecurity-cef-network-traffic-success-5152.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-network-traffic-success-5152&type=code)
- [microsoft-evsecurity-cef-share-access-success-5142](CodeChanges/microsoft-evsecurity-cef-share-access-success-5142.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-share-access-success-5142&type=code)
- [microsoft-evsecurity-cef-share-access-success-5143](CodeChanges/microsoft-evsecurity-cef-share-access-success-5143.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-share-access-success-5143&type=code)
- [microsoft-evsecurity-cef-share-access-success-5144](CodeChanges/microsoft-evsecurity-cef-share-access-success-5144.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-share-access-success-5144&type=code)
- [microsoft-evsecurity-cef-user-delete-success-4743](CodeChanges/microsoft-evsecurity-cef-user-delete-success-4743.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-user-delete-success-4743&type=code)
- [microsoft-evsecurity-cef-user-privilege-assign-success-4672](CodeChanges/microsoft-evsecurity-cef-user-privilege-assign-success-4672.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-user-privilege-assign-success-4672&type=code)
- [microsoft-evsecurity-cef-user-privilege-assign-success-4673](CodeChanges/microsoft-evsecurity-cef-user-privilege-assign-success-4673.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-user-privilege-assign-success-4673&type=code)
- [microsoft-evsecurity-csv-endpoint-login-4769](CodeChanges/microsoft-evsecurity-csv-endpoint-login-4769.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-csv-endpoint-login-4769&type=code)
- [microsoft-evsecurity-csv-user-privilege-modify-success-4672](CodeChanges/microsoft-evsecurity-csv-user-privilege-modify-success-4672.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-csv-user-privilege-modify-success-4672&type=code)
- [microsoft-evsecurity-json-ds-object-modify-success-4742](CodeChanges/microsoft-evsecurity-json-ds-object-modify-success-4742.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-ds-object-modify-success-4742&type=code)
- [microsoft-evsecurity-json-endpoint-kerberosauth](CodeChanges/microsoft-evsecurity-json-endpoint-kerberosauth.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-endpoint-kerberosauth&type=code)
- [microsoft-evsecurity-json-endpoint-login-4769](CodeChanges/microsoft-evsecurity-json-endpoint-login-4769.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-endpoint-login-4769&type=code)
- [microsoft-evsecurity-json-endpoint-login-4769-1](CodeChanges/microsoft-evsecurity-json-endpoint-login-4769-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-endpoint-login-4769-1&type=code)
- [microsoft-evsecurity-json-endpoint-login-4769-3](CodeChanges/microsoft-evsecurity-json-endpoint-login-4769-3.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-endpoint-login-4769-3&type=code)
- [microsoft-evsecurity-json-endpoint-login-4769-4](CodeChanges/microsoft-evsecurity-json-endpoint-login-4769-4.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-endpoint-login-4769-4&type=code)
- [microsoft-evsecurity-json-endpoint-login-4769-5](CodeChanges/microsoft-evsecurity-json-endpoint-login-4769-5.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-endpoint-login-4769-5&type=code)
- [microsoft-evsecurity-json-endpoint-login-4769-7](CodeChanges/microsoft-evsecurity-json-endpoint-login-4769-7.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-endpoint-login-4769-7&type=code)
- [microsoft-evsecurity-json-endpoint-login-4769-8](CodeChanges/microsoft-evsecurity-json-endpoint-login-4769-8.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-endpoint-login-4769-8&type=code)
- [microsoft-evsecurity-json-endpoint-login-4769-9](CodeChanges/microsoft-evsecurity-json-endpoint-login-4769-9.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-endpoint-login-4769-9&type=code)
- [microsoft-evsecurity-json-network-session-fail-4653](CodeChanges/microsoft-evsecurity-json-network-session-fail-4653.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-network-session-fail-4653&type=code)
- [microsoft-evsecurity-json-rdp-traffic-success-4778](CodeChanges/microsoft-evsecurity-json-rdp-traffic-success-4778.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-rdp-traffic-success-4778&type=code)
- [microsoft-evsecurity-json-share-access-success-5145](CodeChanges/microsoft-evsecurity-json-share-access-success-5145.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-share-access-success-5145&type=code)
- [microsoft-evsecurity-json-user-privilege-assign-success-4672](CodeChanges/microsoft-evsecurity-json-user-privilege-assign-success-4672.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-user-privilege-assign-success-4672&type=code)
- [microsoft-evsecurity-json-user-privilege-assign-success-4672-4](CodeChanges/microsoft-evsecurity-json-user-privilege-assign-success-4672-4.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-user-privilege-assign-success-4672-4&type=code)
- [microsoft-evsecurity-json-user-privilege-assign-success-4672-5](CodeChanges/microsoft-evsecurity-json-user-privilege-assign-success-4672-5.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-user-privilege-assign-success-4672-5&type=code)
- [microsoft-evsecurity-json-user-privilege-assign-success-4672-6](CodeChanges/microsoft-evsecurity-json-user-privilege-assign-success-4672-6.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-user-privilege-assign-success-4672-6&type=code)
- [microsoft-evsecurity-json-user-privilege-assign-success-4673](CodeChanges/microsoft-evsecurity-json-user-privilege-assign-success-4673.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-user-privilege-assign-success-4673&type=code)
- [microsoft-evsecurity-json-user-privilege-assign-success-4673-1](CodeChanges/microsoft-evsecurity-json-user-privilege-assign-success-4673-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-user-privilege-assign-success-4673-1&type=code)
- [microsoft-evsecurity-kv-ds-object-modify-success-4738](CodeChanges/microsoft-evsecurity-kv-ds-object-modify-success-4738.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-ds-object-modify-success-4738&type=code)
- [microsoft-evsecurity-kv-ds-object-modify-success-4742](CodeChanges/microsoft-evsecurity-kv-ds-object-modify-success-4742.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-ds-object-modify-success-4742&type=code)
- [microsoft-evsecurity-kv-endpoint-authentication-success-4776](CodeChanges/microsoft-evsecurity-kv-endpoint-authentication-success-4776.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-authentication-success-4776&type=code)
- [microsoft-evsecurity-kv-endpoint-login-4769](CodeChanges/microsoft-evsecurity-kv-endpoint-login-4769.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-4769&type=code)
- [microsoft-evsecurity-kv-endpoint-login-4769-10](CodeChanges/microsoft-evsecurity-kv-endpoint-login-4769-10.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-4769-10&type=code)
- [microsoft-evsecurity-kv-endpoint-login-4769-11](CodeChanges/microsoft-evsecurity-kv-endpoint-login-4769-11.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-4769-11&type=code)
- [microsoft-evsecurity-kv-endpoint-login-4769-12](CodeChanges/microsoft-evsecurity-kv-endpoint-login-4769-12.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-4769-12&type=code)
- [microsoft-evsecurity-kv-endpoint-login-4769-2](CodeChanges/microsoft-evsecurity-kv-endpoint-login-4769-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-4769-2&type=code)
- [microsoft-evsecurity-kv-endpoint-login-4769-3](CodeChanges/microsoft-evsecurity-kv-endpoint-login-4769-3.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-4769-3&type=code)
- [microsoft-evsecurity-kv-endpoint-login-4769-4](CodeChanges/microsoft-evsecurity-kv-endpoint-login-4769-4.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-4769-4&type=code)
- [microsoft-evsecurity-kv-endpoint-login-4769-5](CodeChanges/microsoft-evsecurity-kv-endpoint-login-4769-5.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-4769-5&type=code)
- [microsoft-evsecurity-kv-endpoint-login-4769-6](CodeChanges/microsoft-evsecurity-kv-endpoint-login-4769-6.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-4769-6&type=code)
- [microsoft-evsecurity-kv-endpoint-login-4769-9](CodeChanges/microsoft-evsecurity-kv-endpoint-login-4769-9.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-4769-9&type=code)
- [microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4625](CodeChanges/microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4625.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4625&type=code)
- [microsoft-evsecurity-kv-endpoint-login-success-4624-5](CodeChanges/microsoft-evsecurity-kv-endpoint-login-success-4624-5.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-success-4624-5&type=code)
- [microsoft-evsecurity-kv-endpoint-login-success-adaudit-4624](CodeChanges/microsoft-evsecurity-kv-endpoint-login-success-adaudit-4624.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-success-adaudit-4624&type=code)
- [microsoft-evsecurity-kv-endpoint-logout-success-4779](CodeChanges/microsoft-evsecurity-kv-endpoint-logout-success-4779.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-logout-success-4779&type=code)
- [microsoft-evsecurity-kv-endpoint-notification-4653](CodeChanges/microsoft-evsecurity-kv-endpoint-notification-4653.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-notification-4653&type=code)
- [microsoft-evsecurity-kv-endpoint-notification-success-4780](CodeChanges/microsoft-evsecurity-kv-endpoint-notification-success-4780.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-notification-success-4780&type=code)
- [microsoft-evsecurity-kv-endpoint-notification-success-4780-1](CodeChanges/microsoft-evsecurity-kv-endpoint-notification-success-4780-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-notification-success-4780-1&type=code)
- [microsoft-evsecurity-kv-endpoint-success-4624-2](CodeChanges/microsoft-evsecurity-kv-endpoint-success-4624-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-success-4624-2&type=code)
- [microsoft-evsecurity-kv-group-modify-success-4735](CodeChanges/microsoft-evsecurity-kv-group-modify-success-4735.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-group-modify-success-4735&type=code)
- [microsoft-evsecurity-kv-key-5061](CodeChanges/microsoft-evsecurity-kv-key-5061.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-key-5061&type=code)
- [microsoft-evsecurity-kv-network-session-fail-4653-1](CodeChanges/microsoft-evsecurity-kv-network-session-fail-4653-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-network-session-fail-4653-1&type=code)
- [microsoft-evsecurity-kv-rdp-traffic-success-4778](CodeChanges/microsoft-evsecurity-kv-rdp-traffic-success-4778.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-rdp-traffic-success-4778&type=code)
- [microsoft-evsecurity-kv-rdp-traffic-success-4778-1](CodeChanges/microsoft-evsecurity-kv-rdp-traffic-success-4778-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-rdp-traffic-success-4778-1&type=code)
- [microsoft-evsecurity-kv-rdp-traffic-success-adaudit-4778](CodeChanges/microsoft-evsecurity-kv-rdp-traffic-success-adaudit-4778.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-rdp-traffic-success-adaudit-4778&type=code)
- [microsoft-evsecurity-kv-share-access-success-5142](CodeChanges/microsoft-evsecurity-kv-share-access-success-5142.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-share-access-success-5142&type=code)
- [microsoft-evsecurity-kv-share-access-success-5143](CodeChanges/microsoft-evsecurity-kv-share-access-success-5143.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-share-access-success-5143&type=code)
- [microsoft-evsecurity-kv-share-access-success-5144](CodeChanges/microsoft-evsecurity-kv-share-access-success-5144.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-share-access-success-5144&type=code)
- [microsoft-evsecurity-kv-share-access-success-5145-2](CodeChanges/microsoft-evsecurity-kv-share-access-success-5145-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-share-access-success-5145-2&type=code)
- [microsoft-evsecurity-kv-user-create-success-4720](CodeChanges/microsoft-evsecurity-kv-user-create-success-4720.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-user-create-success-4720&type=code)
- [microsoft-evsecurity-kv-user-delete-fail-26304740](CodeChanges/microsoft-evsecurity-kv-user-delete-fail-26304740.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-user-delete-fail-26304740&type=code)
- [microsoft-evsecurity-kv-user-delete-fail-4740](CodeChanges/microsoft-evsecurity-kv-user-delete-fail-4740.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-user-delete-fail-4740&type=code)
- [microsoft-evsecurity-kv-user-delete-fail-4743](CodeChanges/microsoft-evsecurity-kv-user-delete-fail-4743.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-user-delete-fail-4743&type=code)
- [microsoft-evsecurity-kv-user-delete-fail-locked](CodeChanges/microsoft-evsecurity-kv-user-delete-fail-locked.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-user-delete-fail-locked&type=code)
- [microsoft-evsecurity-kv-user-delete-fail-lockedout](CodeChanges/microsoft-evsecurity-kv-user-delete-fail-lockedout.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-user-delete-fail-lockedout&type=code)
- [microsoft-evsecurity-kv-user-delete-fail-wls](CodeChanges/microsoft-evsecurity-kv-user-delete-fail-wls.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-user-delete-fail-wls&type=code)
- [microsoft-evsecurity-kv-user-delete-success-4743](CodeChanges/microsoft-evsecurity-kv-user-delete-success-4743.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-user-delete-success-4743&type=code)
- [microsoft-evsecurity-kv-user-delete-success-4743-1](CodeChanges/microsoft-evsecurity-kv-user-delete-success-4743-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-user-delete-success-4743-1&type=code)
- [microsoft-evsecurity-kv-user-enable-success-4722](CodeChanges/microsoft-evsecurity-kv-user-enable-success-4722.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-user-enable-success-4722&type=code)
- [microsoft-evsecurity-kv-user-password-read-5379](CodeChanges/microsoft-evsecurity-kv-user-password-read-5379.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-user-password-read-5379&type=code)
- [microsoft-evsecurity-kv-user-password-read-5379-1](CodeChanges/microsoft-evsecurity-kv-user-password-read-5379-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-user-password-read-5379-1&type=code)
- [microsoft-evsecurity-kv-user-privilege-assign-success-4673](CodeChanges/microsoft-evsecurity-kv-user-privilege-assign-success-4673.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-user-privilege-assign-success-4673&type=code)
- [microsoft-evsecurity-kv-user-privilege-assign-success-4673-1](CodeChanges/microsoft-evsecurity-kv-user-privilege-assign-success-4673-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-user-privilege-assign-success-4673-1&type=code)
- [microsoft-evsecurity-kv-user-privilege-assign-success-4674](CodeChanges/microsoft-evsecurity-kv-user-privilege-assign-success-4674.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-user-privilege-assign-success-4674&type=code)
- [microsoft-evsecurity-kv-user-privilege-use-success-4674-1](CodeChanges/microsoft-evsecurity-kv-user-privilege-use-success-4674-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-user-privilege-use-success-4674-1&type=code)
- [microsoft-evsecurity-mix-ds-object-modify-success-4742](CodeChanges/microsoft-evsecurity-mix-ds-object-modify-success-4742.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-ds-object-modify-success-4742&type=code)
- [microsoft-evsecurity-mix-endpoint-login-4769](CodeChanges/microsoft-evsecurity-mix-endpoint-login-4769.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-endpoint-login-4769&type=code)
- [microsoft-evsecurity-mix-endpoint-login-4769-2](CodeChanges/microsoft-evsecurity-mix-endpoint-login-4769-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-endpoint-login-4769-2&type=code)
- [microsoft-evsecurity-mix-endpoint-login-fail-1201](CodeChanges/microsoft-evsecurity-mix-endpoint-login-fail-1201.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-endpoint-login-fail-1201&type=code)
- [microsoft-evsecurity-mix-endpoint-login-fail-1203](CodeChanges/microsoft-evsecurity-mix-endpoint-login-fail-1203.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-endpoint-login-fail-1203&type=code)
- [microsoft-evsecurity-mix-endpoint-login-success-1200](CodeChanges/microsoft-evsecurity-mix-endpoint-login-success-1200.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-endpoint-login-success-1200&type=code)
- [microsoft-evsecurity-mix-network-traffic-fail-5152](CodeChanges/microsoft-evsecurity-mix-network-traffic-fail-5152.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-network-traffic-fail-5152&type=code)
- [microsoft-evsecurity-mix-network-traffic-fail-5152-1](CodeChanges/microsoft-evsecurity-mix-network-traffic-fail-5152-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-network-traffic-fail-5152-1&type=code)
- [microsoft-evsecurity-mix-user-privilege-assign-success-4672](CodeChanges/microsoft-evsecurity-mix-user-privilege-assign-success-4672.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-user-privilege-assign-success-4672&type=code)
- [microsoft-evsecurity-mix-user-privilege-assign-success-4673](CodeChanges/microsoft-evsecurity-mix-user-privilege-assign-success-4673.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-user-privilege-assign-success-4673&type=code)
- [microsoft-evsecurity-sk4-share-access-success-5145](CodeChanges/microsoft-evsecurity-sk4-share-access-success-5145.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-sk4-share-access-success-5145&type=code)
- [microsoft-evsecurity-sk4-share-create-success-5142](CodeChanges/microsoft-evsecurity-sk4-share-create-success-5142.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-sk4-share-create-success-5142&type=code)
- [microsoft-evsecurity-sk4-share-modify-success-5143](CodeChanges/microsoft-evsecurity-sk4-share-modify-success-5143.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-sk4-share-modify-success-5143&type=code)
- [microsoft-evsecurity-sk4-user-privilege-assign-success-4672](CodeChanges/microsoft-evsecurity-sk4-user-privilege-assign-success-4672.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-sk4-user-privilege-assign-success-4672&type=code)
- [microsoft-evsecurity-sk4-user-privilege-assign-success-4673](CodeChanges/microsoft-evsecurity-sk4-user-privilege-assign-success-4673.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-sk4-user-privilege-assign-success-4673&type=code)
- [microsoft-evsecurity-str-network-traffic-fail-5152](CodeChanges/microsoft-evsecurity-str-network-traffic-fail-5152.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-str-network-traffic-fail-5152&type=code)
- [microsoft-evsecurity-str-registry-create-success-4657](CodeChanges/microsoft-evsecurity-str-registry-create-success-4657.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-str-registry-create-success-4657&type=code)
- [microsoft-evsecurity-str-user-privilege-assign-success-4672](CodeChanges/microsoft-evsecurity-str-user-privilege-assign-success-4672.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-str-user-privilege-assign-success-4672&type=code)
- [microsoft-evsecurity-xml-configuration-modify-success-4742](CodeChanges/microsoft-evsecurity-xml-configuration-modify-success-4742.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-configuration-modify-success-4742&type=code)
- [microsoft-evsecurity-xml-configuration-modify-success-eventid4957](CodeChanges/microsoft-evsecurity-xml-configuration-modify-success-eventid4957.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-configuration-modify-success-eventid4957&type=code)
- [microsoft-evsecurity-xml-ds-object-activity-success-4742](CodeChanges/microsoft-evsecurity-xml-ds-object-activity-success-4742.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-ds-object-activity-success-4742&type=code)
- [microsoft-evsecurity-xml-ds-object-modify-success-4742](CodeChanges/microsoft-evsecurity-xml-ds-object-modify-success-4742.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-ds-object-modify-success-4742&type=code)
- [microsoft-evsecurity-xml-endpoint-activity-4655](CodeChanges/microsoft-evsecurity-xml-endpoint-activity-4655.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-activity-4655&type=code)
- [microsoft-evsecurity-xml-endpoint-login-4769](CodeChanges/microsoft-evsecurity-xml-endpoint-login-4769.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-login-4769&type=code)
- [microsoft-evsecurity-xml-endpoint-login-4769-2](CodeChanges/microsoft-evsecurity-xml-endpoint-login-4769-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-login-4769-2&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-4654](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-4654.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-4654&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-success-4780](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-success-4780.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-success-4780&type=code)
- [microsoft-evsecurity-xml-file-read-success-4663](CodeChanges/microsoft-evsecurity-xml-file-read-success-4663.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-file-read-success-4663&type=code)
- [microsoft-evsecurity-xml-group-modify-success-4735-2](CodeChanges/microsoft-evsecurity-xml-group-modify-success-4735-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-group-modify-success-4735-2&type=code)
- [microsoft-evsecurity-xml-network-session-success-4981](CodeChanges/microsoft-evsecurity-xml-network-session-success-4981.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-network-session-success-4981&type=code)
- [microsoft-evsecurity-xml-network-traffic-fail-5152](CodeChanges/microsoft-evsecurity-xml-network-traffic-fail-5152.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-network-traffic-fail-5152&type=code)
- [microsoft-evsecurity-xml-rdp-traffic-success-4778](CodeChanges/microsoft-evsecurity-xml-rdp-traffic-success-4778.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-rdp-traffic-success-4778&type=code)
- [microsoft-evsecurity-xml-share-modify-success-5143](CodeChanges/microsoft-evsecurity-xml-share-modify-success-5143.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-share-modify-success-5143&type=code)
- [microsoft-evsecurity-xml-user-delete-success-4743](CodeChanges/microsoft-evsecurity-xml-user-delete-success-4743.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-user-delete-success-4743&type=code)
- [microsoft-evsecurity-xml-user-delete-success-4743-1](CodeChanges/microsoft-evsecurity-xml-user-delete-success-4743-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-user-delete-success-4743-1&type=code)
- [microsoft-evsecurity-xml-user-privilege-assign-success-4672](CodeChanges/microsoft-evsecurity-xml-user-privilege-assign-success-4672.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-user-privilege-assign-success-4672&type=code)
- [microsoft-evsecurity-xml-user-privilege-assign-success-4673](CodeChanges/microsoft-evsecurity-xml-user-privilege-assign-success-4673.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-user-privilege-assign-success-4673&type=code)
- [microsoft-evsecurity-xml-user-privilege-assign-success-4673-1](CodeChanges/microsoft-evsecurity-xml-user-privilege-assign-success-4673-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-user-privilege-assign-success-4673-1&type=code)
- [microsoft-nps-kv-radius-traffic-fail-6273](CodeChanges/microsoft-nps-kv-radius-traffic-fail-6273.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-nps-kv-radius-traffic-fail-6273&type=code)
- [microsoft-nps-kv-radius-traffic-success-6272](CodeChanges/microsoft-nps-kv-radius-traffic-success-6272.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-nps-kv-radius-traffic-success-6272&type=code)
- [microsoft-nps-xml-endpoint-authentication-success-6272](CodeChanges/microsoft-nps-xml-endpoint-authentication-success-6272.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-nps-xml-endpoint-authentication-success-6272&type=code)
- [microsoft-nps-xml-radius-traffic-fail-6273](CodeChanges/microsoft-nps-xml-radius-traffic-fail-6273.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-nps-xml-radius-traffic-fail-6273&type=code)
- [microsoft-nps-xml-radius-traffic-success-6278](CodeChanges/microsoft-nps-xml-radius-traffic-success-6278.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-nps-xml-radius-traffic-success-6278&type=code)
- [microsoft-windows-mix-endpoint-login-success-1202](CodeChanges/microsoft-windows-mix-endpoint-login-success-1202.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-windows-mix-endpoint-login-success-1202&type=code)
- [microsoft-windows-sk4-app-notification-success-8001](CodeChanges/microsoft-windows-sk4-app-notification-success-8001.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-windows-sk4-app-notification-success-8001&type=code)

#### Edit Regex Field
<a id="edit-regex-field"></a>
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
- [auth0-a-json-endpoint-login-fail-fp](CodeChanges/auth0-a-json-endpoint-login-fail-fp.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-endpoint-login-fail-fp&type=code)
- [auth0-a-json-endpoint-login-fail-invalidrequest](CodeChanges/auth0-a-json-endpoint-login-fail-invalidrequest.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-endpoint-login-fail-invalidrequest&type=code)
- [auth0-a-json-endpoint-login-success-exchange](CodeChanges/auth0-a-json-endpoint-login-success-exchange.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-endpoint-login-success-exchange&type=code)
- [auth0-a-json-endpoint-login-success-verification](CodeChanges/auth0-a-json-endpoint-login-success-verification.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-endpoint-login-success-verification&type=code)
- [auth0-a-json-http-session-success-mgmt_api_read](CodeChanges/auth0-a-json-http-session-success-mgmt_api_read.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-http-session-success-mgmt_api_read&type=code)
- [auth0-a-json-http-session-success-sapi](CodeChanges/auth0-a-json-http-session-success-sapi.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-http-session-success-sapi&type=code)
- [auth0-a-json-user-delete-success-userdeletion](CodeChanges/auth0-a-json-user-delete-success-userdeletion.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-user-delete-success-userdeletion&type=code)
- [auth0-a-json-user-password-modify-fail-fcp](CodeChanges/auth0-a-json-user-password-modify-fail-fcp.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-user-password-modify-fail-fcp&type=code)
- [auth0-a-json-user-password-modify-success-changepassword](CodeChanges/auth0-a-json-user-password-modify-success-changepassword.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-user-password-modify-success-changepassword&type=code)
- [canon-iradv-csv-endpoint-activity-8193-catchall](CodeChanges/canon-iradv-csv-endpoint-activity-8193-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20canon-iradv-csv-endpoint-activity-8193-catchall&type=code)
- [canon-iradv-csv-endpoint-login-4098-catchall](CodeChanges/canon-iradv-csv-endpoint-login-4098-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20canon-iradv-csv-endpoint-login-4098-catchall&type=code)
- [canon-iradv-csv-printer-activity-1001-catchall](CodeChanges/canon-iradv-csv-printer-activity-1001-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20canon-iradv-csv-printer-activity-1001-catchall&type=code)
- [cisco-asa-kv-radius-traffic-success-113004](CodeChanges/cisco-asa-kv-radius-traffic-success-113004.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-kv-radius-traffic-success-113004&type=code)
- [cisco-asa-kv-vpn-login-fail-113005](CodeChanges/cisco-asa-kv-vpn-login-fail-113005.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-kv-vpn-login-fail-113005&type=code)
- [crowdstrike-falcon-mix-dns-request-success-dnsrequest](CodeChanges/crowdstrike-falcon-mix-dns-request-success-dnsrequest.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-mix-dns-request-success-dnsrequest&type=code)
- [dell-emcisilon-str-file-read-success-open](CodeChanges/dell-emcisilon-str-file-read-success-open.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20dell-emcisilon-str-file-read-success-open&type=code)
- [extrahop-revealx-json-dns-request-success-dnsquery](CodeChanges/extrahop-revealx-json-dns-request-success-dnsquery.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20extrahop-revealx-json-dns-request-success-dnsquery&type=code)
- [google-workspace-cef-email-receive](CodeChanges/google-workspace-cef-email-receive.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20google-workspace-cef-email-receive&type=code)
- [google-workspace-cef-email-send](CodeChanges/google-workspace-cef-email-send.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20google-workspace-cef-email-send&type=code)
- [microsoft-evapp-xml-app-activity-adaccess](CodeChanges/microsoft-evapp-xml-app-activity-adaccess.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-app-activity-adaccess&type=code)
- [microsoft-evapp-xml-app-activity-applicationlogic](CodeChanges/microsoft-evapp-xml-app-activity-applicationlogic.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-app-activity-applicationlogic&type=code)
- [microsoft-evapp-xml-app-activity-assistants](CodeChanges/microsoft-evapp-xml-app-activity-assistants.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-app-activity-assistants&type=code)
- [microsoft-evapp-xml-app-activity-certificatenotification](CodeChanges/microsoft-evapp-xml-app-activity-certificatenotification.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-app-activity-certificatenotification&type=code)
- [microsoft-evapp-xml-app-activity-common](CodeChanges/microsoft-evapp-xml-app-activity-common.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-app-activity-common&type=code)
- [microsoft-evapp-xml-app-activity-frontendhttpproxy](CodeChanges/microsoft-evapp-xml-app-activity-frontendhttpproxy.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-app-activity-frontendhttpproxy&type=code)
- [microsoft-evapp-xml-app-activity-mailboxreplication](CodeChanges/microsoft-evapp-xml-app-activity-mailboxreplication.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-app-activity-mailboxreplication&type=code)
- [microsoft-evapp-xml-app-activity-midtierstorage](CodeChanges/microsoft-evapp-xml-app-activity-midtierstorage.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-app-activity-midtierstorage&type=code)
- [microsoft-evapp-xml-app-activity-msexchangeis](CodeChanges/microsoft-evapp-xml-app-activity-msexchangeis.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-app-activity-msexchangeis&type=code)
- [microsoft-evapp-xml-app-activity-msexchangerepl](CodeChanges/microsoft-evapp-xml-app-activity-msexchangerepl.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-app-activity-msexchangerepl&type=code)
- [microsoft-evapp-xml-app-activity-owa](CodeChanges/microsoft-evapp-xml-app-activity-owa.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-app-activity-owa&type=code)
- [microsoft-evapp-xml-app-activity-transport](CodeChanges/microsoft-evapp-xml-app-activity-transport.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-app-activity-transport&type=code)
- [microsoft-evapp-xml-app-activity-transportdelivery](CodeChanges/microsoft-evapp-xml-app-activity-transportdelivery.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-app-activity-transportdelivery&type=code)
- [microsoft-evapp-xml-app-activity-transportsearch](CodeChanges/microsoft-evapp-xml-app-activity-transportsearch.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-app-activity-transportsearch&type=code)
- [microsoft-evapp-xml-app-activity-transportsubmission](CodeChanges/microsoft-evapp-xml-app-activity-transportsubmission.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-app-activity-transportsubmission&type=code)
- [microsoft-evapp-xml-app-authentication-1200](CodeChanges/microsoft-evapp-xml-app-authentication-1200.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-app-authentication-1200&type=code)
- [microsoft-evapp-xml-app-notification-500](CodeChanges/microsoft-evapp-xml-app-notification-500.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-app-notification-500&type=code)
- [microsoft-evapp-xml-configuration-modify-16028](CodeChanges/microsoft-evapp-xml-configuration-modify-16028.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-configuration-modify-16028&type=code)
- [microsoft-evapp-xml-endpoint-activity-esent](CodeChanges/microsoft-evapp-xml-endpoint-activity-esent.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-endpoint-activity-esent&type=code)
- [microsoft-evapp-xml-endpoint-activity-filter](CodeChanges/microsoft-evapp-xml-endpoint-activity-filter.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-endpoint-activity-filter&type=code)
- [microsoft-evapp-xml-endpoint-activity-perflib](CodeChanges/microsoft-evapp-xml-endpoint-activity-perflib.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-endpoint-activity-perflib&type=code)
- [microsoft-evpowershell-xml-endpoint-notification-4106](CodeChanges/microsoft-evpowershell-xml-endpoint-notification-4106.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evpowershell-xml-endpoint-notification-4106&type=code)
- [microsoft-evpowershell-xml-script-execute-4105](CodeChanges/microsoft-evpowershell-xml-script-execute-4105.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evpowershell-xml-script-execute-4105&type=code)
- [microsoft-evsecurity-json-group-member-list-4799](CodeChanges/microsoft-evsecurity-json-group-member-list-4799.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-group-member-list-4799&type=code)
- [microsoft-evsecurity-kv-group-member-list-4799](CodeChanges/microsoft-evsecurity-kv-group-member-list-4799.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-group-member-list-4799&type=code)
- [microsoft-evsecurity-xml-app-authentication-1200](CodeChanges/microsoft-evsecurity-xml-app-authentication-1200.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-app-authentication-1200&type=code)
- [microsoft-evsecurity-xml-app-authentication-1202](CodeChanges/microsoft-evsecurity-xml-app-authentication-1202.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-app-authentication-1202&type=code)
- [microsoft-evsecurity-xml-app-authentication-299](CodeChanges/microsoft-evsecurity-xml-app-authentication-299.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-app-authentication-299&type=code)
- [microsoft-evsecurity-xml-app-authentication-412](CodeChanges/microsoft-evsecurity-xml-app-authentication-412.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-app-authentication-412&type=code)
- [microsoft-evsecurity-xml-app-authentication-fail-1203](CodeChanges/microsoft-evsecurity-xml-app-authentication-fail-1203.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-app-authentication-fail-1203&type=code)
- [microsoft-evsecurity-xml-app-authentication-fail-411](CodeChanges/microsoft-evsecurity-xml-app-authentication-fail-411.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-app-authentication-fail-411&type=code)
- [microsoft-evsecurity-xml-app-notification-410](CodeChanges/microsoft-evsecurity-xml-app-notification-410.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-app-notification-410&type=code)
- [microsoft-evsecurity-xml-app-notification-431](CodeChanges/microsoft-evsecurity-xml-app-notification-431.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-app-notification-431&type=code)
- [microsoft-evsecurity-xml-app-notification-500](CodeChanges/microsoft-evsecurity-xml-app-notification-500.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-app-notification-500&type=code)
- [microsoft-evsecurity-xml-app-notification-501](CodeChanges/microsoft-evsecurity-xml-app-notification-501.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-app-notification-501&type=code)
- [microsoft-evsecurity-xml-app-notification-510](CodeChanges/microsoft-evsecurity-xml-app-notification-510.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-app-notification-510&type=code)
- [microsoft-evsecurity-xml-audit-policy-modify-4907](CodeChanges/microsoft-evsecurity-xml-audit-policy-modify-4907.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-audit-policy-modify-4907&type=code)
- [microsoft-evsecurity-xml-configuration-load-4826](CodeChanges/microsoft-evsecurity-xml-configuration-load-4826.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-configuration-load-4826&type=code)
- [microsoft-evsecurity-xml-ds-replication-modify-4931-1](CodeChanges/microsoft-evsecurity-xml-ds-replication-modify-4931-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-ds-replication-modify-4931-1&type=code)
- [microsoft-evsecurity-xml-endpoint-activity-dfssvc](CodeChanges/microsoft-evsecurity-xml-endpoint-activity-dfssvc.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-activity-dfssvc&type=code)
- [microsoft-evsecurity-xml-endpoint-activity-success-5889](CodeChanges/microsoft-evsecurity-xml-endpoint-activity-success-5889.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-activity-success-5889&type=code)
- [microsoft-evsecurity-xml-endpoint-authentication-fail-4822](CodeChanges/microsoft-evsecurity-xml-endpoint-authentication-fail-4822.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-authentication-fail-4822&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-4653](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-4653.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-4653&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-4653-1](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-4653-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-4653-1&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-4793](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-4793.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-4793&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-4797](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-4797.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-4797&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-4902](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-4902.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-4902&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-4965](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-4965.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-4965&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-4985](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-4985.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-4985&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-5024](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-5024.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-5024&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-5033](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-5033.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-5033&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-5125](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-5125.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-5125&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-5127](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-5127.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-5127&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-5890](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-5890.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-5890&type=code)
- [microsoft-evsecurity-xml-endpoint-start-4608](CodeChanges/microsoft-evsecurity-xml-endpoint-start-4608.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-start-4608&type=code)
- [microsoft-evsecurity-xml-group-list-4798-1](CodeChanges/microsoft-evsecurity-xml-group-list-4798-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-group-list-4798-1&type=code)
- [microsoft-evsecurity-xml-group-member-list-4799-1](CodeChanges/microsoft-evsecurity-xml-group-member-list-4799-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-group-member-list-4799-1&type=code)
- [microsoft-evsecurity-xml-http-request-403](CodeChanges/microsoft-evsecurity-xml-http-request-403.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-http-request-403&type=code)
- [microsoft-evsecurity-xml-http-response-404](CodeChanges/microsoft-evsecurity-xml-http-response-404.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-http-response-404&type=code)
- [microsoft-evsecurity-xml-log-backup-1105](CodeChanges/microsoft-evsecurity-xml-log-backup-1105.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-log-backup-1105&type=code)
- [microsoft-evsecurity-xml-log-disable-1100](CodeChanges/microsoft-evsecurity-xml-log-disable-1100.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-log-disable-1100&type=code)
- [microsoft-evsecurity-xml-password-read-5379](CodeChanges/microsoft-evsecurity-xml-password-read-5379.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-password-read-5379&type=code)
- [microsoft-evsecurity-xml-password-read-5381](CodeChanges/microsoft-evsecurity-xml-password-read-5381.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-password-read-5381&type=code)
- [microsoft-evsecurity-xml-policy-apply-4954](CodeChanges/microsoft-evsecurity-xml-policy-apply-4954.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-policy-apply-4954&type=code)
- [microsoft-evsecurity-xml-policy-apply-6144](CodeChanges/microsoft-evsecurity-xml-policy-apply-6144.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-policy-apply-6144&type=code)
- [microsoft-evsecurity-xml-policy-modify-4947](CodeChanges/microsoft-evsecurity-xml-policy-modify-4947.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-policy-modify-4947&type=code)
- [microsoft-evsecurity-xml-policy-modify-4948](CodeChanges/microsoft-evsecurity-xml-policy-modify-4948.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-policy-modify-4948&type=code)
- [microsoft-evsecurity-xml-process-close-4689](CodeChanges/microsoft-evsecurity-xml-process-close-4689.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-process-close-4689&type=code)
- [microsoft-evsecurity-xml-process-token-assign-4696](CodeChanges/microsoft-evsecurity-xml-process-token-assign-4696.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-process-token-assign-4696&type=code)
- [microsoft-evsecurity-xml-scheduled-task-delete-4699](CodeChanges/microsoft-evsecurity-xml-scheduled-task-delete-4699.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-scheduled-task-delete-4699&type=code)
- [microsoft-evsecurity-xml-scheduled-task-disable-4701](CodeChanges/microsoft-evsecurity-xml-scheduled-task-disable-4701.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-scheduled-task-disable-4701&type=code)
- [microsoft-evsecurity-xml-user-privilege-modify-4703](CodeChanges/microsoft-evsecurity-xml-user-privilege-modify-4703.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-user-privilege-modify-4703&type=code)
- [microsoft-evsystem-xml-endpoint-activity-microsoftwindowswas](CodeChanges/microsoft-evsystem-xml-endpoint-activity-microsoftwindowswas.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-xml-endpoint-activity-microsoftwindowswas&type=code)
- [microsoft-evsystem-xml-endpoint-activity-schannel](CodeChanges/microsoft-evsystem-xml-endpoint-activity-schannel.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-xml-endpoint-activity-schannel&type=code)
- [microsoft-evsystem-xml-endpoint-activity-servicecontrolmanager](CodeChanges/microsoft-evsystem-xml-endpoint-activity-servicecontrolmanager.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-xml-endpoint-activity-servicecontrolmanager&type=code)
- [microsoft-evsystem-xml-endpoint-authentication-fail-5723](CodeChanges/microsoft-evsystem-xml-endpoint-authentication-fail-5723.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-xml-endpoint-authentication-fail-5723&type=code)
- [microsoft-evsystem-xml-policy-apply-success-1503](CodeChanges/microsoft-evsystem-xml-policy-apply-success-1503.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-xml-policy-apply-success-1503&type=code)
- [microsoft-evterminalserviceslicensing-xml-endpoint-notification-success-4105](CodeChanges/microsoft-evterminalserviceslicensing-xml-endpoint-notification-success-4105.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evterminalserviceslicensing-xml-endpoint-notification-success-4105&type=code)
- [microsoft-networkwatcher-json-network-traffic-flowlogevent](CodeChanges/microsoft-networkwatcher-json-network-traffic-flowlogevent.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-networkwatcher-json-network-traffic-flowlogevent&type=code)
- [pan-ngfw-csv-alert-trigger-success-file](CodeChanges/pan-ngfw-csv-alert-trigger-success-file.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-alert-trigger-success-file&type=code)
- [pan-ngfw-mix-alert-trigger-success-spywarealert](CodeChanges/pan-ngfw-mix-alert-trigger-success-spywarealert.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-mix-alert-trigger-success-spywarealert&type=code)
- [unix-unix-str-endpoint-activity-sshd](CodeChanges/unix-unix-str-endpoint-activity-sshd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-activity-sshd&type=code)
- [zscaler-ia-json-network-traffic-event](CodeChanges/zscaler-ia-json-network-traffic-event.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zscaler-ia-json-network-traffic-event&type=code)
- [zscaler-pa-json-app-activity-success-create](CodeChanges/zscaler-pa-json-app-activity-success-create.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zscaler-pa-json-app-activity-success-create&type=code)
- [zscaler-pa-json-app-activity-success-delete](CodeChanges/zscaler-pa-json-app-activity-success-delete.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zscaler-pa-json-app-activity-success-delete&type=code)
- [zscaler-pa-json-app-activity-success-update](CodeChanges/zscaler-pa-json-app-activity-success-update.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zscaler-pa-json-app-activity-success-update&type=code)
- [zscaler-pa-json-app-login-fail-signinfailure](CodeChanges/zscaler-pa-json-app-login-fail-signinfailure.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zscaler-pa-json-app-login-fail-signinfailure&type=code)
- [zscaler-pa-json-app-login-success-signin](CodeChanges/zscaler-pa-json-app-login-success-signin.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zscaler-pa-json-app-login-success-signin&type=code)
- [zscaler-pa-json-app-logout-success-signout](CodeChanges/zscaler-pa-json-app-logout-success-signout.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zscaler-pa-json-app-logout-success-signout&type=code)
- [zscaler-pa-json-user-lock-success-accountlock](CodeChanges/zscaler-pa-json-user-lock-success-accountlock.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zscaler-pa-json-user-lock-success-accountlock&type=code)
- [zscaler-pa-json-user-unlock-success-accountunlock](CodeChanges/zscaler-pa-json-user-unlock-success-accountunlock.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zscaler-pa-json-user-unlock-success-accountunlock&type=code)
- [zyxel-usgflex-kv-network-traffic-success-trafficlog](CodeChanges/zyxel-usgflex-kv-network-traffic-success-trafficlog.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zyxel-usgflex-kv-network-traffic-success-trafficlog&type=code)

#### Removed Parser
<a id="removed-parser"></a>
- [citrix-cgateway-str-http-session-success-sslvpn](CodeChanges/citrix-cgateway-str-http-session-success-sslvpn.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20citrix-cgateway-str-http-session-success-sslvpn&type=code)

</details>

<details>
<summary><strong id="parsertemplate">ParserTemplate (8)</strong></summary>


### Change Types
- [Added Parser Template](#added-parser-template)
- [Changed Parsed Fields](#changed-parsed-fields)
- [Edit Regex Field](#edit-regex-field)

#### Added Parser Template
<a id="added-parser-template"></a>
- [json-google-email-activity](CodeChanges/json-google-email-activity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20json-google-email-activity&type=code)

#### Changed Parsed Fields
<a id="changed-parsed-fields"></a>
- [cef-defender-atp-events](CodeChanges/cef-defender-atp-events.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cef-defender-atp-events&type=code)
- [cef-microsoft-app-activity](CodeChanges/cef-microsoft-app-activity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cef-microsoft-app-activity&type=code)
- [zyxel-network-events](CodeChanges/zyxel-network-events.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zyxel-network-events&type=code)

#### Edit Regex Field
<a id="edit-regex-field"></a>
- [auth0-authentication-template](CodeChanges/auth0-authentication-template.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-authentication-template&type=code)
- [canon-endpoint-events](CodeChanges/canon-endpoint-events.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20canon-endpoint-events&type=code)
- [s-xml-events](CodeChanges/s-xml-events.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20s-xml-events&type=code)
- [zscaler-audit-events](CodeChanges/zscaler-audit-events.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zscaler-audit-events&type=code)

</details>