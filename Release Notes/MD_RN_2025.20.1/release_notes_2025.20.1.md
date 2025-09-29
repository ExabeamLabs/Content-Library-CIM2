# Content Package 2025.20.1

These release notes contain information about content package 2025.20.1, released on 25 Sep 2025.


## Enhancements
- Added new parser - juniper-srx-kv-network-traffic-success-udpflood for juniper SRX traffic logs.
- Added new subject & activity type for ai_agent & ai_agent-request:success
- Created parser for Check Point Identity Collector VPN logout event logs.
- Added new parser f5-dc-json-app-activity-success-apiaudit
- updated parser proofpoint-casb-json-alert-trigger-success-severity
- Added new parser vectra-cd-json-app-activity-success-accountscoring
- Created parser for AutomatedLeadSummaryEvent of CrowdStrike Falcon.
- Updated EventBuilder condition for microsoft-evsecurity-kv-file-fileoperation ,microsoft-evsecurity-mix-user-privilege-assign-success-4672,microsoft-evsecurity-mix-user-privilege-use-success-4674 parser to generate events .
- Updated field extractions for user, dest_host & full_name for parser: microsoft-evsecurity-xml-registry-create-success-4657
- Updated definition for field 'state' to be used in geographical context. For other fields we have replaced it to status_msg or service_state.
- Added new event_type and added user,syscall_name,syscall_number ,process_command_line ,system_architecture fields for unix-ad-kv-process-create-fail-syscall and unix-unix-kv-process-create-success-exe parser .
- Deprecated unused legacy parsers netskope-sc-json-app-login-success-loginsuccess netskope-sc-json-alert-trigger-success-compromised netskope-sc-sk4-app-login-success-page netskope-sc-sk4-app-logout-success-logout netskope-sc-sk4-app-notification-success-auditevent microsoft-defendercloud-sk4-alert-trigger-success-simulateda mcafee-wg-leef-http-session-webgateway netskope-sc-json-app-activity-success-propertyupdated
- Added new parsers for Check Point Avanan
- Updated process_name & process_id extractions for Unix
- Updated the regex of 'additional_info' field.
- Created parser for Sailpoint tomcat logs.
- Developed new NSA enricher for login_type & login_type_text
- Added enricher for login_type and login_type_text field
- Updated bytes_in & bytes_out extractions for google, fortinet, suricata, cisco, mcafee & microsoft-azure
- Updated bytes_in & bytes_out extractions for google, fortinet, suricata, cisco, mcafee & microsoft-azure

## Addressed Issues
- Updated dest_user field extractions for parser: microsoft-evsecurity-mix-user-enable-success-4722
- Updated dns_query field for infoblox-bddi-cef-alert-trigger-success-alert parser.
- Updated file_path, file_name and file_ext field extractions for parser - zeek-z-json-file-success-sbmfiles
- Added mapping for the field Logon Type
- Added event_code field for crowdstrike-falcon-sk4-endpoint-login-userloginfail parser
- Updated device_name field extractions for parser: okta-amfa-mix-app-login-success-securitycontext
- Updated old_user_name, new_user_name, dest_domain, dest_user_sid, user_sid, user, domain, login_id, privileges field extractions for parser: microsoft-evsecurity-xml-user-name-modify-4781-1
- Updated aip , src_ip , host field extractions for Crowdstrike logs
- Updated EventBuilder condition for sentinelone-singularityp-json-alert-trigger-success-url-1 parser.
- Updated user and full_name field extractions in parser - gitlab-gl-json-app-activity-success-entity.
- Fixed slow regexes issue for parser - microsoft-azuread-json-group-member-add-success-aadiam, microsoft-azure-cef-group-member-remove-success-removefromgroup, microsoft-azuread-json-group-member-remove-success-groupmemberremoved.
- Added new parser for  Check Point NGFW logs - checkpoint-ngfw-kv-network-traffic-success-checkpoint.
- Updated regex for dns_query, dns_query_type, src_ip, src_host and src_port for Unix Named Updated event builder conditions for for Unix Named
- Updated regex for host field extraction in parser - microsoft-defenderep-json-alert-trigger-success-category.
- Updated the field name from audispd_type (Non-CIM field) to event_name (CIM field) in parser - unix-unix-kv-endpoint-login-userstart.
- Updated process_guid, user_sid, parent_process_id and additional_info extractions for parser: microsoft-sysmon-json-process-create-success-processcreate
- Updated process related fields extractions to filter '-' value for parser: microsoft-sysmon-xml-process-create-success-processcreate
- Updated action, category field extractions for parser: netskope-sc-json-alert-trigger-success-alertname
- updated parser zscaler-ia-csv-network-traffic-success-zscalerclientconnector
- Added field extraction for 'user' and 'domain' field for parser microsoft-evdirservice-xml-app-notification-success-directoryservice
- Updated regex for src_ip and src_host for parser unix-auditd-kv-user-switch-success-userrolechange Updated event builder conditions for parser:unix-auditd-kv-user-switch-success-userrolechange
- updated parser microsoft-evsecurity-kv-endpoint-login-success-successfullyloggedon
- Updated regex for dest_email_address for parsers: proofpoint-tappod-json-email-send-receive-sendmailto and proofpoint-tappod-json-email-send-receive-sendmailfrom
- Fixed condition for feature id Prof-GA-Country-O-SCountry, Prof-GA-Country-U-SCountry, Prof-GA-Country-DZ-SCountry & Prof-GA-Country-SZ-DCountry
- Added file_dir ,file_name , file_ext and process_command_line fields for crowdstrike-falcon-sk4-alert-trigger-firewallmatchevent parser.
- Fixed mac_address regex into parser unix-unix-str-dhcp-session-success-appliedadd
- Updated email_address, user field extractions for parser microsoft-o365-cef-app-login-fail-userloginfailed
- Updated the CrowdStrike Falcon and Microsoft parsers to correctly extract the host field. Parsers: crowdstrike-falcon-mix-alert-trigger-success-detection, crowdstrike-falcon-json-alert-trigger-success-identityprotection and microsoft-o365-sk4-app-file-workload.
- Updated regex for email_address field extraction in parser - zeek-z-json-email-send-receive-rcptto.
- Updated the regex for host and dest_host for parser linux-dhcp-str-dhcp-session-success-dhcprequest
- Added mapping for hostname, dsthost field for the parser netskope-sc-json-network-session-success-typenetwork
- Added dest_user_sid , dest_domain , user fields for microsoft-evsecurity-xml-endpoint-login-success-4624-1 and microsoft-evsecurity-kv-endpoint-login-success-successfullyloggedon parser.
- Updated the parser 'sentinelone-singularityp-kv-app-activity-success-malware'
- Added serial_num regex in parsers - okta-amfa-mix-app-login-success-securitycontext and okta-amfa-json-app-login-success-evaluatesignon-1.
- Updated parser 'mimecast-seg-cef-email-url v1.0.0'
- Updated the rule Fact-PCgup-AF ('title': 'The Notepad++ updater was executed from an unknown path') expression to exclude false positives related to standard Notepad++ software updates.
- Updated SentinelOne Singularity Platform parser to parse src.process.parent as grandparent_process*, src.process as parent_process*, and tgt.process as process for script/process-related event types.

## Code Changes
### ℹ️ How to Read This Document

Each item listed under **Code Changes** includes:

- **A link to a detailed change file**  
  Click the filename (e.g., `Carbon Black.md`) to open a full table showing what changed.

- **A search icon 🔍**  
  Click the 🔍 icon to search for this resource in the [Exabeam Content Library](https://github.com/ExabeamLabs/Content-Library-CIM2).


<details>
<summary><strong id="event-builder">Event Builder (36)</strong></summary>


### Change Types
- [Added Event Builder](#added-event-builder)
- [Edit Conditions](#edit-conditions)
- [Removed Event Builder](#removed-event-builder)

#### Added Event Builder
<a id="added-event-builder"></a>
- [dl-checkpoint-securitygateway-vpn-logout-success](CodeChanges/dl-checkpoint-securitygateway-vpn-logout-success.md)
- [dl-proofpoint-casb-alert-trigger-success-1](CodeChanges/dl-proofpoint-casb-alert-trigger-success-1.md)
- [dl-sailpoint-iiq-app-notification-success](CodeChanges/dl-sailpoint-iiq-app-notification-success.md)
- [dl-vectra-cognitodetect-alert-trigger-success-3](CodeChanges/dl-vectra-cognitodetect-alert-trigger-success-3.md)
- [f5-dc-app-activity-fail](CodeChanges/f5-dc-app-activity-fail.md)
- [f5-dc-app-activity-success](CodeChanges/f5-dc-app-activity-success.md)
- [f5-dc-configuration-create-fail](CodeChanges/f5-dc-configuration-create-fail.md)
- [f5-dc-configuration-create-success](CodeChanges/f5-dc-configuration-create-success.md)
- [f5-dc-configuration-delete-fail](CodeChanges/f5-dc-configuration-delete-fail.md)
- [f5-dc-configuration-delete-success](CodeChanges/f5-dc-configuration-delete-success.md)
- [f5-dc-configuration-modify-fail](CodeChanges/f5-dc-configuration-modify-fail.md)
- [f5-dc-configuration-modify-success](CodeChanges/f5-dc-configuration-modify-success.md)
- [f5-dc-configuration-read-fail](CodeChanges/f5-dc-configuration-read-fail.md)
- [f5-dc-configuration-read-success](CodeChanges/f5-dc-configuration-read-success.md)
- [proofpoint-casb-alert-trigger-success-1](CodeChanges/proofpoint-casb-alert-trigger-success-1.md)
- [unix-syscall-execute-fail](CodeChanges/unix-syscall-execute-fail.md)
- [unix-syscall-execute-fail-3](CodeChanges/unix-syscall-execute-fail-3.md)
- [unix-syscall-execute-success-5](CodeChanges/unix-syscall-execute-success-5.md)
- [vectra-cognitodetect-alert-trigger-success-3](CodeChanges/vectra-cognitodetect-alert-trigger-success-3.md)

#### Edit Conditions
<a id="edit-conditions"></a>
- [dl-microsoft-windows-log-disable-success-1](CodeChanges/dl-microsoft-windows-log-disable-success-1.md)
- [dl-microsoft-windows-log-enable-success](CodeChanges/dl-microsoft-windows-log-enable-success.md)
- [dl-microsoft-windows-user-privilege-use-fail](CodeChanges/dl-microsoft-windows-user-privilege-use-fail.md)
- [dl-sentinelone-singularity-alert-trigger-success](CodeChanges/dl-sentinelone-singularity-alert-trigger-success.md)
- [microsoft-windows-user-privilege-assign-success](CodeChanges/microsoft-windows-user-privilege-assign-success.md)
- [microsoft-windows-user-privilege-use-success-1](CodeChanges/microsoft-windows-user-privilege-use-success-1.md)
- [salesforce-http-request-fail](CodeChanges/salesforce-http-request-fail.md)
- [sentinelone-network-http-session-success-1](CodeChanges/sentinelone-network-http-session-success-1.md)
- [sentinelone-singularity-alert-trigger-success](CodeChanges/sentinelone-singularity-alert-trigger-success.md)
- [unix-auditd-user-switch-success-1](CodeChanges/unix-auditd-user-switch-success-1.md)
- [unix-unix-endpoint-login-fail](CodeChanges/unix-unix-endpoint-login-fail.md)
- [unix-unix-ssh-traffic-success-2](CodeChanges/unix-unix-ssh-traffic-success-2.md)

#### Removed Event Builder
<a id="removed-event-builder"></a>
- [dl-netskope-sc-app-notification-success](CodeChanges/dl-netskope-sc-app-notification-success.md)
- [microsoft-defendercloud-alert-trigger-success-3](CodeChanges/microsoft-defendercloud-alert-trigger-success-3.md)
- [unix-process-create-fail](CodeChanges/unix-process-create-fail.md)
- [unix-process-create-fail-3](CodeChanges/unix-process-create-fail-3.md)
- [unix-process-create-success-5](CodeChanges/unix-process-create-success-5.md)

</details>

<details>
<summary><strong id="parser">Parser (359)</strong></summary>


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
- [amazon-awscloudtrail-json-app-activity-awsapicall](CodeChanges/amazon-awscloudtrail-json-app-activity-awsapicall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-app-activity-awsapicall&type=code)
- [zscaler-ia-csv-network-traffic-success-zscalerclientconnector](CodeChanges/zscaler-ia-csv-network-traffic-success-zscalerclientconnector.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zscaler-ia-csv-network-traffic-success-zscalerclientconnector&type=code)

#### Added Parser
<a id="added-parser"></a>
- [checkpoint-avanan-json-alert-trigger-success-confidenceindicator](CodeChanges/checkpoint-avanan-json-alert-trigger-success-confidenceindicator.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-avanan-json-alert-trigger-success-confidenceindicator&type=code)
- [checkpoint-avanan-json-email-receive-entitypayload](CodeChanges/checkpoint-avanan-json-email-receive-entitypayload.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-avanan-json-email-receive-entitypayload&type=code)
- [checkpoint-avanan-json-email-send-entitypayload](CodeChanges/checkpoint-avanan-json-email-send-entitypayload.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-avanan-json-email-send-entitypayload&type=code)
- [checkpoint-ia-kv-vpn-logout-success-logout](CodeChanges/checkpoint-ia-kv-vpn-logout-success-logout.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-ia-kv-vpn-logout-success-logout&type=code)
- [checkpoint-ngfw-kv-network-traffic-success-checkpoint](CodeChanges/checkpoint-ngfw-kv-network-traffic-success-checkpoint.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-ngfw-kv-network-traffic-success-checkpoint&type=code)
- [crowdstrike-falcon-json-alert-trigger-success-automatedleadsummaryevent](CodeChanges/crowdstrike-falcon-json-alert-trigger-success-automatedleadsummaryevent.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-alert-trigger-success-automatedleadsummaryevent&type=code)
- [f5-dc-json-app-activity-success-apiaudit](CodeChanges/f5-dc-json-app-activity-success-apiaudit.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20f5-dc-json-app-activity-success-apiaudit&type=code)
- [juniper-srx-kv-network-traffic-success-udpflood](CodeChanges/juniper-srx-kv-network-traffic-success-udpflood.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20juniper-srx-kv-network-traffic-success-udpflood&type=code)
- [proofpoint-casb-json-alert-trigger-success-severity](CodeChanges/proofpoint-casb-json-alert-trigger-success-severity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20proofpoint-casb-json-alert-trigger-success-severity&type=code)
- [sailpoint-iiq-str-app-notification-success-tomcat](CodeChanges/sailpoint-iiq-str-app-notification-success-tomcat.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sailpoint-iiq-str-app-notification-success-tomcat&type=code)
- [vectra-cd-json-alert-trigger-success-accountscoring](CodeChanges/vectra-cd-json-alert-trigger-success-accountscoring.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vectra-cd-json-alert-trigger-success-accountscoring&type=code)

#### Changed
<a id="changed"></a>
- [sentinelone-singularityp-kv-app-activity-success-malware](CodeChanges/sentinelone-singularityp-kv-app-activity-success-malware.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-singularityp-kv-app-activity-success-malware&type=code)

#### Changed Parsed Fields
<a id="changed-parsed-fields"></a>
- [crowdstrike-falcon-cef-file-download-success-loadconfirmation](CodeChanges/crowdstrike-falcon-cef-file-download-success-loadconfirmation.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-cef-file-download-success-loadconfirmation&type=code)
- [crowdstrike-falcon-cef-file-write-success-critialfilemodified](CodeChanges/crowdstrike-falcon-cef-file-write-success-critialfilemodified.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-cef-file-write-success-critialfilemodified&type=code)
- [crowdstrike-falcon-cef-file-write-success-fsvolumemounted](CodeChanges/crowdstrike-falcon-cef-file-write-success-fsvolumemounted.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-cef-file-write-success-fsvolumemounted&type=code)
- [crowdstrike-falcon-cef-file-write-success-unmounted](CodeChanges/crowdstrike-falcon-cef-file-write-success-unmounted.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-cef-file-write-success-unmounted&type=code)
- [crowdstrike-falcon-cef-file-write-success-written](CodeChanges/crowdstrike-falcon-cef-file-write-success-written.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-cef-file-write-success-written&type=code)
- [crowdstrike-falcon-json-app-activity-success-scriptcontrolscantelemetry](CodeChanges/crowdstrike-falcon-json-app-activity-success-scriptcontrolscantelemetry.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-app-activity-success-scriptcontrolscantelemetry&type=code)
- [crowdstrike-falcon-json-app-notification-success-kextload](CodeChanges/crowdstrike-falcon-json-app-notification-success-kextload.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-app-notification-success-kextload&type=code)
- [crowdstrike-falcon-json-app-notification-success-processexeconsmbfile](CodeChanges/crowdstrike-falcon-json-app-notification-success-processexeconsmbfile.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-app-notification-success-processexeconsmbfile&type=code)
- [crowdstrike-falcon-json-app-notification-success-registerrawinputdevicesetw](CodeChanges/crowdstrike-falcon-json-app-notification-success-registerrawinputdevicesetw.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-app-notification-success-registerrawinputdevicesetw&type=code)
- [crowdstrike-falcon-json-configuration-modify-success-firewall](CodeChanges/crowdstrike-falcon-json-configuration-modify-success-firewall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-configuration-modify-success-firewall&type=code)
- [crowdstrike-falcon-json-endpoint-logout-success-userlogoff](CodeChanges/crowdstrike-falcon-json-endpoint-logout-success-userlogoff.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-endpoint-logout-success-userlogoff&type=code)
- [crowdstrike-falcon-json-file-delete-success-deleted](CodeChanges/crowdstrike-falcon-json-file-delete-success-deleted.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-file-delete-success-deleted&type=code)
- [crowdstrike-falcon-json-file-download-success-bitsjobcreated](CodeChanges/crowdstrike-falcon-json-file-download-success-bitsjobcreated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-file-download-success-bitsjobcreated&type=code)
- [crowdstrike-falcon-json-file-read-success-criticalfileaccessed](CodeChanges/crowdstrike-falcon-json-file-read-success-criticalfileaccessed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-file-read-success-criticalfileaccessed&type=code)
- [crowdstrike-falcon-json-file-read-success-ransomware](CodeChanges/crowdstrike-falcon-json-file-read-success-ransomware.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-file-read-success-ransomware&type=code)
- [crowdstrike-falcon-json-file-write-success-machofilewritten](CodeChanges/crowdstrike-falcon-json-file-write-success-machofilewritten.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-file-write-success-machofilewritten&type=code)
- [crowdstrike-falcon-json-file-write-success-renamed](CodeChanges/crowdstrike-falcon-json-file-write-success-renamed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-file-write-success-renamed&type=code)
- [crowdstrike-falcon-json-file-write-success-scriptfilewritteninfo](CodeChanges/crowdstrike-falcon-json-file-write-success-scriptfilewritteninfo.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-file-write-success-scriptfilewritteninfo&type=code)
- [crowdstrike-falcon-json-network-session-success-listenip](CodeChanges/crowdstrike-falcon-json-network-session-success-listenip.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-network-session-success-listenip&type=code)
- [crowdstrike-falcon-json-process-create-success-servicestarted](CodeChanges/crowdstrike-falcon-json-process-create-success-servicestarted.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-process-create-success-servicestarted&type=code)
- [crowdstrike-falcon-json-registry-modify-success-reggenericvalueupdate](CodeChanges/crowdstrike-falcon-json-registry-modify-success-reggenericvalueupdate.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-registry-modify-success-reggenericvalueupdate&type=code)
- [crowdstrike-falcon-json-service-stop-success-hostedservicestopped](CodeChanges/crowdstrike-falcon-json-service-stop-success-hostedservicestopped.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-service-stop-success-hostedservicestopped&type=code)
- [crowdstrike-falcon-kv-app-notification-crashnotification](CodeChanges/crowdstrike-falcon-kv-app-notification-crashnotification.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-kv-app-notification-crashnotification&type=code)
- [crowdstrike-falcon-mix-alert-trigger-success-detection](CodeChanges/crowdstrike-falcon-mix-alert-trigger-success-detection.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-mix-alert-trigger-success-detection&type=code)
- [crowdstrike-falcon-mix-endpoint-login-success-hostinfo](CodeChanges/crowdstrike-falcon-mix-endpoint-login-success-hostinfo.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-mix-endpoint-login-success-hostinfo&type=code)
- [crowdstrike-falcon-mix-endpoint-login-success-useridentity](CodeChanges/crowdstrike-falcon-mix-endpoint-login-success-useridentity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-mix-endpoint-login-success-useridentity&type=code)
- [crowdstrike-falcon-mix-endpoint-login-success-userlogon](CodeChanges/crowdstrike-falcon-mix-endpoint-login-success-userlogon.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-mix-endpoint-login-success-userlogon&type=code)
- [crowdstrike-falcon-mix-file-write-success-directorycreate](CodeChanges/crowdstrike-falcon-mix-file-write-success-directorycreate.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-mix-file-write-success-directorycreate&type=code)
- [crowdstrike-falcon-sk4-alert-trigger-firewallmatchevent](CodeChanges/crowdstrike-falcon-sk4-alert-trigger-firewallmatchevent.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-sk4-alert-trigger-firewallmatchevent&type=code)
- [crowdstrike-falcon-sk4-alert-trigger-suspiciousdnsrequest](CodeChanges/crowdstrike-falcon-sk4-alert-trigger-suspiciousdnsrequest.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-sk4-alert-trigger-suspiciousdnsrequest&type=code)
- [crowdstrike-falcon-sk4-app-activity-eventsimplename](CodeChanges/crowdstrike-falcon-sk4-app-activity-eventsimplename.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-sk4-app-activity-eventsimplename&type=code)
- [crowdstrike-falcon-sk4-endpoint-login-userloginfail](CodeChanges/crowdstrike-falcon-sk4-endpoint-login-userloginfail.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-sk4-endpoint-login-userloginfail&type=code)
- [f5-asm-kv-alert-trigger-success-botdefense](CodeChanges/f5-asm-kv-alert-trigger-success-botdefense.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20f5-asm-kv-alert-trigger-success-botdefense&type=code)
- [ftp-f-str-app-activity-kick](CodeChanges/ftp-f-str-app-activity-kick.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20ftp-f-str-app-activity-kick&type=code)
- [ftp-f-str-app-activity-list](CodeChanges/ftp-f-str-app-activity-list.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20ftp-f-str-app-activity-list&type=code)
- [ftp-f-str-app-activity-mkd](CodeChanges/ftp-f-str-app-activity-mkd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20ftp-f-str-app-activity-mkd&type=code)
- [ftp-f-str-app-activity-quit](CodeChanges/ftp-f-str-app-activity-quit.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20ftp-f-str-app-activity-quit&type=code)
- [ftp-f-str-app-activity-retr](CodeChanges/ftp-f-str-app-activity-retr.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20ftp-f-str-app-activity-retr&type=code)
- [ftp-f-str-app-activity-size](CodeChanges/ftp-f-str-app-activity-size.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20ftp-f-str-app-activity-size&type=code)
- [ftp-f-str-app-activity-sshdisconnect](CodeChanges/ftp-f-str-app-activity-sshdisconnect.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20ftp-f-str-app-activity-sshdisconnect&type=code)
- [ftp-f-str-app-activity-undefined](CodeChanges/ftp-f-str-app-activity-undefined.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20ftp-f-str-app-activity-undefined&type=code)
- [ftp-f-str-app-activity-user](CodeChanges/ftp-f-str-app-activity-user.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20ftp-f-str-app-activity-user&type=code)
- [gitlab-gl-json-app-activity-success-entity](CodeChanges/gitlab-gl-json-app-activity-success-entity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20gitlab-gl-json-app-activity-success-entity&type=code)
- [infoblox-bddi-cef-alert-trigger-success-alert](CodeChanges/infoblox-bddi-cef-alert-trigger-success-alert.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-cef-alert-trigger-success-alert&type=code)
- [infoblox-bddi-csv-app-notification-fixed](CodeChanges/infoblox-bddi-csv-app-notification-fixed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-csv-app-notification-fixed&type=code)
- [infoblox-bddi-csv-ip-free-dhcpd](CodeChanges/infoblox-bddi-csv-ip-free-dhcpd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-csv-ip-free-dhcpd&type=code)
- [infoblox-bddi-kv-endpoint-login-success-loginallow](CodeChanges/infoblox-bddi-kv-endpoint-login-success-loginallow.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-kv-endpoint-login-success-loginallow&type=code)
- [infoblox-bddi-str-configuration-modify-deletedip](CodeChanges/infoblox-bddi-str-configuration-modify-deletedip.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-configuration-modify-deletedip&type=code)
- [infoblox-bddi-str-configuration-modify-success-named](CodeChanges/infoblox-bddi-str-configuration-modify-success-named.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-configuration-modify-success-named&type=code)
- [infoblox-bddi-str-configuration-modify-success-policyzone](CodeChanges/infoblox-bddi-str-configuration-modify-success-policyzone.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-configuration-modify-success-policyzone&type=code)
- [infoblox-bddi-str-configuration-modify-success-transfersuccess](CodeChanges/infoblox-bddi-str-configuration-modify-success-transfersuccess.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-configuration-modify-success-transfersuccess&type=code)
- [infoblox-bddi-str-dhcp-discover-dhcpd](CodeChanges/infoblox-bddi-str-dhcp-discover-dhcpd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-dhcp-discover-dhcpd&type=code)
- [infoblox-bddi-str-dhcp-session-success-dhcprequest](CodeChanges/infoblox-bddi-str-dhcp-session-success-dhcprequest.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-dhcp-session-success-dhcprequest&type=code)
- [infoblox-bddi-str-dhcp-session-success-dynamicleases](CodeChanges/infoblox-bddi-str-dhcp-session-success-dynamicleases.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-dhcp-session-success-dynamicleases&type=code)
- [infoblox-bddi-str-dhcp-traffic-dhcpdecline](CodeChanges/infoblox-bddi-str-dhcp-traffic-dhcpdecline.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-dhcp-traffic-dhcpdecline&type=code)
- [infoblox-bddi-str-dhcp-traffic-dhcpexpire](CodeChanges/infoblox-bddi-str-dhcp-traffic-dhcpexpire.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-dhcp-traffic-dhcpexpire&type=code)
- [infoblox-bddi-str-dhcp-traffic-dhcprelease](CodeChanges/infoblox-bddi-str-dhcp-traffic-dhcprelease.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-dhcp-traffic-dhcprelease&type=code)
- [infoblox-bddi-str-dhcp-traffic-release](CodeChanges/infoblox-bddi-str-dhcp-traffic-release.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-dhcp-traffic-release&type=code)
- [infoblox-bddi-str-dhcp-traffic-success-dhcpd](CodeChanges/infoblox-bddi-str-dhcp-traffic-success-dhcpd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-dhcp-traffic-success-dhcpd&type=code)
- [infoblox-bddi-str-dns-record-delete-httpd](CodeChanges/infoblox-bddi-str-dns-record-delete-httpd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-dns-record-delete-httpd&type=code)
- [infoblox-bddi-str-dns-request-successresolving](CodeChanges/infoblox-bddi-str-dns-request-successresolving.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-dns-request-successresolving&type=code)
- [infoblox-bddi-str-endpoint-login-success-dhcpack](CodeChanges/infoblox-bddi-str-endpoint-login-success-dhcpack.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-endpoint-login-success-dhcpack&type=code)
- [infoblox-bddi-str-endpoint-login-success-dhcpoffer](CodeChanges/infoblox-bddi-str-endpoint-login-success-dhcpoffer.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-endpoint-login-success-dhcpoffer&type=code)
- [infoblox-bddi-str-endpoint-login-success-requestdhcp](CodeChanges/infoblox-bddi-str-endpoint-login-success-requestdhcp.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-endpoint-login-success-requestdhcp&type=code)
- [infoblox-bddi-str-file-write-success-backupsuccess](CodeChanges/infoblox-bddi-str-file-write-success-backupsuccess.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-file-write-success-backupsuccess&type=code)
- [infoblox-bddi-str-network-notification-addforwardreverse](CodeChanges/infoblox-bddi-str-network-notification-addforwardreverse.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-addforwardreverse&type=code)
- [infoblox-bddi-str-network-notification-dhcpdissued](CodeChanges/infoblox-bddi-str-network-notification-dhcpdissued.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-dhcpdissued&type=code)
- [infoblox-bddi-str-network-notification-forwardmapupdate](CodeChanges/infoblox-bddi-str-network-notification-forwardmapupdate.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-forwardmapupdate&type=code)
- [infoblox-bddi-str-network-notification-removedforwardmap](CodeChanges/infoblox-bddi-str-network-notification-removedforwardmap.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-removedforwardmap&type=code)
- [infoblox-bddi-str-network-notification-removedreversemap](CodeChanges/infoblox-bddi-str-network-notification-removedreversemap.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-removedreversemap&type=code)
- [infoblox-bddi-str-network-notification-reversemapupdate](CodeChanges/infoblox-bddi-str-network-notification-reversemapupdate.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-reversemapupdate&type=code)
- [infoblox-bddi-str-network-notification-success-balancedpool](CodeChanges/infoblox-bddi-str-network-notification-success-balancedpool.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-success-balancedpool&type=code)
- [infoblox-bddi-str-network-notification-success-balancingpool](CodeChanges/infoblox-bddi-str-network-notification-success-balancingpool.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-success-balancingpool&type=code)
- [infoblox-bddi-str-network-notification-success-deltadiskopen](CodeChanges/infoblox-bddi-str-network-notification-success-deltadiskopen.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-success-deltadiskopen&type=code)
- [infoblox-bddi-str-network-notification-success-dhcpnakon](CodeChanges/infoblox-bddi-str-network-notification-success-dhcpnakon.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-success-dhcpnakon&type=code)
- [infoblox-bddi-str-network-notification-success-disconnected](CodeChanges/infoblox-bddi-str-network-notification-success-disconnected.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-success-disconnected&type=code)
- [infoblox-bddi-str-network-notification-success-dnsupdatelatency](CodeChanges/infoblox-bddi-str-network-notification-success-dnsupdatelatency.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-success-dnsupdatelatency&type=code)
- [infoblox-bddi-str-network-notification-success-dnsupdatetimeoutcount](CodeChanges/infoblox-bddi-str-network-notification-success-dnsupdatetimeoutcount.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-success-dnsupdatetimeoutcount&type=code)
- [infoblox-bddi-str-network-notification-success-failoverpeer](CodeChanges/infoblox-bddi-str-network-notification-success-failoverpeer.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-success-failoverpeer&type=code)
- [infoblox-bddi-str-network-notification-success-forwardmap](CodeChanges/infoblox-bddi-str-network-notification-success-forwardmap.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-success-forwardmap&type=code)
- [infoblox-bddi-str-network-notification-success-leasepublishingdisabled](CodeChanges/infoblox-bddi-str-network-notification-success-leasepublishingdisabled.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-success-leasepublishingdisabled&type=code)
- [infoblox-bddi-str-network-notification-success-leasetodatabase](CodeChanges/infoblox-bddi-str-network-notification-success-leasetodatabase.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-success-leasetodatabase&type=code)
- [infoblox-bddi-str-network-notification-success-nopeer](CodeChanges/infoblox-bddi-str-network-notification-success-nopeer.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-success-nopeer&type=code)
- [infoblox-bddi-str-network-notification-success-outofsync](CodeChanges/infoblox-bddi-str-network-notification-success-outofsync.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-success-outofsync&type=code)
- [infoblox-bddi-str-network-notification-success-retryingdnsupdates](CodeChanges/infoblox-bddi-str-network-notification-success-retryingdnsupdates.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-success-retryingdnsupdates&type=code)
- [infoblox-bddi-str-network-notification-success-uidlease](CodeChanges/infoblox-bddi-str-network-notification-success-uidlease.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-success-uidlease&type=code)
- [infoblox-bddi-str-network-notification-unableaddforwardmap](CodeChanges/infoblox-bddi-str-network-notification-unableaddforwardmap.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-network-notification-unableaddforwardmap&type=code)
- [infoblox-bddi-str-vpn-session-success-connectioninitiated](CodeChanges/infoblox-bddi-str-vpn-session-success-connectioninitiated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-bddi-str-vpn-session-success-connectioninitiated&type=code)
- [infoblox-nios-kv-app-notification-failure](CodeChanges/infoblox-nios-kv-app-notification-failure.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20infoblox-nios-kv-app-notification-failure&type=code)
- [microsoft-azuread-cef-app-login-clientappused](CodeChanges/microsoft-azuread-cef-app-login-clientappused.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuread-cef-app-login-clientappused&type=code)
- [microsoft-evnetworkprofile-xml-endpoint-activity-success-networkprofile](CodeChanges/microsoft-evnetworkprofile-xml-endpoint-activity-success-networkprofile.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evnetworkprofile-xml-endpoint-activity-success-networkprofile&type=code)
- [microsoft-evsecurity-kv-endpoint-login-success-successfullyloggedon](CodeChanges/microsoft-evsecurity-kv-endpoint-login-success-successfullyloggedon.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-success-successfullyloggedon&type=code)
- [microsoft-evsecurity-xml-endpoint-login-success-4624-1](CodeChanges/microsoft-evsecurity-xml-endpoint-login-success-4624-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-login-success-4624-1&type=code)
- [microsoft-evsecurity-xml-network-session-fail-4984](CodeChanges/microsoft-evsecurity-xml-network-session-fail-4984.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-network-session-fail-4984&type=code)
- [microsoft-evsecurity-xml-registry-create-success-4657](CodeChanges/microsoft-evsecurity-xml-registry-create-success-4657.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-registry-create-success-4657&type=code)
- [microsoft-o365-cef-app-login-fail-userloginfailed](CodeChanges/microsoft-o365-cef-app-login-fail-userloginfailed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-login-fail-userloginfailed&type=code)
- [microsoft-sysmon-json-log-4](CodeChanges/microsoft-sysmon-json-log-4.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-sysmon-json-log-4&type=code)
- [microsoft-sysmon-json-process-create-success-processcreate](CodeChanges/microsoft-sysmon-json-process-create-success-processcreate.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-sysmon-json-process-create-success-processcreate&type=code)
- [microsoft-sysmon-xml-dll-load-7](CodeChanges/microsoft-sysmon-xml-dll-load-7.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-sysmon-xml-dll-load-7&type=code)
- [microsoft-sysmon-xml-file-stream-create-15](CodeChanges/microsoft-sysmon-xml-file-stream-create-15.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-sysmon-xml-file-stream-create-15&type=code)
- [microsoft-sysmon-xml-file-time-modify-2-1](CodeChanges/microsoft-sysmon-xml-file-time-modify-2-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-sysmon-xml-file-time-modify-2-1&type=code)
- [microsoft-sysmon-xml-log-4](CodeChanges/microsoft-sysmon-xml-log-4.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-sysmon-xml-log-4&type=code)
- [microsoft-sysmon-xml-process-close-5](CodeChanges/microsoft-sysmon-xml-process-close-5.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-sysmon-xml-process-close-5&type=code)
- [microsoft-sysmon-xml-registry-12](CodeChanges/microsoft-sysmon-xml-registry-12.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-sysmon-xml-registry-12&type=code)
- [microsoft-sysmon-xml-service-state-modify-4](CodeChanges/microsoft-sysmon-xml-service-state-modify-4.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-sysmon-xml-service-state-modify-4&type=code)
- [netskope-sc-json-network-session-success-typenetwork](CodeChanges/netskope-sc-json-network-session-success-typenetwork.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20netskope-sc-json-network-session-success-typenetwork&type=code)
- [okta-amfa-cef-app-login-success-coreuserauthloginsuccess](CodeChanges/okta-amfa-cef-app-login-success-coreuserauthloginsuccess.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20okta-amfa-cef-app-login-success-coreuserauthloginsuccess&type=code)
- [okta-amfa-json-app-login-success-evaluatesignon-1](CodeChanges/okta-amfa-json-app-login-success-evaluatesignon-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20okta-amfa-json-app-login-success-evaluatesignon-1&type=code)
- [servicenow-s-cef-file-syscreated](CodeChanges/servicenow-s-cef-file-syscreated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20servicenow-s-cef-file-syscreated&type=code)
- [servicenow-s-json-http-session-success-transcation](CodeChanges/servicenow-s-json-http-session-success-transcation.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20servicenow-s-json-http-session-success-transcation&type=code)
- [unix-ad-kv-process-create-fail-syscall](CodeChanges/unix-ad-kv-process-create-fail-syscall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-ad-kv-process-create-fail-syscall&type=code)
- [unix-ad-str-endpoint-activity-auditd](CodeChanges/unix-ad-str-endpoint-activity-auditd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-ad-str-endpoint-activity-auditd&type=code)
- [unix-ad-str-endpoint-authentication-loginfailed](CodeChanges/unix-ad-str-endpoint-authentication-loginfailed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-ad-str-endpoint-authentication-loginfailed&type=code)
- [unix-dhcpd-csv-dhcp-session-success-dhcpdrenewed](CodeChanges/unix-dhcpd-csv-dhcp-session-success-dhcpdrenewed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-dhcpd-csv-dhcp-session-success-dhcpdrenewed&type=code)
- [unix-dhcpd-str-dhcp-discover-nofreeleases](CodeChanges/unix-dhcpd-str-dhcp-discover-nofreeleases.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-dhcpd-str-dhcp-discover-nofreeleases&type=code)
- [unix-dhcpd-str-dhcp-session-success-forwardmap](CodeChanges/unix-dhcpd-str-dhcp-session-success-forwardmap.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-dhcpd-str-dhcp-session-success-forwardmap&type=code)
- [unix-dhcpd-str-dhcp-session-success-reversemap](CodeChanges/unix-dhcpd-str-dhcp-session-success-reversemap.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-dhcpd-str-dhcp-session-success-reversemap&type=code)
- [unix-sm-kv-email-delay](CodeChanges/unix-sm-kv-email-delay.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-sm-kv-email-delay&type=code)
- [unix-sm-kv-email-send](CodeChanges/unix-sm-kv-email-send.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-sm-kv-email-send&type=code)
- [unix-unix-kv-database-login-authentication](CodeChanges/unix-unix-kv-database-login-authentication.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-database-login-authentication&type=code)
- [unix-unix-kv-email-send-success-smtp](CodeChanges/unix-unix-kv-email-send-success-smtp.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-email-send-success-smtp&type=code)
- [unix-unix-kv-endpoint-activity-fail-integrityfail](CodeChanges/unix-unix-kv-endpoint-activity-fail-integrityfail.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-endpoint-activity-fail-integrityfail&type=code)
- [unix-unix-kv-endpoint-activity-success-bprmfcaps](CodeChanges/unix-unix-kv-endpoint-activity-success-bprmfcaps.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-endpoint-activity-success-bprmfcaps&type=code)
- [unix-unix-kv-endpoint-activity-success-sockaddr](CodeChanges/unix-unix-kv-endpoint-activity-success-sockaddr.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-endpoint-activity-success-sockaddr&type=code)
- [unix-unix-kv-endpoint-login-fail-logindenied](CodeChanges/unix-unix-kv-endpoint-login-fail-logindenied.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-endpoint-login-fail-logindenied&type=code)
- [unix-unix-kv-endpoint-login-sshdauth](CodeChanges/unix-unix-kv-endpoint-login-sshdauth.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-endpoint-login-sshdauth&type=code)
- [unix-unix-kv-endpoint-login-success-userauth](CodeChanges/unix-unix-kv-endpoint-login-success-userauth.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-endpoint-login-success-userauth&type=code)
- [unix-unix-kv-endpoint-login-success-userauth-1](CodeChanges/unix-unix-kv-endpoint-login-success-userauth-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-endpoint-login-success-userauth-1&type=code)
- [unix-unix-kv-endpoint-login-userlogin](CodeChanges/unix-unix-kv-endpoint-login-userlogin.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-endpoint-login-userlogin&type=code)
- [unix-unix-kv-endpoint-login-userstart](CodeChanges/unix-unix-kv-endpoint-login-userstart.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-endpoint-login-userstart&type=code)
- [unix-unix-kv-endpoint-start-stop-virtcontrol](CodeChanges/unix-unix-kv-endpoint-start-stop-virtcontrol.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-endpoint-start-stop-virtcontrol&type=code)
- [unix-unix-kv-process-create-success-command](CodeChanges/unix-unix-kv-process-create-success-command.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-process-create-success-command&type=code)
- [unix-unix-kv-process-create-success-exe](CodeChanges/unix-unix-kv-process-create-success-exe.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-process-create-success-exe&type=code)
- [unix-unix-kv-process-create-success-execve](CodeChanges/unix-unix-kv-process-create-success-execve.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-process-create-success-execve&type=code)
- [unix-unix-kv-service-start-success-servicestart](CodeChanges/unix-unix-kv-service-start-success-servicestart.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-service-start-success-servicestart&type=code)
- [unix-unix-kv-service-stop-success-servicestop](CodeChanges/unix-unix-kv-service-stop-success-servicestop.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-service-stop-success-servicestop&type=code)
- [unix-unix-kv-ssh-traffic-audispd](CodeChanges/unix-unix-kv-ssh-traffic-audispd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-ssh-traffic-audispd&type=code)
- [unix-unix-kv-ssh-traffic-sshuserauth](CodeChanges/unix-unix-kv-ssh-traffic-sshuserauth.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-ssh-traffic-sshuserauth&type=code)
- [unix-unix-kv-user-create-success-useradd](CodeChanges/unix-unix-kv-user-create-success-useradd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-user-create-success-useradd&type=code)
- [unix-unix-mix-ssh-traffic-success-ssh2accepted](CodeChanges/unix-unix-mix-ssh-traffic-success-ssh2accepted.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-mix-ssh-traffic-success-ssh2accepted&type=code)
- [unix-unix-mix-user-password-modify-success-passwordchanged](CodeChanges/unix-unix-mix-user-password-modify-success-passwordchanged.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-mix-user-password-modify-success-passwordchanged&type=code)
- [unix-unix-mix-user-switch-success-sshdsession](CodeChanges/unix-unix-mix-user-switch-success-sshdsession.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-mix-user-switch-success-sshdsession&type=code)
- [unix-unix-mix-user-switch-success-susession](CodeChanges/unix-unix-mix-user-switch-success-susession.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-mix-user-switch-success-susession&type=code)
- [unix-unix-str-alert-trigger-sshdbreakinattempt](CodeChanges/unix-unix-str-alert-trigger-sshdbreakinattempt.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-alert-trigger-sshdbreakinattempt&type=code)
- [unix-unix-str-app-activity-sftp-server](CodeChanges/unix-unix-str-app-activity-sftp-server.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-app-activity-sftp-server&type=code)
- [unix-unix-str-cron-session-success-sessionopened](CodeChanges/unix-unix-str-cron-session-success-sessionopened.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-cron-session-success-sessionopened&type=code)
- [unix-unix-str-dhcp-session-success-appliedadd](CodeChanges/unix-unix-str-dhcp-session-success-appliedadd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-dhcp-session-success-appliedadd&type=code)
- [unix-unix-str-dns-record-create-success-registeringnewaddress](CodeChanges/unix-unix-str-dns-record-create-success-registeringnewaddress.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-dns-record-create-success-registeringnewaddress&type=code)
- [unix-unix-str-dns-record-delete-success-withdrawingaddresrecord](CodeChanges/unix-unix-str-dns-record-delete-success-withdrawingaddresrecord.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-dns-record-delete-success-withdrawingaddresrecord&type=code)
- [unix-unix-str-endpoint-activity-anacron](CodeChanges/unix-unix-str-endpoint-activity-anacron.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-activity-anacron&type=code)
- [unix-unix-str-endpoint-activity-crond](CodeChanges/unix-unix-str-endpoint-activity-crond.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-activity-crond&type=code)
- [unix-unix-str-endpoint-activity-fail-sshdfatal](CodeChanges/unix-unix-str-endpoint-activity-fail-sshdfatal.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-activity-fail-sshdfatal&type=code)
- [unix-unix-str-endpoint-activity-smtpd](CodeChanges/unix-unix-str-endpoint-activity-smtpd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-activity-smtpd&type=code)
- [unix-unix-str-endpoint-activity-sshd](CodeChanges/unix-unix-str-endpoint-activity-sshd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-activity-sshd&type=code)
- [unix-unix-str-endpoint-activity-system](CodeChanges/unix-unix-str-endpoint-activity-system.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-activity-system&type=code)
- [unix-unix-str-endpoint-activity-systemd](CodeChanges/unix-unix-str-endpoint-activity-systemd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-activity-systemd&type=code)
- [unix-unix-str-endpoint-authentication-smbdunabletovalidate](CodeChanges/unix-unix-str-endpoint-authentication-smbdunabletovalidate.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-authentication-smbdunabletovalidate&type=code)
- [unix-unix-str-endpoint-authentication-sshdaccepted](CodeChanges/unix-unix-str-endpoint-authentication-sshdaccepted.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-authentication-sshdaccepted&type=code)
- [unix-unix-str-endpoint-authentication-sshderrorretrieve](CodeChanges/unix-unix-str-endpoint-authentication-sshderrorretrieve.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-authentication-sshderrorretrieve&type=code)
- [unix-unix-str-endpoint-authentication-sshdnotreceiveid](CodeChanges/unix-unix-str-endpoint-authentication-sshdnotreceiveid.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-authentication-sshdnotreceiveid&type=code)
- [unix-unix-str-endpoint-login-authentication](CodeChanges/unix-unix-str-endpoint-login-authentication.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-login-authentication&type=code)
- [unix-unix-str-endpoint-login-fail-check](CodeChanges/unix-unix-str-endpoint-login-fail-check.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-login-fail-check&type=code)
- [unix-unix-str-endpoint-login-fail-expiredpassword](CodeChanges/unix-unix-str-endpoint-login-fail-expiredpassword.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-login-fail-expiredpassword&type=code)
- [unix-unix-str-endpoint-login-fail-failedpassword](CodeChanges/unix-unix-str-endpoint-login-fail-failedpassword.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-login-fail-failedpassword&type=code)
- [unix-unix-str-endpoint-login-fail-invaliduser](CodeChanges/unix-unix-str-endpoint-login-fail-invaliduser.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-login-fail-invaliduser&type=code)
- [unix-unix-str-endpoint-login-fail-manyauthfail](CodeChanges/unix-unix-str-endpoint-login-fail-manyauthfail.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-login-fail-manyauthfail&type=code)
- [unix-unix-str-endpoint-login-fail-noauth](CodeChanges/unix-unix-str-endpoint-login-fail-noauth.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-login-fail-noauth&type=code)
- [unix-unix-str-endpoint-login-fail-ssh38](CodeChanges/unix-unix-str-endpoint-login-fail-ssh38.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-login-fail-ssh38&type=code)
- [unix-unix-str-endpoint-login-fail-sshdauthfailed](CodeChanges/unix-unix-str-endpoint-login-fail-sshdauthfailed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-login-fail-sshdauthfailed&type=code)
- [unix-unix-str-endpoint-login-fail-unablesshd](CodeChanges/unix-unix-str-endpoint-login-fail-unablesshd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-login-fail-unablesshd&type=code)
- [unix-unix-str-endpoint-login-sshdconnectionfrom](CodeChanges/unix-unix-str-endpoint-login-sshdconnectionfrom.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-login-sshdconnectionfrom&type=code)
- [unix-unix-str-endpoint-login-sshdrefusedconnect](CodeChanges/unix-unix-str-endpoint-login-sshdrefusedconnect.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-login-sshdrefusedconnect&type=code)
- [unix-unix-str-endpoint-login-success-authsucceede](CodeChanges/unix-unix-str-endpoint-login-success-authsucceede.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-login-success-authsucceede&type=code)
- [unix-unix-str-endpoint-logout-disconnected](CodeChanges/unix-unix-str-endpoint-logout-disconnected.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-logout-disconnected&type=code)
- [unix-unix-str-endpoint-logout-sshdconnectionclosed](CodeChanges/unix-unix-str-endpoint-logout-sshdconnectionclosed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-logout-sshdconnectionclosed&type=code)
- [unix-unix-str-endpoint-logout-sshddisconnected](CodeChanges/unix-unix-str-endpoint-logout-sshddisconnected.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-logout-sshddisconnected&type=code)
- [unix-unix-str-endpoint-logout-sshdreceiveddisconnect](CodeChanges/unix-unix-str-endpoint-logout-sshdreceiveddisconnect.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-logout-sshdreceiveddisconnect&type=code)
- [unix-unix-str-endpoint-notification-bash](CodeChanges/unix-unix-str-endpoint-notification-bash.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-notification-bash&type=code)
- [unix-unix-str-endpoint-notification-passwordexpire](CodeChanges/unix-unix-str-endpoint-notification-passwordexpire.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-notification-passwordexpire&type=code)
- [unix-unix-str-endpoint-notification-selinux](CodeChanges/unix-unix-str-endpoint-notification-selinux.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-notification-selinux&type=code)
- [unix-unix-str-endpoint-notification-sshdset](CodeChanges/unix-unix-str-endpoint-notification-sshdset.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-notification-sshdset&type=code)
- [unix-unix-str-endpoint-notification-success-avahidaemon](CodeChanges/unix-unix-str-endpoint-notification-success-avahidaemon.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-notification-success-avahidaemon&type=code)
- [unix-unix-str-endpoint-notification-success-catchall](CodeChanges/unix-unix-str-endpoint-notification-success-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-notification-success-catchall&type=code)
- [unix-unix-str-endpoint-notification-success-config](CodeChanges/unix-unix-str-endpoint-notification-success-config.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-notification-success-config&type=code)
- [unix-unix-str-endpoint-notification-success-cron](CodeChanges/unix-unix-str-endpoint-notification-success-cron.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-notification-success-cron&type=code)
- [unix-unix-str-endpoint-notification-success-multipathd](CodeChanges/unix-unix-str-endpoint-notification-success-multipathd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-notification-success-multipathd&type=code)
- [unix-unix-str-endpoint-notification-success-snapd](CodeChanges/unix-unix-str-endpoint-notification-success-snapd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-notification-success-snapd&type=code)
- [unix-unix-str-endpoint-notification-success-systemd](CodeChanges/unix-unix-str-endpoint-notification-success-systemd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-notification-success-systemd&type=code)
- [unix-unix-str-endpoint-time-modify-synchronized](CodeChanges/unix-unix-str-endpoint-time-modify-synchronized.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-time-modify-synchronized&type=code)
- [unix-unix-str-file-read-success-close](CodeChanges/unix-unix-str-file-read-success-close.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-file-read-success-close&type=code)
- [unix-unix-str-file-read-success-open](CodeChanges/unix-unix-str-file-read-success-open.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-file-read-success-open&type=code)
- [unix-unix-str-file-write-success](CodeChanges/unix-unix-str-file-write-success.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-file-write-success&type=code)
- [unix-unix-str-group-create-success-groupadd](CodeChanges/unix-unix-str-group-create-success-groupadd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-group-create-success-groupadd&type=code)
- [unix-unix-str-group-delete-success-groupdel](CodeChanges/unix-unix-str-group-delete-success-groupdel.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-group-delete-success-groupdel&type=code)
- [unix-unix-str-group-member-add-success-gpasswd](CodeChanges/unix-unix-str-group-member-add-success-gpasswd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-group-member-add-success-gpasswd&type=code)
- [unix-unix-str-group-member-add-success-useradd](CodeChanges/unix-unix-str-group-member-add-success-useradd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-group-member-add-success-useradd&type=code)
- [unix-unix-str-group-member-add-success-usermod](CodeChanges/unix-unix-str-group-member-add-success-usermod.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-group-member-add-success-usermod&type=code)
- [unix-unix-str-group-member-add-success-usermod-1](CodeChanges/unix-unix-str-group-member-add-success-usermod-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-group-member-add-success-usermod-1&type=code)
- [unix-unix-str-group-member-remove-success-removed](CodeChanges/unix-unix-str-group-member-remove-success-removed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-group-member-remove-success-removed&type=code)
- [unix-unix-str-network-notification-success-networkmanager](CodeChanges/unix-unix-str-network-notification-success-networkmanager.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-network-notification-success-networkmanager&type=code)
- [unix-unix-str-network-start-snmpd](CodeChanges/unix-unix-str-network-start-snmpd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-network-start-snmpd&type=code)
- [unix-unix-str-scheduled-task-create-success-cmd](CodeChanges/unix-unix-str-scheduled-task-create-success-cmd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-scheduled-task-create-success-cmd&type=code)
- [unix-unix-str-scheduled-task-create-success-croncmd](CodeChanges/unix-unix-str-scheduled-task-create-success-croncmd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-scheduled-task-create-success-croncmd&type=code)
- [unix-unix-str-scheduled-task-start-anacronjob](CodeChanges/unix-unix-str-scheduled-task-start-anacronjob.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-scheduled-task-start-anacronjob&type=code)
- [unix-unix-str-scheduled-task-start-crond](CodeChanges/unix-unix-str-scheduled-task-start-crond.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-scheduled-task-start-crond&type=code)
- [unix-unix-str-scheduled-task-start-runningprogram](CodeChanges/unix-unix-str-scheduled-task-start-runningprogram.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-scheduled-task-start-runningprogram&type=code)
- [unix-unix-str-smtp-close-lostconnection](CodeChanges/unix-unix-str-smtp-close-lostconnection.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-smtp-close-lostconnection&type=code)
- [unix-unix-str-ssh-close-success-sessionclosed](CodeChanges/unix-unix-str-ssh-close-success-sessionclosed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-ssh-close-success-sessionclosed&type=code)
- [unix-unix-str-ssh-traffic-success-sftpsessionopened](CodeChanges/unix-unix-str-ssh-traffic-success-sftpsessionopened.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-ssh-traffic-success-sftpsessionopened&type=code)
- [unix-unix-str-user-delete-success-deleteuser](CodeChanges/unix-unix-str-user-delete-success-deleteuser.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-user-delete-success-deleteuser&type=code)
- [unix-unix-str-user-delete-success-deleteuser-1](CodeChanges/unix-unix-str-user-delete-success-deleteuser-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-user-delete-success-deleteuser-1&type=code)
- [unix-unix-str-user-modify-usermod](CodeChanges/unix-unix-str-user-modify-usermod.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-user-modify-usermod&type=code)
- [unix-unix-str-user-password-modify-fail-keyringpassword](CodeChanges/unix-unix-str-user-password-modify-fail-keyringpassword.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-user-password-modify-fail-keyringpassword&type=code)
- [unix-unix-str-user-password-modify-success-chage](CodeChanges/unix-unix-str-user-password-modify-success-chage.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-user-password-modify-success-chage&type=code)
- [unix-unix-str-user-switch-success-accountswitch-1](CodeChanges/unix-unix-str-user-switch-success-accountswitch-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-user-switch-success-accountswitch-1&type=code)
- [unix-unix-str-user-switch-success-pam_unix](CodeChanges/unix-unix-str-user-switch-success-pam_unix.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-user-switch-success-pam_unix&type=code)
- [unix-unixauditd-str-endpoint-login-success-authenticated](CodeChanges/unix-unixauditd-str-endpoint-login-success-authenticated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unixauditd-str-endpoint-login-success-authenticated&type=code)
- [unix-unixauditd-str-endpoint-login-success-authentication](CodeChanges/unix-unixauditd-str-endpoint-login-success-authentication.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unixauditd-str-endpoint-login-success-authentication&type=code)
- [unix-unixnamed-str-app-activity-success-lameservers](CodeChanges/unix-unixnamed-str-app-activity-success-lameservers.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unixnamed-str-app-activity-success-lameservers&type=code)
- [unix-unixnamed-str-app-notification-lameserverresolving](CodeChanges/unix-unixnamed-str-app-notification-lameserverresolving.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unixnamed-str-app-notification-lameserverresolving&type=code)
- [unix-unixnamed-str-app-notification-namedconnected](CodeChanges/unix-unixnamed-str-app-notification-namedconnected.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unixnamed-str-app-notification-namedconnected&type=code)
- [unix-unixnamed-str-app-notification-resolving](CodeChanges/unix-unixnamed-str-app-notification-resolving.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unixnamed-str-app-notification-resolving&type=code)
- [unix-unixnamed-str-app-notification-signature](CodeChanges/unix-unixnamed-str-app-notification-signature.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unixnamed-str-app-notification-signature&type=code)
- [unix-unixnamed-str-app-notification-success-cname](CodeChanges/unix-unixnamed-str-app-notification-success-cname.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unixnamed-str-app-notification-success-cname&type=code)
- [unix-unixnamed-str-app-notification-success-named](CodeChanges/unix-unixnamed-str-app-notification-success-named.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unixnamed-str-app-notification-success-named&type=code)
- [unix-unixnamed-str-app-notification-success-notify](CodeChanges/unix-unixnamed-str-app-notification-success-notify.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unixnamed-str-app-notification-success-notify&type=code)
- [unix-unixnamed-str-app-notification-transferredserial](CodeChanges/unix-unixnamed-str-app-notification-transferredserial.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unixnamed-str-app-notification-transferredserial&type=code)
- [unix-unixnamed-str-app-notification-zonenotify](CodeChanges/unix-unixnamed-str-app-notification-zonenotify.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unixnamed-str-app-notification-zonenotify&type=code)
- [unix-unixnamed-str-dns-request-namedquery](CodeChanges/unix-unixnamed-str-dns-request-namedquery.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unixnamed-str-dns-request-namedquery&type=code)
- [unix-unixnamed-str-network-notification-notifyforzone](CodeChanges/unix-unixnamed-str-network-notification-notifyforzone.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unixnamed-str-network-notification-notifyforzone&type=code)
- [unix-unixnamed-str-network-notification-rfc1918](CodeChanges/unix-unixnamed-str-network-notification-rfc1918.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unixnamed-str-network-notification-rfc1918&type=code)
- [unix-unixnamed-str-network-notification-success-rcoderesolving](CodeChanges/unix-unixnamed-str-network-notification-success-rcoderesolving.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unixnamed-str-network-notification-success-rcoderesolving&type=code)
- [unix-unixnamed-str-network-notification-transferstarted](CodeChanges/unix-unixnamed-str-network-notification-transferstarted.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unixnamed-str-network-notification-transferstarted&type=code)
- [vmware-carbonblack-sk4-alert-trigger-success-cbanalytics](CodeChanges/vmware-carbonblack-sk4-alert-trigger-success-cbanalytics.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-carbonblack-sk4-alert-trigger-success-cbanalytics&type=code)
- [vmware-carbonblackceedr-sk4-network-session-success-edr](CodeChanges/vmware-carbonblackceedr-sk4-network-session-success-edr.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-carbonblackceedr-sk4-network-session-success-edr&type=code)
- [zeek-z-json-email-send-receive-rcptto](CodeChanges/zeek-z-json-email-send-receive-rcptto.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zeek-z-json-email-send-receive-rcptto&type=code)
- [zeek-z-json-file-success-sbmfiles](CodeChanges/zeek-z-json-file-success-sbmfiles.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zeek-z-json-file-success-sbmfiles&type=code)

#### Edit Attribute
<a id="edit-attribute"></a>
- [checkpoint-avanan-json-alert-trigger-success-avanansecurityeventmalware](CodeChanges/checkpoint-avanan-json-alert-trigger-success-avanansecurityeventmalware.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-avanan-json-alert-trigger-success-avanansecurityeventmalware&type=code)
- [checkpoint-avanan-json-alert-trigger-success-securityeventmalware](CodeChanges/checkpoint-avanan-json-alert-trigger-success-securityeventmalware.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-avanan-json-alert-trigger-success-securityeventmalware&type=code)
- [checkpoint-avanan-json-alert-trigger-success-securityeventmalware-1](CodeChanges/checkpoint-avanan-json-alert-trigger-success-securityeventmalware-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-avanan-json-alert-trigger-success-securityeventmalware-1&type=code)
- [checkpoint-avanan-json-alert-trigger-success-severity](CodeChanges/checkpoint-avanan-json-alert-trigger-success-severity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-avanan-json-alert-trigger-success-severity&type=code)
- [checkpoint-avanan-json-alert-trigger-success-severity-1](CodeChanges/checkpoint-avanan-json-alert-trigger-success-severity-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-avanan-json-alert-trigger-success-severity-1&type=code)

#### Edit Regex Field
<a id="edit-regex-field"></a>
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
- [crowdstrike-falcon-json-alert-trigger-success-identityprotection](CodeChanges/crowdstrike-falcon-json-alert-trigger-success-identityprotection.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-alert-trigger-success-identityprotection&type=code)
- [crowdstrike-falcon-json-network-traffic-success-connectip](CodeChanges/crowdstrike-falcon-json-network-traffic-success-connectip.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-json-network-traffic-success-connectip&type=code)
- [crowdstrike-falcon-mix-dns-request-success-dnsrequest](CodeChanges/crowdstrike-falcon-mix-dns-request-success-dnsrequest.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-mix-dns-request-success-dnsrequest&type=code)
- [f5-bigip-str-network-notification-success](CodeChanges/f5-bigip-str-network-notification-success.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20f5-bigip-str-network-notification-success&type=code)
- [linux-dhcp-str-dhcp-session-success-dhcprequest](CodeChanges/linux-dhcp-str-dhcp-session-success-dhcprequest.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20linux-dhcp-str-dhcp-session-success-dhcprequest&type=code)
- [microsoft-azure-cef-group-member-remove-success-removefromgroup](CodeChanges/microsoft-azure-cef-group-member-remove-success-removefromgroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-cef-group-member-remove-success-removefromgroup&type=code)
- [microsoft-azuread-json-group-member-add-success-aadiam](CodeChanges/microsoft-azuread-json-group-member-add-success-aadiam.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuread-json-group-member-add-success-aadiam&type=code)
- [microsoft-azuread-json-group-member-remove-success-groupmemberremoved](CodeChanges/microsoft-azuread-json-group-member-remove-success-groupmemberremoved.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuread-json-group-member-remove-success-groupmemberremoved&type=code)
- [microsoft-azuremon-sk4-app-activity-auditevent](CodeChanges/microsoft-azuremon-sk4-app-activity-auditevent.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuremon-sk4-app-activity-auditevent&type=code)
- [microsoft-defenderep-json-alert-trigger-success-category](CodeChanges/microsoft-defenderep-json-alert-trigger-success-category.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-json-alert-trigger-success-category&type=code)
- [microsoft-defenderep-json-alert-trigger-success-collection](CodeChanges/microsoft-defenderep-json-alert-trigger-success-collection.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-json-alert-trigger-success-collection&type=code)
- [microsoft-defenderep-json-alert-trigger-success-exploit-1](CodeChanges/microsoft-defenderep-json-alert-trigger-success-exploit-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-json-alert-trigger-success-exploit-1&type=code)
- [microsoft-defenderep-json-alert-trigger-success-lateralmovement-1](CodeChanges/microsoft-defenderep-json-alert-trigger-success-lateralmovement-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-json-alert-trigger-success-lateralmovement-1&type=code)
- [microsoft-defenderep-json-alert-trigger-success-malware-1](CodeChanges/microsoft-defenderep-json-alert-trigger-success-malware-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-json-alert-trigger-success-malware-1&type=code)
- [microsoft-defenderep-json-alert-trigger-success-persistence-1](CodeChanges/microsoft-defenderep-json-alert-trigger-success-persistence-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-json-alert-trigger-success-persistence-1&type=code)
- [microsoft-defenderep-json-alert-trigger-success-persistence-2](CodeChanges/microsoft-defenderep-json-alert-trigger-success-persistence-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-json-alert-trigger-success-persistence-2&type=code)
- [microsoft-defenderep-json-alert-trigger-success-suspiciousactivity](CodeChanges/microsoft-defenderep-json-alert-trigger-success-suspiciousactivity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-json-alert-trigger-success-suspiciousactivity&type=code)
- [microsoft-defenderep-json-alert-trigger-success-unwantedsoftware](CodeChanges/microsoft-defenderep-json-alert-trigger-success-unwantedsoftware.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-json-alert-trigger-success-unwantedsoftware&type=code)
- [microsoft-evdirservice-xml-app-notification-success-directoryservice](CodeChanges/microsoft-evdirservice-xml-app-notification-success-directoryservice.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evdirservice-xml-app-notification-success-directoryservice&type=code)
- [microsoft-evsecurity-mix-user-enable-success-4722](CodeChanges/microsoft-evsecurity-mix-user-enable-success-4722.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-user-enable-success-4722&type=code)
- [microsoft-evsecurity-xml-user-name-modify-4781-1](CodeChanges/microsoft-evsecurity-xml-user-name-modify-4781-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-user-name-modify-4781-1&type=code)
- [microsoft-mcas-json-alert-trigger-success-download](CodeChanges/microsoft-mcas-json-alert-trigger-success-download.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-mcas-json-alert-trigger-success-download&type=code)
- [microsoft-mcas-json-alert-trigger-success-login](CodeChanges/microsoft-mcas-json-alert-trigger-success-login.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-mcas-json-alert-trigger-success-login&type=code)
- [microsoft-mcas-json-alert-trigger-success-ransomware](CodeChanges/microsoft-mcas-json-alert-trigger-success-ransomware.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-mcas-json-alert-trigger-success-ransomware&type=code)
- [microsoft-mcas-json-alert-trigger-success-velocity](CodeChanges/microsoft-mcas-json-alert-trigger-success-velocity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-mcas-json-alert-trigger-success-velocity&type=code)
- [microsoft-o365-sk4-app-file-operationworkload](CodeChanges/microsoft-o365-sk4-app-file-operationworkload.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-sk4-app-file-operationworkload&type=code)
- [microsoft-o365-sk4-app-file-workload](CodeChanges/microsoft-o365-sk4-app-file-workload.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-sk4-app-file-workload&type=code)
- [microsoft-sysmon-xml-process-create-success-processcreate](CodeChanges/microsoft-sysmon-xml-process-create-success-processcreate.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-sysmon-xml-process-create-success-processcreate&type=code)
- [mimecast-seg-cef-email-url](CodeChanges/mimecast-seg-cef-email-url.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20mimecast-seg-cef-email-url&type=code)
- [okta-amfa-mix-app-login-success-securitycontext](CodeChanges/okta-amfa-mix-app-login-success-securitycontext.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20okta-amfa-mix-app-login-success-securitycontext&type=code)
- [proofpoint-tappod-json-email-send-receive-sendmailfrom](CodeChanges/proofpoint-tappod-json-email-send-receive-sendmailfrom.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20proofpoint-tappod-json-email-send-receive-sendmailfrom&type=code)
- [proofpoint-tappod-json-email-send-receive-sendmailto](CodeChanges/proofpoint-tappod-json-email-send-receive-sendmailto.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20proofpoint-tappod-json-email-send-receive-sendmailto&type=code)
- [unix-auditd-kv-user-switch-success-userrolechange](CodeChanges/unix-auditd-kv-user-switch-success-userrolechange.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-auditd-kv-user-switch-success-userrolechange&type=code)
- [unix-unix-kv-endpoint-login-fail-ruser](CodeChanges/unix-unix-kv-endpoint-login-fail-ruser.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-endpoint-login-fail-ruser&type=code)

#### Removed Parser
<a id="removed-parser"></a>
- [mcafee-wg-leef-http-session-webgateway](CodeChanges/mcafee-wg-leef-http-session-webgateway.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20mcafee-wg-leef-http-session-webgateway&type=code)
- [microsoft-defendercloud-sk4-alert-trigger-success-simulated](CodeChanges/microsoft-defendercloud-sk4-alert-trigger-success-simulated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defendercloud-sk4-alert-trigger-success-simulated&type=code)
- [netskope-sc-json-alert-trigger-success-compromised](CodeChanges/netskope-sc-json-alert-trigger-success-compromised.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20netskope-sc-json-alert-trigger-success-compromised&type=code)
- [netskope-sc-json-app-activity-success-propertyupdated](CodeChanges/netskope-sc-json-app-activity-success-propertyupdated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20netskope-sc-json-app-activity-success-propertyupdated&type=code)
- [netskope-sc-json-app-login-success-loginsuccess](CodeChanges/netskope-sc-json-app-login-success-loginsuccess.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20netskope-sc-json-app-login-success-loginsuccess&type=code)
- [netskope-sc-sk4-app-login-success-page](CodeChanges/netskope-sc-sk4-app-login-success-page.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20netskope-sc-sk4-app-login-success-page&type=code)
- [netskope-sc-sk4-app-logout-success-logout](CodeChanges/netskope-sc-sk4-app-logout-success-logout.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20netskope-sc-sk4-app-logout-success-logout&type=code)
- [netskope-sc-sk4-app-notification-success-auditevent](CodeChanges/netskope-sc-sk4-app-notification-success-auditevent.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20netskope-sc-sk4-app-notification-success-auditevent&type=code)

</details>

<details>
<summary><strong id="parsertemplate">ParserTemplate (9)</strong></summary>


### Change Types
- [Changed Parsed Fields](#changed-parsed-fields)
- [Edit Regex Field](#edit-regex-field)

#### Changed Parsed Fields
<a id="changed-parsed-fields"></a>
- [crowdstrike-file-operations](CodeChanges/crowdstrike-file-operations.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-file-operations&type=code)
- [crowdstrike-json-app-notification](CodeChanges/crowdstrike-json-app-notification.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-json-app-notification&type=code)
- [s-common-ftp-app-activity](CodeChanges/s-common-ftp-app-activity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20s-common-ftp-app-activity&type=code)
- [s-infoblox-one-dhcp-dl-events](CodeChanges/s-infoblox-one-dhcp-dl-events.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20s-infoblox-one-dhcp-dl-events&type=code)
- [unix-kv-template](CodeChanges/unix-kv-template.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-kv-template&type=code)
- [unix-system-info](CodeChanges/unix-system-info.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-system-info&type=code)
- [xml-sysmon-activity](CodeChanges/xml-sysmon-activity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20xml-sysmon-activity&type=code)

#### Edit Regex Field
<a id="edit-regex-field"></a>
- [aws-cloudtrail-json](CodeChanges/aws-cloudtrail-json.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20aws-cloudtrail-json&type=code)
- [defender-atp-security-alert-events](CodeChanges/defender-atp-security-alert-events.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20defender-atp-security-alert-events&type=code)

</details>