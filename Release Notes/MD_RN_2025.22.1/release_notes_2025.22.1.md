# Content Package 2025.22.1

These release notes contain information about content package 2025.22.1, released on 23 Oct 2025.


## Enhancements
- Updated JSON extractor  fields for tenable-t-json-endpoint-scan-scaninformation parser.
- Updated the parser microsoft-defenderep-sk4-dll-load-deviceimageloadevents to improve file field parsing.
- Added new parsers proofpoint-tap-json-app-notification-success-phishingquarantine
- Updated pan-prisma-sk4-alert-trigger-success-prismacloud conditions to parse broader category of Prisma Cloud logs.
- Added new parser for product Azure virtual network
- Created new event builders for the parser microsoft-mcas-cef-file-write-success-appidonedrive
- Added new parsers for Extrahop logs: extrahop-revealx-leef-alert-trigger-success-extrahopdetection
- Updated the parser salesforce-sf-json-app-login-success-loginurl to match the new logs. Also, added the new field extractions as per the new logs.
- Added new parser checkpoint-hs-kv-alert-trigger-success-compromizedaccount
- Added new activity-type - group-member-add and group-member-remove event builders for parser: azure-azuread-json-app-activity-useractivitydisplayname.
- Added new parser nasuni-n-kv-app-activity
- Added New parsers and event builders for check point logs.
- Added 'dest_email_address' and 'group_name' for parser microsoft-mcas-cef-file-write-success-appidonedrive Created new event builders for the parser microsoft-mcas-cef-file-write-success-appidonedrive
- Added parsers and event builders for Cisco Firepower FMC logs
- Added New Enrichers: Invalid Domain-2 and Invalid Domain-3
- Added new parsers for Darktrace logs: darktrace-darktrace-json-alert-trigger-success-alertname, darktrace-darktrace-json-alert-trigger-success-suspiciousproperties
- Updated src_ip, dest_ip, browser, connection_id, mime, domain, src_country, host_ip, origin_ip, rule_reason, rule, region, method, http_response_code, severity and user field extractions for parser - menlo-ms-json-http-session-security.
- Added new parsers and event builders for Check Point Security Gateway logs.
- Added New parsers and event builders for check point logs.
- In the 'aws-cloudtrail-json' template, reduced three requestparameter parsing entries to two and updated the exa_regex to handle all patterns.
- Added Zero Networks parser to support new product .Parser Name  - zeronetworks-zeronetworks-json-app-activity-success-auditlogevent .
- Created new EventBuilders for the parser microsoft-azure-json-file-success-1 Modified EventBuilder conditions for the parser microsoft-azure-json-file-success-1 Updated the regexes in the parsers unix-unix-kv-endpoint-login-userlogin, unix-unix-kv-endpoint-login-userstart In the 'aws-cloudtrail-json' template, reduced three requestparameter parsing entries to two and updated the exa_regex to handle all patterns.
- Updated group_name, task_id, item_name, event_name, dest_user, activity_details and additional_info field extractions for parser: servicenow-s-json-http-session-success-transcation
- Developed new enricher service_type_text to enrich service_type_text value based on service_type value

## Addressed Issues
- Updated group_name field extractions for parser microsoft-evsecurity-xml-group-create-4754
- Updated src_ip & user field extractions for parser unix-unix-str-endpoint-activity-fail-sshd
- Added new parser for Microsoft - Active Directory Federation Services logs for event id  - 364.
- Updated precedence of zscaler-ia-cef-http-session-spriv parser.
- Updated src_ip regex for unix-unix-kv-endpoint-login-sshdauth parser.
- Updated src_ip, additional_info field extractions and event builder conditions for parser: fortinet-fortigate-kv-app-activity-system
- Fixed src_ip/dest_ip field to parser from LocalAddressIP4/RemoteAddressIP4 with respectively into crowdstrike-falcon-sk4-endpoint-login-userloginfail & crowdstrike-falcon-mix-endpoint-login-success-userlogon
- Updated group_name field extractions for parser: microsoft-evsecurity-kv-group-member-add-success-4756-2
- Added src_network_zone field for s-okta-app-login template.
- Updated imperva-securesphere-cef-alert-trigger-success-servergroup conditions to parse broader category of Imperva SecureSphere logs
- Fixed json regex for parsers google-cloudplatform-mix-app-activity-success-prototpayload, google-cloudplatform-json-endpoint-modify-success-computeprojectssetcommoninstancemetadata, google-cloudplatform-json-endpoint-modify-success-computeinstancessetmetadata, google-cloudplatform-json-disk-create-success-computedisksinsert, google-cloudplatform-json-disk-attach-success-computeinstancesattachdisk, google-cloudplatform-json-endpoint-create-success-betacomputeinstancesinsert
- Renamed field name action to result for microsoft-azurefw-json-network-session-azfwnetworkrule parser .
- Updated the parser abnormalsecurity-as-json-alert-trigger-success-attacktype-1 for extracting src_ip field.
- Updated src_mac, src_ip field extractions for parser: microsoft-nps-xml-radius-traffic-fail-6273, microsoft-evnps-xml-radius-traffic-success-6272
- Updated object, profile and host_type field extractions for parser - pan-tesm-csv-alert-trigger-hipmatch.
- Added uac_status,old_value,new_value fields for 4742 event_code parsers.
- Fixed regex of dest_ip and dest_port for parser amazon-awsguardduty-cef-alert-trigger-success-catsecurity
- Updated process_command_line field extraction for parser - microsoft-evsecurity-kv-process-create-success-mswineventlog4688.
- update parser 'amazon-awsguardduty-json-alert-trigger-success-sshbruteforce' with src_ip field mapping.
- Fixed host regex of parsers 1. cisco-asa-str-app-notification-success-sys 2. cisco-asa-str-app-notification-success-ssh 3. cisco-ios-str-endpoint-authentication-fail-authenticationfailed 4. cisco-asa-str-ssh-traffic-success-sshuserauth 5. cisco-asa-str-ssh-close-ssh 6. cisco-asa-str-ssh-start-session 7. cisco-ios-str-endpoint-authentication-success-authpassed
- Updated condition for parser apache-a-str-http-session-apacheaccess to parse unparsed logs.
- Changed parser precedence to correctly recognize Azure logs.
- Updated target and group_name fields for parser: microsoft-o365-cef-app-file-success-removememberfromgroup
- Updated target and group_name fields for parser: microsoft-o365-cef-app-file-success-addtogroup

## Code Changes
### ℹ️ How to Read This Document

Each item listed under **Code Changes** includes:

- **A link to a detailed change file**  
  Click the filename (e.g., `Carbon Black.md`) to open a full table showing what changed.

- **A search icon 🔍**  
  Click the 🔍 icon to search for this resource in the [Exabeam Content Library](https://github.com/ExabeamLabs/Content-Library-CIM2).


<details>
<summary><strong id="event-builder">Event Builder (68)</strong></summary>


### Change Types
- [Added Event Builder](#added-event-builder)
- [Edit Conditions](#edit-conditions)

#### Added Event Builder
<a id="added-event-builder"></a>
- [checkpoint-network-network-traffic-success-4](CodeChanges/checkpoint-network-network-traffic-success-4.md)
- [checkpoint-ngfw-alert-trigger-success-1](CodeChanges/checkpoint-ngfw-alert-trigger-success-1.md)
- [dl-checkpoint-network-network-notification-success](CodeChanges/dl-checkpoint-network-network-notification-success.md)
- [dl-checkpoint-network-network-notification-success-1](CodeChanges/dl-checkpoint-network-network-notification-success-1.md)
- [dl-cisco-firepower-app-login-success](CodeChanges/dl-cisco-firepower-app-login-success.md)
- [dl-cisco-firepower-app-logout-success](CodeChanges/dl-cisco-firepower-app-logout-success.md)
- [dl-cisco-firepower-policy-modify-success](CodeChanges/dl-cisco-firepower-policy-modify-success.md)
- [dl-microsoft-network-network-close-success](CodeChanges/dl-microsoft-network-network-close-success.md)
- [dl-proofpoint-tap-app-notification-success](CodeChanges/dl-proofpoint-tap-app-notification-success.md)
- [microsoft-365-app-activity-success-17](CodeChanges/microsoft-365-app-activity-success-17.md)
- [microsoft-365-file-copy-success-1](CodeChanges/microsoft-365-file-copy-success-1.md)
- [microsoft-365-file-delete-success-7](CodeChanges/microsoft-365-file-delete-success-7.md)
- [microsoft-365-file-move-success-1](CodeChanges/microsoft-365-file-move-success-1.md)
- [microsoft-365-file-rename-success-1](CodeChanges/microsoft-365-file-rename-success-1.md)
- [microsoft-365-file-restore-success](CodeChanges/microsoft-365-file-restore-success.md)
- [microsoft-365-file-share-fail](CodeChanges/microsoft-365-file-share-fail.md)
- [microsoft-365-file-share-success-1](CodeChanges/microsoft-365-file-share-success-1.md)
- [microsoft-365-folder-create-success-2](CodeChanges/microsoft-365-folder-create-success-2.md)
- [microsoft-365-folder-modify-success-1](CodeChanges/microsoft-365-folder-modify-success-1.md)
- [microsoft-365-group-create-success-1](CodeChanges/microsoft-365-group-create-success-1.md)
- [microsoft-365-group-member-add-success-1](CodeChanges/microsoft-365-group-member-add-success-1.md)
- [microsoft-365-group-member-remove-success-1](CodeChanges/microsoft-365-group-member-remove-success-1.md)
- [microsoft-365-policy-modify-success](CodeChanges/microsoft-365-policy-modify-success.md)
- [microsoft-azure-directory-create-fail](CodeChanges/microsoft-azure-directory-create-fail.md)
- [microsoft-azure-directory-create-success](CodeChanges/microsoft-azure-directory-create-success.md)
- [microsoft-azure-directory-delete-fail](CodeChanges/microsoft-azure-directory-delete-fail.md)
- [microsoft-azure-directory-delete-success](CodeChanges/microsoft-azure-directory-delete-success.md)
- [microsoft-azure-file-create-fail-2](CodeChanges/microsoft-azure-file-create-fail-2.md)
- [microsoft-azure-file-create-success-2](CodeChanges/microsoft-azure-file-create-success-2.md)
- [microsoft-azure-file-rename-fail](CodeChanges/microsoft-azure-file-rename-fail.md)
- [microsoft-azure-file-rename-success](CodeChanges/microsoft-azure-file-rename-success.md)
- [microsoft-azure-group-member-add-fail-1](CodeChanges/microsoft-azure-group-member-add-fail-1.md)
- [microsoft-azure-group-member-add-success-1](CodeChanges/microsoft-azure-group-member-add-success-1.md)
- [microsoft-azure-group-member-remove-success](CodeChanges/microsoft-azure-group-member-remove-success.md)
- [microsoft-network-network-traffic-fail-4](CodeChanges/microsoft-network-network-traffic-fail-4.md)
- [microsoft-network-network-traffic-success-3](CodeChanges/microsoft-network-network-traffic-success-3.md)
- [nasuni-app-activity-fail](CodeChanges/nasuni-app-activity-fail.md)
- [nasuni-app-activity-success](CodeChanges/nasuni-app-activity-success.md)
- [nasuni-file-owner-modify-fail](CodeChanges/nasuni-file-owner-modify-fail.md)
- [nasuni-file-owner-modify-success](CodeChanges/nasuni-file-owner-modify-success.md)
- [nasuni-file-rename-fail](CodeChanges/nasuni-file-rename-fail.md)
- [nasuni-file-rename-success](CodeChanges/nasuni-file-rename-success.md)
- [nasuni-file-write-fail](CodeChanges/nasuni-file-write-fail.md)
- [nasuni-file-write-success](CodeChanges/nasuni-file-write-success.md)
- [nasuni-folder-delete-fail](CodeChanges/nasuni-folder-delete-fail.md)
- [nasuni-folder-delete-success](CodeChanges/nasuni-folder-delete-success.md)
- [unix-unix-ssh-traffic-success-3](CodeChanges/unix-unix-ssh-traffic-success-3.md)
- [vmware-vcenter-user-password-modify-fail](CodeChanges/vmware-vcenter-user-password-modify-fail.md)
- [zeronetwork-app-activity-success](CodeChanges/zeronetwork-app-activity-success.md)

#### Edit Conditions
<a id="edit-conditions"></a>
- [dl-fortinet-fortigate-app-activity-success-2](CodeChanges/dl-fortinet-fortigate-app-activity-success-2.md)
- [dl-microsoft-azurefw-network-session-fail](CodeChanges/dl-microsoft-azurefw-network-session-fail.md)
- [dl-microsoft-azurefw-network-session-success](CodeChanges/dl-microsoft-azurefw-network-session-success.md)
- [fortinet-fortigate-app-login-fail](CodeChanges/fortinet-fortigate-app-login-fail.md)
- [fortinet-fortigate-app-login-success-2](CodeChanges/fortinet-fortigate-app-login-success-2.md)
- [google-cloudplatform-app-activity-success](CodeChanges/google-cloudplatform-app-activity-success.md)
- [microsoft-365-file-write-success-4](CodeChanges/microsoft-365-file-write-success-4.md)
- [microsoft-azure-app-activity-fail-3](CodeChanges/microsoft-azure-app-activity-fail-3.md)
- [microsoft-azure-app-activity-fail-6](CodeChanges/microsoft-azure-app-activity-fail-6.md)
- [microsoft-azure-app-activity-success-5](CodeChanges/microsoft-azure-app-activity-success-5.md)
- [microsoft-azure-app-activity-success-6](CodeChanges/microsoft-azure-app-activity-success-6.md)
- [microsoft-azure-file-delete-fail](CodeChanges/microsoft-azure-file-delete-fail.md)
- [microsoft-azure-file-delete-success-2](CodeChanges/microsoft-azure-file-delete-success-2.md)
- [microsoft-azure-file-read-fail](CodeChanges/microsoft-azure-file-read-fail.md)
- [microsoft-azure-file-read-success-2](CodeChanges/microsoft-azure-file-read-success-2.md)
- [microsoft-azure-file-write-fail](CodeChanges/microsoft-azure-file-write-fail.md)
- [microsoft-azure-file-write-success-1](CodeChanges/microsoft-azure-file-write-success-1.md)
- [unix-unix-endpoint-login-fail](CodeChanges/unix-unix-endpoint-login-fail.md)
- [unix-unix-ssh-traffic-success-2](CodeChanges/unix-unix-ssh-traffic-success-2.md)

</details>

<details>
<summary><strong id="parser">Parser (225)</strong></summary>


### Change Types
- [Could Not Compare](#could-not-compare)
- [Added Parser](#added-parser)
- [Changed](#changed)
- [Changed Parsed Fields](#changed-parsed-fields)
- [Edit Attribute](#edit-attribute)
- [Edit Regex Field](#edit-regex-field)

#### Could Not Compare
<a id="could-not-compare"></a>
- [cisco-asa-str-ssh-traffic-success-sshuserauth](CodeChanges/cisco-asa-str-ssh-traffic-success-sshuserauth.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-ssh-traffic-success-sshuserauth&type=code)
- [microsoft-evsecurity-xml-ds-object-modify-success-4742](CodeChanges/microsoft-evsecurity-xml-ds-object-modify-success-4742.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-ds-object-modify-success-4742&type=code)
- [tenable-t-json-endpoint-scan-scaninformation](CodeChanges/tenable-t-json-endpoint-scan-scaninformation.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20tenable-t-json-endpoint-scan-scaninformation&type=code)

#### Added Parser
<a id="added-parser"></a>
- [checkpoint-hs-kv-alert-trigger-success-compromizedaccount](CodeChanges/checkpoint-hs-kv-alert-trigger-success-compromizedaccount.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-hs-kv-alert-trigger-success-compromizedaccount&type=code)
- [checkpoint-ngfw-kv-alert-trigger-success-halert](CodeChanges/checkpoint-ngfw-kv-alert-trigger-success-halert.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-ngfw-kv-alert-trigger-success-halert&type=code)
- [checkpoint-ngfw-kv-network-traffic-denialofservice](CodeChanges/checkpoint-ngfw-kv-network-traffic-denialofservice.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-ngfw-kv-network-traffic-denialofservice&type=code)
- [checkpoint-ngfw-kv-network-traffic-scans](CodeChanges/checkpoint-ngfw-kv-network-traffic-scans.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-ngfw-kv-network-traffic-scans&type=code)
- [cisco-fp-str-app-login-success-loginsuccess](CodeChanges/cisco-fp-str-app-login-success-loginsuccess.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-fp-str-app-login-success-loginsuccess&type=code)
- [cisco-fp-str-app-logout-success-logoutsuccess](CodeChanges/cisco-fp-str-app-logout-success-logoutsuccess.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-fp-str-app-logout-success-logoutsuccess&type=code)
- [cisco-fp-str-app-logout-success-sessionexpired](CodeChanges/cisco-fp-str-app-logout-success-sessionexpired.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-fp-str-app-logout-success-sessionexpired&type=code)
- [cisco-fp-str-policy-modify-success-policies](CodeChanges/cisco-fp-str-policy-modify-success-policies.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-fp-str-policy-modify-success-policies&type=code)
- [darktrace-darktrace-json-alert-trigger-success-alertname](CodeChanges/darktrace-darktrace-json-alert-trigger-success-alertname.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20darktrace-darktrace-json-alert-trigger-success-alertname&type=code)
- [darktrace-darktrace-json-alert-trigger-success-suspiciousproperties](CodeChanges/darktrace-darktrace-json-alert-trigger-success-suspiciousproperties.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20darktrace-darktrace-json-alert-trigger-success-suspiciousproperties&type=code)
- [extrahop-revealx-leef-alert-trigger-success-extrahopdetection](CodeChanges/extrahop-revealx-leef-alert-trigger-success-extrahopdetection.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20extrahop-revealx-leef-alert-trigger-success-extrahopdetection&type=code)
- [microsoft-adfs-kv-app-activity-fail-364](CodeChanges/microsoft-adfs-kv-app-activity-fail-364.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-adfs-kv-app-activity-fail-364&type=code)
- [microsoft-networkwatcher-json-network-traffic-flowlogevent](CodeChanges/microsoft-networkwatcher-json-network-traffic-flowlogevent.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-networkwatcher-json-network-traffic-flowlogevent&type=code)
- [nasuni-n-kv-app-activity](CodeChanges/nasuni-n-kv-app-activity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20nasuni-n-kv-app-activity&type=code)
- [proofpoint-tap-json-app-notification-success-phishingquarantine](CodeChanges/proofpoint-tap-json-app-notification-success-phishingquarantine.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20proofpoint-tap-json-app-notification-success-phishingquarantine&type=code)
- [vmware-vcenter-str-user-password-modify-fail-error](CodeChanges/vmware-vcenter-str-user-password-modify-fail-error.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-vcenter-str-user-password-modify-fail-error&type=code)
- [zeronetworks-zeronetworks-json-app-activity-success-auditlogevent](CodeChanges/zeronetworks-zeronetworks-json-app-activity-success-auditlogevent.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zeronetworks-zeronetworks-json-app-activity-success-auditlogevent&type=code)

#### Changed
<a id="changed"></a>
- [apache-a-str-http-session-apacheaccess](CodeChanges/apache-a-str-http-session-apacheaccess.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20apache-a-str-http-session-apacheaccess&type=code)
- [checkpoint-sg-kv-vpn-authentication-fail-reject](CodeChanges/checkpoint-sg-kv-vpn-authentication-fail-reject.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-sg-kv-vpn-authentication-fail-reject&type=code)
- [checkpoint-sg-kv-vpn-authentication-success-authorize](CodeChanges/checkpoint-sg-kv-vpn-authentication-success-authorize.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-sg-kv-vpn-authentication-success-authorize&type=code)
- [checkpoint-sg-kv-vpn-login-fail-failedlogin](CodeChanges/checkpoint-sg-kv-vpn-login-fail-failedlogin.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-sg-kv-vpn-login-fail-failedlogin&type=code)
- [checkpoint-sg-kv-vpn-login-success-login](CodeChanges/checkpoint-sg-kv-vpn-login-success-login.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-sg-kv-vpn-login-success-login&type=code)
- [checkpoint-sg-kv-vpn-logout-success-logout-2](CodeChanges/checkpoint-sg-kv-vpn-logout-success-logout-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-sg-kv-vpn-logout-success-logout-2&type=code)
- [imperva-securesphere-cef-alert-trigger-success-servergroup](CodeChanges/imperva-securesphere-cef-alert-trigger-success-servergroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20imperva-securesphere-cef-alert-trigger-success-servergroup&type=code)
- [pan-prisma-sk4-alert-trigger-success-prismacloud](CodeChanges/pan-prisma-sk4-alert-trigger-success-prismacloud.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-prisma-sk4-alert-trigger-success-prismacloud&type=code)

#### Changed Parsed Fields
<a id="changed-parsed-fields"></a>
- [abnormalsecurity-as-json-alert-trigger-success-attacktype-1](CodeChanges/abnormalsecurity-as-json-alert-trigger-success-attacktype-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20abnormalsecurity-as-json-alert-trigger-success-attacktype-1&type=code)
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
- [auth0-a-json-endpoint-login-fail-invalidrequest](CodeChanges/auth0-a-json-endpoint-login-fail-invalidrequest.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-endpoint-login-fail-invalidrequest&type=code)
- [auth0-a-json-endpoint-login-success-exchange](CodeChanges/auth0-a-json-endpoint-login-success-exchange.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-endpoint-login-success-exchange&type=code)
- [auth0-a-json-endpoint-login-success-verification](CodeChanges/auth0-a-json-endpoint-login-success-verification.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-endpoint-login-success-verification&type=code)
- [auth0-a-json-http-session-success-mgmt_api_read](CodeChanges/auth0-a-json-http-session-success-mgmt_api_read.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-http-session-success-mgmt_api_read&type=code)
- [auth0-a-json-http-session-success-sapi](CodeChanges/auth0-a-json-http-session-success-sapi.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-http-session-success-sapi&type=code)
- [auth0-a-json-user-delete-success-userdeletion](CodeChanges/auth0-a-json-user-delete-success-userdeletion.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-user-delete-success-userdeletion&type=code)
- [auth0-a-json-user-password-modify-fail-fcp](CodeChanges/auth0-a-json-user-password-modify-fail-fcp.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-user-password-modify-fail-fcp&type=code)
- [auth0-a-json-user-password-modify-success-changepassword](CodeChanges/auth0-a-json-user-password-modify-success-changepassword.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-a-json-user-password-modify-success-changepassword&type=code)
- [crowdstrike-falcon-mix-endpoint-login-success-userlogon](CodeChanges/crowdstrike-falcon-mix-endpoint-login-success-userlogon.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-mix-endpoint-login-success-userlogon&type=code)
- [crowdstrike-falcon-sk4-endpoint-login-userloginfail](CodeChanges/crowdstrike-falcon-sk4-endpoint-login-userloginfail.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-sk4-endpoint-login-userloginfail&type=code)
- [crowdstrike-falcon-sk4-endpoint-notification-timestamp](CodeChanges/crowdstrike-falcon-sk4-endpoint-notification-timestamp.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-sk4-endpoint-notification-timestamp&type=code)
- [microsoft-azurefw-json-dns-request-success-azfwdnsquery](CodeChanges/microsoft-azurefw-json-dns-request-success-azfwdnsquery.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azurefw-json-dns-request-success-azfwdnsquery&type=code)
- [microsoft-azurefw-json-network-session-azfwapplicationrule](CodeChanges/microsoft-azurefw-json-network-session-azfwapplicationrule.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azurefw-json-network-session-azfwapplicationrule&type=code)
- [microsoft-azurefw-json-network-session-azfwidpssignature](CodeChanges/microsoft-azurefw-json-network-session-azfwidpssignature.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azurefw-json-network-session-azfwidpssignature&type=code)
- [microsoft-azurefw-json-network-session-azfwnetworkrule](CodeChanges/microsoft-azurefw-json-network-session-azfwnetworkrule.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azurefw-json-network-session-azfwnetworkrule&type=code)
- [microsoft-defenderep-sk4-dll-load-deviceimageloadevents](CodeChanges/microsoft-defenderep-sk4-dll-load-deviceimageloadevents.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-defenderep-sk4-dll-load-deviceimageloadevents&type=code)
- [microsoft-evnps-xml-radius-traffic-success-6272](CodeChanges/microsoft-evnps-xml-radius-traffic-success-6272.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evnps-xml-radius-traffic-success-6272&type=code)
- [microsoft-evsecurity-cef-ds-object-activity-success-4742](CodeChanges/microsoft-evsecurity-cef-ds-object-activity-success-4742.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-ds-object-activity-success-4742&type=code)
- [microsoft-evsecurity-json-ds-object-modify-success-4742](CodeChanges/microsoft-evsecurity-json-ds-object-modify-success-4742.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-ds-object-modify-success-4742&type=code)
- [microsoft-evsecurity-json-endpoint-activity-auditing](CodeChanges/microsoft-evsecurity-json-endpoint-activity-auditing.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-endpoint-activity-auditing&type=code)
- [microsoft-evsecurity-kv-ds-object-modify-success-4742](CodeChanges/microsoft-evsecurity-kv-ds-object-modify-success-4742.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-ds-object-modify-success-4742&type=code)
- [microsoft-evsecurity-mix-ds-object-modify-success-4742](CodeChanges/microsoft-evsecurity-mix-ds-object-modify-success-4742.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-ds-object-modify-success-4742&type=code)
- [microsoft-evsecurity-xml-configuration-modify-success-4742](CodeChanges/microsoft-evsecurity-xml-configuration-modify-success-4742.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-configuration-modify-success-4742&type=code)
- [microsoft-evsecurity-xml-ds-object-activity-success-4742](CodeChanges/microsoft-evsecurity-xml-ds-object-activity-success-4742.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-ds-object-activity-success-4742&type=code)
- [microsoft-mcas-cef-file-write-success-appidonedrive](CodeChanges/microsoft-mcas-cef-file-write-success-appidonedrive.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-mcas-cef-file-write-success-appidonedrive&type=code)
- [microsoft-nps-xml-radius-traffic-fail-6273](CodeChanges/microsoft-nps-xml-radius-traffic-fail-6273.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-nps-xml-radius-traffic-fail-6273&type=code)
- [microsoft-o365-cef-app-file-success-addtogroup](CodeChanges/microsoft-o365-cef-app-file-success-addtogroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-addtogroup&type=code)
- [okta-amfa-cef-app-login-success-userssosuccess](CodeChanges/okta-amfa-cef-app-login-success-userssosuccess.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20okta-amfa-cef-app-login-success-userssosuccess&type=code)
- [okta-amfa-json-app-login-success-evaluatesignon-1](CodeChanges/okta-amfa-json-app-login-success-evaluatesignon-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20okta-amfa-json-app-login-success-evaluatesignon-1&type=code)
- [okta-amfa-json-app-login-success-oauth2signon](CodeChanges/okta-amfa-json-app-login-success-oauth2signon.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20okta-amfa-json-app-login-success-oauth2signon&type=code)
- [okta-amfa-json-app-login-success-signon](CodeChanges/okta-amfa-json-app-login-success-signon.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20okta-amfa-json-app-login-success-signon&type=code)
- [okta-amfa-json-app-login-success-singlesignon-1](CodeChanges/okta-amfa-json-app-login-success-singlesignon-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20okta-amfa-json-app-login-success-singlesignon-1&type=code)
- [okta-amfa-json-endpoint-login-success-authenticateuser](CodeChanges/okta-amfa-json-endpoint-login-success-authenticateuser.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20okta-amfa-json-endpoint-login-success-authenticateuser&type=code)
- [okta-amfa-json-endpoint-login-success-userlogin](CodeChanges/okta-amfa-json-endpoint-login-success-userlogin.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20okta-amfa-json-endpoint-login-success-userlogin&type=code)
- [pan-ngfw-csv-http-session-9999](CodeChanges/pan-ngfw-csv-http-session-9999.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-http-session-9999&type=code)
- [pan-tesm-csv-alert-trigger-hipmatch](CodeChanges/pan-tesm-csv-alert-trigger-hipmatch.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-tesm-csv-alert-trigger-hipmatch&type=code)
- [salesforce-sf-json-app-login-success-loginurl](CodeChanges/salesforce-sf-json-app-login-success-loginurl.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20salesforce-sf-json-app-login-success-loginurl&type=code)
- [unix-unix-str-endpoint-activity-fail-sshd](CodeChanges/unix-unix-str-endpoint-activity-fail-sshd.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-str-endpoint-activity-fail-sshd&type=code)

#### Edit Attribute
<a id="edit-attribute"></a>
- [azure-azuread-json-app-activity-useractivitydisplayname](CodeChanges/azure-azuread-json-app-activity-useractivitydisplayname.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-app-activity-useractivitydisplayname&type=code)
- [azure-azuread-json-app-activity-useractivitydisplayname-1](CodeChanges/azure-azuread-json-app-activity-useractivitydisplayname-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-azuread-json-app-activity-useractivitydisplayname-1&type=code)
- [microsoft-azure-json-file-success-1](CodeChanges/microsoft-azure-json-file-success-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azure-json-file-success-1&type=code)

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
- [cisco-asa-str-app-notification-success-ssh](CodeChanges/cisco-asa-str-app-notification-success-ssh.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-ssh&type=code)
- [cisco-asa-str-app-notification-success-sys](CodeChanges/cisco-asa-str-app-notification-success-sys.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-app-notification-success-sys&type=code)
- [cisco-asa-str-ssh-close-ssh](CodeChanges/cisco-asa-str-ssh-close-ssh.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-ssh-close-ssh&type=code)
- [cisco-asa-str-ssh-start-session](CodeChanges/cisco-asa-str-ssh-start-session.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-asa-str-ssh-start-session&type=code)
- [cisco-ios-str-endpoint-authentication-fail-authenticationfailed](CodeChanges/cisco-ios-str-endpoint-authentication-fail-authenticationfailed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-ios-str-endpoint-authentication-fail-authenticationfailed&type=code)
- [cisco-ios-str-endpoint-authentication-success-authpassed](CodeChanges/cisco-ios-str-endpoint-authentication-success-authpassed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-ios-str-endpoint-authentication-success-authpassed&type=code)
- [fortinet-fortigate-kv-app-activity-system](CodeChanges/fortinet-fortigate-kv-app-activity-system.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20fortinet-fortigate-kv-app-activity-system&type=code)
- [google-cloudplatform-mix-app-activity-success-prototpayload](CodeChanges/google-cloudplatform-mix-app-activity-success-prototpayload.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20google-cloudplatform-mix-app-activity-success-prototpayload&type=code)
- [microsoft-atp-cef-alert-trigger-success-directoryservicesreplicatio](CodeChanges/microsoft-atp-cef-alert-trigger-success-directoryservicesreplicatio.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-atp-cef-alert-trigger-success-directoryservicesreplicatio&type=code)
- [microsoft-atp-cef-alert-trigger-success-ldapbruteforce](CodeChanges/microsoft-atp-cef-alert-trigger-success-ldapbruteforce.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-atp-cef-alert-trigger-success-ldapbruteforce&type=code)
- [microsoft-atp-cef-alert-trigger-success-ldapsearch](CodeChanges/microsoft-atp-cef-alert-trigger-success-ldapsearch.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-atp-cef-alert-trigger-success-ldapsearch&type=code)
- [microsoft-atp-cef-alert-trigger-success-passtheticket](CodeChanges/microsoft-atp-cef-alert-trigger-success-passtheticket.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-atp-cef-alert-trigger-success-passtheticket&type=code)
- [microsoft-atp-cef-alert-trigger-success-sensitivegroupmembershipchange](CodeChanges/microsoft-atp-cef-alert-trigger-success-sensitivegroupmembershipchange.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-atp-cef-alert-trigger-success-sensitivegroupmembershipchange&type=code)
- [microsoft-atp-cef-alert-trigger-success-sensorcapture](CodeChanges/microsoft-atp-cef-alert-trigger-success-sensorcapture.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-atp-cef-alert-trigger-success-sensorcapture&type=code)
- [microsoft-atp-cef-alert-trigger-success-sensordirectory](CodeChanges/microsoft-atp-cef-alert-trigger-success-sensordirectory.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-atp-cef-alert-trigger-success-sensordirectory&type=code)
- [microsoft-atp-cef-alert-trigger-success-sensorlowmemory](CodeChanges/microsoft-atp-cef-alert-trigger-success-sensorlowmemory.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-atp-cef-alert-trigger-success-sensorlowmemory&type=code)
- [microsoft-atp-cef-alert-trigger-success-sensornetwork](CodeChanges/microsoft-atp-cef-alert-trigger-success-sensornetwork.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-atp-cef-alert-trigger-success-sensornetwork&type=code)
- [microsoft-atp-cef-alert-trigger-success-workspacedirectory](CodeChanges/microsoft-atp-cef-alert-trigger-success-workspacedirectory.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-atp-cef-alert-trigger-success-workspacedirectory&type=code)
- [microsoft-evpowershell-kv-script-execute-success-4104](CodeChanges/microsoft-evpowershell-kv-script-execute-success-4104.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evpowershell-kv-script-execute-success-4104&type=code)
- [microsoft-evsecurity-cef-app-notification-5061](CodeChanges/microsoft-evsecurity-cef-app-notification-5061.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-app-notification-5061&type=code)
- [microsoft-evsecurity-json-service-create-success-4697](CodeChanges/microsoft-evsecurity-json-service-create-success-4697.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-service-create-success-4697&type=code)
- [microsoft-evsecurity-kv-endpoint-login-4768-3](CodeChanges/microsoft-evsecurity-kv-endpoint-login-4768-3.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-4768-3&type=code)
- [microsoft-evsecurity-kv-endpoint-login-4769-2](CodeChanges/microsoft-evsecurity-kv-endpoint-login-4769-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-4769-2&type=code)
- [microsoft-evsecurity-kv-endpoint-login-4769-6](CodeChanges/microsoft-evsecurity-kv-endpoint-login-4769-6.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-4769-6&type=code)
- [microsoft-evsecurity-kv-endpoint-login-fail-4625-2](CodeChanges/microsoft-evsecurity-kv-endpoint-login-fail-4625-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-fail-4625-2&type=code)
- [microsoft-evsecurity-kv-endpoint-login-success-4624-2](CodeChanges/microsoft-evsecurity-kv-endpoint-login-success-4624-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-success-4624-2&type=code)
- [microsoft-evsecurity-kv-endpoint-login-success-4624-3](CodeChanges/microsoft-evsecurity-kv-endpoint-login-success-4624-3.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-endpoint-login-success-4624-3&type=code)
- [microsoft-evsecurity-kv-group-member-add-success-4756-2](CodeChanges/microsoft-evsecurity-kv-group-member-add-success-4756-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-group-member-add-success-4756-2&type=code)
- [microsoft-evsecurity-kv-process-create-success-mswineventlog4688](CodeChanges/microsoft-evsecurity-kv-process-create-success-mswineventlog4688.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-process-create-success-mswineventlog4688&type=code)
- [microsoft-evsecurity-mix-share-access-success-5140](CodeChanges/microsoft-evsecurity-mix-share-access-success-5140.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-share-access-success-5140&type=code)
- [microsoft-evsecurity-mix-share-access-success-5140-1](CodeChanges/microsoft-evsecurity-mix-share-access-success-5140-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-share-access-success-5140-1&type=code)
- [microsoft-evsecurity-mix-share-access-success-5140-2](CodeChanges/microsoft-evsecurity-mix-share-access-success-5140-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-share-access-success-5140-2&type=code)
- [microsoft-evsecurity-xml-group-create-4754](CodeChanges/microsoft-evsecurity-xml-group-create-4754.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-group-create-4754&type=code)
- [microsoft-o365-cef-app-file-success-removememberfromgroup](CodeChanges/microsoft-o365-cef-app-file-success-removememberfromgroup.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-cef-app-file-success-removememberfromgroup&type=code)
- [pan-ngfw-cef-http-session-url](CodeChanges/pan-ngfw-cef-http-session-url.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-cef-http-session-url&type=code)
- [pan-ngfw-csv-alert-trigger-success-data](CodeChanges/pan-ngfw-csv-alert-trigger-success-data.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-alert-trigger-success-data&type=code)
- [pan-ngfw-csv-alert-trigger-success-file](CodeChanges/pan-ngfw-csv-alert-trigger-success-file.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-alert-trigger-success-file&type=code)
- [pan-ngfw-csv-alert-trigger-success-flood](CodeChanges/pan-ngfw-csv-alert-trigger-success-flood.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-alert-trigger-success-flood&type=code)
- [pan-ngfw-csv-alert-trigger-success-scan](CodeChanges/pan-ngfw-csv-alert-trigger-success-scan.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-alert-trigger-success-scan&type=code)
- [pan-ngfw-csv-alert-trigger-success-url](CodeChanges/pan-ngfw-csv-alert-trigger-success-url.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-alert-trigger-success-url&type=code)
- [pan-ngfw-csv-http-session-webbrowsing](CodeChanges/pan-ngfw-csv-http-session-webbrowsing.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-http-session-webbrowsing&type=code)
- [pan-ngfw-csv-network-traffic-fail-drop](CodeChanges/pan-ngfw-csv-network-traffic-fail-drop.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-network-traffic-fail-drop&type=code)
- [pan-ngfw-csv-network-traffic-fail-panorama](CodeChanges/pan-ngfw-csv-network-traffic-fail-panorama.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-network-traffic-fail-panorama&type=code)
- [pan-ngfw-csv-network-traffic-fail-tcp](CodeChanges/pan-ngfw-csv-network-traffic-fail-tcp.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-network-traffic-fail-tcp&type=code)
- [pan-ngfw-csv-network-traffic-packet](CodeChanges/pan-ngfw-csv-network-traffic-packet.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-network-traffic-packet&type=code)
- [pan-ngfw-csv-network-traffic-success-allow](CodeChanges/pan-ngfw-csv-network-traffic-success-allow.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-network-traffic-success-allow&type=code)
- [pan-ngfw-csv-network-traffic-success-connection](CodeChanges/pan-ngfw-csv-network-traffic-success-connection.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-network-traffic-success-connection&type=code)
- [pan-ngfw-csv-network-traffic-success-end](CodeChanges/pan-ngfw-csv-network-traffic-success-end.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-csv-network-traffic-success-end&type=code)
- [pan-ngfw-json-alert-trigger-success-vulnerability](CodeChanges/pan-ngfw-json-alert-trigger-success-vulnerability.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-json-alert-trigger-success-vulnerability&type=code)
- [pan-ngfw-mix-alert-trigger-success-spywarealert](CodeChanges/pan-ngfw-mix-alert-trigger-success-spywarealert.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-mix-alert-trigger-success-spywarealert&type=code)
- [pan-ngfw-mix-alert-trigger-success-threadvulnerability](CodeChanges/pan-ngfw-mix-alert-trigger-success-threadvulnerability.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-mix-alert-trigger-success-threadvulnerability&type=code)
- [pan-ngfw-mix-alert-trigger-success-virus](CodeChanges/pan-ngfw-mix-alert-trigger-success-virus.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-ngfw-mix-alert-trigger-success-virus&type=code)
- [pan-wildfire-csv-alert-trigger-success-threadwildfire](CodeChanges/pan-wildfire-csv-alert-trigger-success-threadwildfire.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-wildfire-csv-alert-trigger-success-threadwildfire&type=code)
- [pan-wildfire-csv-alert-trigger-success-wildfirevirus](CodeChanges/pan-wildfire-csv-alert-trigger-success-wildfirevirus.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-wildfire-csv-alert-trigger-success-wildfirevirus&type=code)
- [servicenow-s-json-http-session-success-transcation](CodeChanges/servicenow-s-json-http-session-success-transcation.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20servicenow-s-json-http-session-success-transcation&type=code)
- [unix-auditd-kv-user-switch-success-userrolechange](CodeChanges/unix-auditd-kv-user-switch-success-userrolechange.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-auditd-kv-user-switch-success-userrolechange&type=code)
- [unix-unix-kv-endpoint-login-sshdauth](CodeChanges/unix-unix-kv-endpoint-login-sshdauth.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-endpoint-login-sshdauth&type=code)
- [unix-unix-kv-endpoint-login-userlogin](CodeChanges/unix-unix-kv-endpoint-login-userlogin.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-endpoint-login-userlogin&type=code)
- [unix-unix-kv-endpoint-login-userstart](CodeChanges/unix-unix-kv-endpoint-login-userstart.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20unix-unix-kv-endpoint-login-userstart&type=code)
- [zscaler-ia-cef-alert-trigger-success-zscalernssweblogdlpdictionaries](CodeChanges/zscaler-ia-cef-alert-trigger-success-zscalernssweblogdlpdictionaries.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zscaler-ia-cef-alert-trigger-success-zscalernssweblogdlpdictionaries&type=code)
- [zscaler-ia-cef-http-session-spriv](CodeChanges/zscaler-ia-cef-http-session-spriv.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20zscaler-ia-cef-http-session-spriv&type=code)

</details>

<details>
<summary><strong id="parsertemplate">ParserTemplate (9)</strong></summary>


### Change Types
- [Added Parser Template](#added-parser-template)
- [Changed Parsed Fields](#changed-parsed-fields)
- [Edit Regex Field](#edit-regex-field)

#### Added Parser Template
<a id="added-parser-template"></a>
- [proofpoint-tap-log](CodeChanges/proofpoint-tap-log.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20proofpoint-tap-log&type=code)

#### Changed Parsed Fields
<a id="changed-parsed-fields"></a>
- [auth0-authentication-template](CodeChanges/auth0-authentication-template.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20auth0-authentication-template&type=code)
- [azure-firewall](CodeChanges/azure-firewall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20azure-firewall&type=code)
- [s-okta-app-login](CodeChanges/s-okta-app-login.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20s-okta-app-login&type=code)

#### Edit Regex Field
<a id="edit-regex-field"></a>
- [aws-cloudtrail-json](CodeChanges/aws-cloudtrail-json.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20aws-cloudtrail-json&type=code)
- [cef-atp-alert](CodeChanges/cef-atp-alert.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cef-atp-alert&type=code)
- [json-aws-guardduty-security-alert-template](CodeChanges/json-aws-guardduty-security-alert-template.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20json-aws-guardduty-security-alert-template&type=code)
- [paloalto-firewall](CodeChanges/paloalto-firewall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20paloalto-firewall&type=code)
- [pan-csv-threat](CodeChanges/pan-csv-threat.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20pan-csv-threat&type=code)

</details>