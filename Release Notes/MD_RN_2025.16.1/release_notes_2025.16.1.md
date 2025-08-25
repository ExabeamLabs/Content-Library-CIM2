# Content Package 2025.16.1

These release notes contain information about content package 2025.16.1, released on 01 Aug 2025.


## Enhancements
- Updated windows and other vendors  parsers to parse out all usernames, including system accounts.
- Added a new parser, microsoft-evsecurity-str-certificate-request-success-4886, to support the newly formatted 4886 Microsoft Event Viewer Security logs
- Added new parser for keeper logs - keepersecurity-keeper-json-app-activity-access-auditevent
- Added support for Imperva DB new format logs.
- Added new parsers thoughtspot-ts-json-app-activity-success-answer, for the ThoughtSpot Logs
- Added new catchall parser for vendor Cimcor Product Cimtrak
- Update Windows XML parsers to support both formats: With single quote ' and with double quotes '
- Updated event builders for windows event id 5136, 5137 and 5141.

## Addressed Issues
- Replaced the http_response_code field with category_id in the  parser fortinet-utm-kv-http-session-webfilter
- Fixed the process related fields parsing issue with microsoft-evpowershell-xml-process-create-success-4103 parser.
- Added time,alert_severity,log_name, region,project_id,category, service_name ,resource_name,operation for parsers -  google-cloudplatform-json-app-database-success-database ,google-cloudplatform-json-scheduled-success-scheduler , google-cloudplatform-json-app-activity-success-catchall_dprocpubsub ,google-cloudplatform-mix-app-activity-success-prototpayload
- Fix the field parsing logic for email_address, user, app, category, and time in the microsoft-m365auditlogs-json-app-activity-operationname parser.
- Updated the region field extractions for parser, amazon-awscloudwatch-cef-network-traffic-success-cloudwatch amazon-awscloudwatch-sk4-app-activity-aws amazon-awscloudtrail-sk4-app-activity-aws
- Updated the account_id and user_type parsing regexes in the AWS GuardDuty parsers, as a slightly different raw log format was observed in a few customer environments.
- Updated condition of parser - microsoft-evsecurity-kv-user-delete-success-4743-1 to capture new format logs of windows event ID 4743.
- Updated src_user, user, db_user field extractions for the Microsoft MsSql parsers.
- cisco-duo-json-endpoint-authentication-result-1 parser has been updated to map the reason field to the result_reason field
- Updated login_id regex for microsoft-evsecurity-xml-user-privilege-assign-success-4672 parser.
- Fix removable_media_vendor and removable_media_serial_number field parsing for the microsoft-o365-sk4-file-app-userkey parser.
- Updated product for barracuda-waf-str-app-notification-samltokenparsed parser.

## Code Changes
### ℹ️ How to Read This Document

Each item listed under **Code Changes** includes:

- **A link to a detailed change file**  
  Click the filename (e.g., `Carbon Black.md`) to open a full table showing what changed.

- **A search icon 🔍**  
  Click the 🔍 icon to search for this resource in the [Exabeam Content Library](https://github.com/ExabeamLabs/Content-Library-CIM2).


<details>
<summary><strong id="event-builder">Event Builder (81)</strong></summary>


### Change Types
- [Added Event Builder](#added-event-builder)
- [Edit Conditions](#edit-conditions)
- [Removed Event Builder](#removed-event-builder)

#### Added Event Builder
<a id="added-event-builder"></a>
- [cimcor-cimtrak-app-activity-fail](CodeChanges/cimcor-cimtrak-app-activity-fail.md)
- [cimcor-cimtrak-app-activity-success](CodeChanges/cimcor-cimtrak-app-activity-success.md)
- [cimcor-cimtrak-app-login-success](CodeChanges/cimcor-cimtrak-app-login-success.md)
- [cimcor-cimtrak-file-delete-success](CodeChanges/cimcor-cimtrak-file-delete-success.md)
- [cimcor-cimtrak-file-write-success](CodeChanges/cimcor-cimtrak-file-write-success.md)
- [cimcor-cimtrak-group-member-add-success](CodeChanges/cimcor-cimtrak-group-member-add-success.md)
- [cimcor-cimtrak-group-member-remove-success](CodeChanges/cimcor-cimtrak-group-member-remove-success.md)
- [dl-cimcor-cimtrak-app-logout-success](CodeChanges/dl-cimcor-cimtrak-app-logout-success.md)
- [dl-cimcor-cimtrak-network-close-success](CodeChanges/dl-cimcor-cimtrak-network-close-success.md)
- [dl-microsoft-ad-configuration-modify-success](CodeChanges/dl-microsoft-ad-configuration-modify-success.md)
- [dl-microsoft-ad-ds-object-delete-success](CodeChanges/dl-microsoft-ad-ds-object-delete-success.md)
- [dl-microsoft-ad-endpoint-create-success-2](CodeChanges/dl-microsoft-ad-endpoint-create-success-2.md)
- [dl-microsoft-ad-endpoint-delete-success-1](CodeChanges/dl-microsoft-ad-endpoint-delete-success-1.md)
- [dl-microsoft-ad-endpoint-modify-success-1](CodeChanges/dl-microsoft-ad-endpoint-modify-success-1.md)
- [dl-microsoft-ad-group-create-success-3](CodeChanges/dl-microsoft-ad-group-create-success-3.md)
- [dl-microsoft-ad-group-delete-success-3](CodeChanges/dl-microsoft-ad-group-delete-success-3.md)
- [dl-microsoft-ad-group-modify-success-4](CodeChanges/dl-microsoft-ad-group-modify-success-4.md)
- [dl-microsoft-ad-user-create-success](CodeChanges/dl-microsoft-ad-user-create-success.md)
- [dl-microsoft-ad-user-delete-success](CodeChanges/dl-microsoft-ad-user-delete-success.md)
- [dl-microsoft-ad-user-modify-success-2](CodeChanges/dl-microsoft-ad-user-modify-success-2.md)
- [dl-monday-monday-app-activity-success](CodeChanges/dl-monday-monday-app-activity-success.md)
- [dl-oracle-public-cloud-app-activity-success](CodeChanges/dl-oracle-public-cloud-app-activity-success.md)
- [dl-servicenow-app-authentication-success](CodeChanges/dl-servicenow-app-authentication-success.md)
- [dl-servicenow-app-logout-success](CodeChanges/dl-servicenow-app-logout-success.md)
- [dl-vmware-airwatch-group-delete-success](CodeChanges/dl-vmware-airwatch-group-delete-success.md)
- [dl-vmware-carbonblackedr-process-close-success](CodeChanges/dl-vmware-carbonblackedr-process-close-success.md)
- [dl-vmware-ciscoasa-endpoint-authentication-success](CodeChanges/dl-vmware-ciscoasa-endpoint-authentication-success.md)
- [dl-vmware-horizon-endpoint-authentication-success](CodeChanges/dl-vmware-horizon-endpoint-authentication-success.md)
- [dl-vmware-macos-process-close-success](CodeChanges/dl-vmware-macos-process-close-success.md)
- [dl-vmware-unix-process-close-success](CodeChanges/dl-vmware-unix-process-close-success.md)
- [dl-vmware-view-app-authentication-fail](CodeChanges/dl-vmware-view-app-authentication-fail.md)
- [dl-vmware-view-app-logout-success](CodeChanges/dl-vmware-view-app-logout-success.md)
- [dl-vmware-view-endpoint-login-success](CodeChanges/dl-vmware-view-endpoint-login-success.md)
- [dl-vmware-view-endpoint-logout-success](CodeChanges/dl-vmware-view-endpoint-logout-success.md)
- [dl-vmware-windows-endpoint-activity-success-1](CodeChanges/dl-vmware-windows-endpoint-activity-success-1.md)
- [dl-vmware-windows-process-close-success](CodeChanges/dl-vmware-windows-process-close-success.md)
- [dl-vmware-windows-process-close-success-1](CodeChanges/dl-vmware-windows-process-close-success-1.md)
- [keepersecurity-keeper-app-activity-success](CodeChanges/keepersecurity-keeper-app-activity-success.md)
- [keepersecurity-keeper-app-login-success](CodeChanges/keepersecurity-keeper-app-login-success.md)
- [microsoft-ad-ds-object-modify-success-3](CodeChanges/microsoft-ad-ds-object-modify-success-3.md)
- [opendj-endpoint-login-fail](CodeChanges/opendj-endpoint-login-fail.md)
- [opendj-endpoint-login-success](CodeChanges/opendj-endpoint-login-success.md)
- [oracle-network-network-traffic-success](CodeChanges/oracle-network-network-traffic-success.md)
- [sentinelone-vigilance-app-activity-success](CodeChanges/sentinelone-vigilance-app-activity-success.md)
- [sigsci-network-http-session-fail](CodeChanges/sigsci-network-http-session-fail.md)
- [sigsci-network-http-session-success](CodeChanges/sigsci-network-http-session-success.md)
- [thoughtspot-ts-app-activity-success](CodeChanges/thoughtspot-ts-app-activity-success.md)
- [visma-megaflex-physical-location-access-fail](CodeChanges/visma-megaflex-physical-location-access-fail.md)
- [visma-megaflex-physical-location-access-success](CodeChanges/visma-megaflex-physical-location-access-success.md)
- [vmware-carbonblackces-file-write-success-1](CodeChanges/vmware-carbonblackces-file-write-success-1.md)
- [vmware-network-network-session-success-1](CodeChanges/vmware-network-network-session-success-1.md)
- [vmware-network-network-session-success-3](CodeChanges/vmware-network-network-session-success-3.md)
- [vmware-vcenter-app-login-success-1](CodeChanges/vmware-vcenter-app-login-success-1.md)
- [vmware-vim-user-privilege-use-success](CodeChanges/vmware-vim-user-privilege-use-success.md)
- [vmware-windows-registry-create-success](CodeChanges/vmware-windows-registry-create-success.md)
- [vmware-windows-registry-modify-success](CodeChanges/vmware-windows-registry-modify-success.md)

#### Edit Conditions
<a id="edit-conditions"></a>
- [imperva-securesphere-alert-trigger-success](CodeChanges/imperva-securesphere-alert-trigger-success.md)
- [microsoft-ad-ds-object-create-success](CodeChanges/microsoft-ad-ds-object-create-success.md)

#### Removed Event Builder
<a id="removed-event-builder"></a>
- [amazon-aws-endpoint-login-success](CodeChanges/amazon-aws-endpoint-login-success.md)
- [amazon-rds-database-query](CodeChanges/amazon-rds-database-query.md)
- [amazon-rds-database-update](CodeChanges/amazon-rds-database-update.md)
- [amd-network-network-session-fail](CodeChanges/amd-network-network-session-fail.md)
- [amd-network-network-session-success](CodeChanges/amd-network-network-session-success.md)
- [anywhere365-app-activity-success](CodeChanges/anywhere365-app-activity-success.md)
- [apache-guacamole-app-login-fail](CodeChanges/apache-guacamole-app-login-fail.md)
- [apache-guacamole-app-login-success](CodeChanges/apache-guacamole-app-login-success.md)
- [apache-network-http-session-fail-1](CodeChanges/apache-network-http-session-fail-1.md)
- [apache-network-http-session-success-1](CodeChanges/apache-network-http-session-success-1.md)
- [appsense-am-alert-trigger-success-1](CodeChanges/appsense-am-alert-trigger-success-1.md)
- [assetview-windows-alert-trigger-success](CodeChanges/assetview-windows-alert-trigger-success.md)
- [bitglass-casb-file-download-success](CodeChanges/bitglass-casb-file-download-success.md)
- [blackberry-cylance-alert-trigger-success](CodeChanges/blackberry-cylance-alert-trigger-success.md)
- [checkpoint-ngfw-app-login-success](CodeChanges/checkpoint-ngfw-app-login-success.md)
- [dl-amazon-aws-user-create-success](CodeChanges/dl-amazon-aws-user-create-success.md)
- [dl-amazon-rds-app-notification-success](CodeChanges/dl-amazon-rds-app-notification-success.md)
- [dl-amd-network-notification-success](CodeChanges/dl-amd-network-notification-success.md)
- [dl-appsense-am-alert-trigger-success-1](CodeChanges/dl-appsense-am-alert-trigger-success-1.md)
- [microsoft-ad-ds-object-create-success-1](CodeChanges/microsoft-ad-ds-object-create-success-1.md)
- [microsoft-ad-ds-object-create-success-3](CodeChanges/microsoft-ad-ds-object-create-success-3.md)
- [microsoft-ad-ds-object-delete-success](CodeChanges/microsoft-ad-ds-object-delete-success.md)
- [sentinelone-network-http-session-success](CodeChanges/sentinelone-network-http-session-success.md)

</details>

<details>
<summary><strong id="parser">Parser (269)</strong></summary>


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
- [google-cloudplatform-json-app-activity-success-catchall_category](CodeChanges/google-cloudplatform-json-app-activity-success-catchall_category.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20google-cloudplatform-json-app-activity-success-catchall_category&type=code)
- [google-cloudplatform-json-scheduled-success-scheduler](CodeChanges/google-cloudplatform-json-scheduled-success-scheduler.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20google-cloudplatform-json-scheduled-success-scheduler&type=code)

#### Added Parser
<a id="added-parser"></a>
- [cimcor-cimtrak-json-app-activity-success-catchall](CodeChanges/cimcor-cimtrak-json-app-activity-success-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cimcor-cimtrak-json-app-activity-success-catchall&type=code)
- [imperva-securesphere-kv-alert-trigger-success-catsecurity](CodeChanges/imperva-securesphere-kv-alert-trigger-success-catsecurity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20imperva-securesphere-kv-alert-trigger-success-catsecurity&type=code)
- [imperva-securesphere-kv-database-query-success-eventcatquery](CodeChanges/imperva-securesphere-kv-database-query-success-eventcatquery.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20imperva-securesphere-kv-database-query-success-eventcatquery&type=code)
- [keepersecurity-keeper-json-app-activity-access-auditevent](CodeChanges/keepersecurity-keeper-json-app-activity-access-auditevent.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20keepersecurity-keeper-json-app-activity-access-auditevent&type=code)
- [microsoft-365defender-sk4-alert-trigger-success-execution](CodeChanges/microsoft-365defender-sk4-alert-trigger-success-execution.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-365defender-sk4-alert-trigger-success-execution&type=code)
- [microsoft-ata-cef-endpoint-notification-gatewaylowmemorymonitoringalert](CodeChanges/microsoft-ata-cef-endpoint-notification-gatewaylowmemorymonitoringalert.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-ata-cef-endpoint-notification-gatewaylowmemorymonitoringalert&type=code)
- [microsoft-ata-kv-alert-trigger-success-abnormalbehaviorsuspiciousactivity](CodeChanges/microsoft-ata-kv-alert-trigger-success-abnormalbehaviorsuspiciousactivity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-ata-kv-alert-trigger-success-abnormalbehaviorsuspiciousactivity&type=code)
- [microsoft-ata-kv-alert-trigger-success-dnsreconnaissancesuspiciousactivity](CodeChanges/microsoft-ata-kv-alert-trigger-success-dnsreconnaissancesuspiciousactivity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-ata-kv-alert-trigger-success-dnsreconnaissancesuspiciousactivity&type=code)
- [microsoft-ata-kv-alert-trigger-success-samrreconnaissancesuspiciousactivity](CodeChanges/microsoft-ata-kv-alert-trigger-success-samrreconnaissancesuspiciousactivity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-ata-kv-alert-trigger-success-samrreconnaissancesuspiciousactivity&type=code)
- [microsoft-atp-cef-alert-trigger-success-ldapbruteforce](CodeChanges/microsoft-atp-cef-alert-trigger-success-ldapbruteforce.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-atp-cef-alert-trigger-success-ldapbruteforce&type=code)
- [microsoft-evsecurity-str-certificate-request-success-4886](CodeChanges/microsoft-evsecurity-str-certificate-request-success-4886.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-str-certificate-request-success-4886&type=code)
- [monday-mon-json-app-activity-catchall](CodeChanges/monday-mon-json-app-activity-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20monday-mon-json-app-activity-catchall&type=code)
- [openai-oai-json-app-activity-success-apikey](CodeChanges/openai-oai-json-app-activity-success-apikey.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20openai-oai-json-app-activity-success-apikey&type=code)
- [opendj-o-kv-endpoint-login-connectconn](CodeChanges/opendj-o-kv-endpoint-login-connectconn.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20opendj-o-kv-endpoint-login-connectconn&type=code)
- [opendj-o-kv-endpoint-login-msgid](CodeChanges/opendj-o-kv-endpoint-login-msgid.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20opendj-o-kv-endpoint-login-msgid&type=code)
- [opendj-o-kv-endpoint-login-uid](CodeChanges/opendj-o-kv-endpoint-login-uid.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20opendj-o-kv-endpoint-login-uid&type=code)
- [oracle-pc-sk4-app-activity-success-oracle](CodeChanges/oracle-pc-sk4-app-activity-success-oracle.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20oracle-pc-sk4-app-activity-success-oracle&type=code)
- [oracle-pc-sk4-network-traffic-success-dataevent](CodeChanges/oracle-pc-sk4-network-traffic-success-dataevent.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20oracle-pc-sk4-network-traffic-success-dataevent&type=code)
- [sentinelone-v-cef-app-activity-success-usercreatedrole](CodeChanges/sentinelone-v-cef-app-activity-success-usercreatedrole.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-v-cef-app-activity-success-usercreatedrole&type=code)
- [sentinelone-v-cef-app-activity-success-usermodified](CodeChanges/sentinelone-v-cef-app-activity-success-usermodified.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-v-cef-app-activity-success-usermodified&type=code)
- [servicenow-s-sk4-app-authentication-success-externalauthenticationsucceeded](CodeChanges/servicenow-s-sk4-app-authentication-success-externalauthenticationsucceeded.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20servicenow-s-sk4-app-authentication-success-externalauthenticationsucceeded&type=code)
- [servicenow-s-sk4-app-authentication-success-sessionestablished](CodeChanges/servicenow-s-sk4-app-authentication-success-sessionestablished.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20servicenow-s-sk4-app-authentication-success-sessionestablished&type=code)
- [servicenow-s-sk4-app-logout-success-impersonationend](CodeChanges/servicenow-s-sk4-app-logout-success-impersonationend.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20servicenow-s-sk4-app-logout-success-impersonationend&type=code)
- [servicenow-s-sk4-app-logout-success-logout](CodeChanges/servicenow-s-sk4-app-logout-success-logout.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20servicenow-s-sk4-app-logout-success-logout&type=code)
- [sigsci-sigsci-json-http-session-uri](CodeChanges/sigsci-sigsci-json-http-session-uri.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sigsci-sigsci-json-http-session-uri&type=code)
- [thoughtspot-ts-json-app-activity-success-answer](CodeChanges/thoughtspot-ts-json-app-activity-success-answer.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20thoughtspot-ts-json-app-activity-success-answer&type=code)
- [visma-megaflex-json-physical-location-access-accesspoint](CodeChanges/visma-megaflex-json-physical-location-access-accesspoint.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20visma-megaflex-json-physical-location-access-accesspoint&type=code)
- [vmware-airwatch-kv-group-delete-success-groupdeleted](CodeChanges/vmware-airwatch-kv-group-delete-success-groupdeleted.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-airwatch-kv-group-delete-success-groupdeleted&type=code)
- [vmware-carbonblack-json-alert-trigger-success-watchlist-1](CodeChanges/vmware-carbonblack-json-alert-trigger-success-watchlist-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-carbonblack-json-alert-trigger-success-watchlist-1&type=code)
- [vmware-carbonblack-sk4-alert-trigger-success-cbanalytics](CodeChanges/vmware-carbonblack-sk4-alert-trigger-success-cbanalytics.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-carbonblack-sk4-alert-trigger-success-cbanalytics&type=code)
- [vmware-carbonblackappctrl-json-process-close-success-deviceexternalip](CodeChanges/vmware-carbonblackappctrl-json-process-close-success-deviceexternalip.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-carbonblackappctrl-json-process-close-success-deviceexternalip&type=code)
- [vmware-carbonblackceedr-json-process-create-success-fileless](CodeChanges/vmware-carbonblackceedr-json-process-create-success-fileless.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-carbonblackceedr-json-process-create-success-fileless&type=code)
- [vmware-carbonblackceedr-sk4-network-session-success-edr](CodeChanges/vmware-carbonblackceedr-sk4-network-session-success-edr.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-carbonblackceedr-sk4-network-session-success-edr&type=code)
- [vmware-carbonblackceedr-sk4-process-create-success-crossproc](CodeChanges/vmware-carbonblackceedr-sk4-process-create-success-crossproc.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-carbonblackceedr-sk4-process-create-success-crossproc&type=code)
- [vmware-carbonblackedr-cef-file-write-success-edr](CodeChanges/vmware-carbonblackedr-cef-file-write-success-edr.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-carbonblackedr-cef-file-write-success-edr&type=code)
- [vmware-carbonblackedr-cef-network-session-success-netconn](CodeChanges/vmware-carbonblackedr-cef-network-session-success-netconn.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-carbonblackedr-cef-network-session-success-netconn&type=code)
- [vmware-carbonblackedr-cef-process-create-success-childproc](CodeChanges/vmware-carbonblackedr-cef-process-create-success-childproc.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-carbonblackedr-cef-process-create-success-childproc&type=code)
- [vmware-carbonblackedr-json-dll-load-success-edr](CodeChanges/vmware-carbonblackedr-json-dll-load-success-edr.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-carbonblackedr-json-dll-load-success-edr&type=code)
- [vmware-carbonblackedr-json-endpoint-activity-success-epapicall](CodeChanges/vmware-carbonblackedr-json-endpoint-activity-success-epapicall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-carbonblackedr-json-endpoint-activity-success-epapicall&type=code)
- [vmware-carbonblackedr-sk4-process-close-success-endpointeventprocend](CodeChanges/vmware-carbonblackedr-sk4-process-close-success-endpointeventprocend.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-carbonblackedr-sk4-process-close-success-endpointeventprocend&type=code)
- [vmware-carbonblackedr-sk4-registry-registryoperation](CodeChanges/vmware-carbonblackedr-sk4-registry-registryoperation.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-carbonblackedr-sk4-registry-registryoperation&type=code)
- [vmware-esxi-kv-app-logout-success-loggedout](CodeChanges/vmware-esxi-kv-app-logout-success-loggedout.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-esxi-kv-app-logout-success-loggedout&type=code)
- [vmware-esxi-str-app-notification-success-fil3invalid](CodeChanges/vmware-esxi-str-app-notification-success-fil3invalid.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-esxi-str-app-notification-success-fil3invalid&type=code)
- [vmware-horizon-str-endpoint-authentication-success-allocated](CodeChanges/vmware-horizon-str-endpoint-authentication-success-allocated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-horizon-str-endpoint-authentication-success-allocated&type=code)
- [vmware-horizon-str-endpoint-authentication-success-requestedpool](CodeChanges/vmware-horizon-str-endpoint-authentication-success-requestedpool.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-horizon-str-endpoint-authentication-success-requestedpool&type=code)
- [vmware-idm-json-user-privilege-use-success-vidm](CodeChanges/vmware-idm-json-user-privilege-use-success-vidm.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-idm-json-user-privilege-use-success-vidm&type=code)
- [vmware-vcenter-json-app-login-success-loggedin](CodeChanges/vmware-vcenter-json-app-login-success-loggedin.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-vcenter-json-app-login-success-loggedin&type=code)
- [vmware-view-str-app-authentication-fail-denied](CodeChanges/vmware-view-str-app-authentication-fail-denied.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-view-str-app-authentication-fail-denied&type=code)
- [vmware-view-str-app-logout-success-loggedoff](CodeChanges/vmware-view-str-app-logout-success-loggedoff.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-view-str-app-logout-success-loggedoff&type=code)
- [vmware-view-str-app-logout-success-loggedout](CodeChanges/vmware-view-str-app-logout-success-loggedout.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-view-str-app-logout-success-loggedout&type=code)
- [vmware-view-str-endpoint-login-success-reconnected](CodeChanges/vmware-view-str-endpoint-login-success-reconnected.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-view-str-endpoint-login-success-reconnected&type=code)
- [vmware-view-str-endpoint-logout-success-disconnected](CodeChanges/vmware-view-str-endpoint-logout-success-disconnected.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20vmware-view-str-endpoint-logout-success-disconnected&type=code)

#### Changed
<a id="changed"></a>
- [microsoft-evsecurity-kv-user-delete-success-4743-1](CodeChanges/microsoft-evsecurity-kv-user-delete-success-4743-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-user-delete-success-4743-1&type=code)
- [microsoft-evsecurity-xml-group-create-4744](CodeChanges/microsoft-evsecurity-xml-group-create-4744.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-group-create-4744&type=code)
- [microsoft-evsystem-xml-network-session-fail-10028-1](CodeChanges/microsoft-evsystem-xml-network-session-fail-10028-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-xml-network-session-fail-10028-1&type=code)
- [microsoft-sysmon-xml-process-pipe-create-17](CodeChanges/microsoft-sysmon-xml-process-pipe-create-17.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-sysmon-xml-process-pipe-create-17&type=code)
- [netskope-sc-str-http-session-websocket](CodeChanges/netskope-sc-str-http-session-websocket.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20netskope-sc-str-http-session-websocket&type=code)
- [openai-oai-json-app-activity-success-projectcreated](CodeChanges/openai-oai-json-app-activity-success-projectcreated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20openai-oai-json-app-activity-success-projectcreated&type=code)
- [openai-oai-json-app-login-success-loginsucceeded](CodeChanges/openai-oai-json-app-login-success-loginsucceeded.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20openai-oai-json-app-login-success-loginsucceeded&type=code)
- [openai-oai-json-configuration-modify-success-organizationupdated](CodeChanges/openai-oai-json-configuration-modify-success-organizationupdated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20openai-oai-json-configuration-modify-success-organizationupdated&type=code)

#### Changed Parsed Fields
<a id="changed-parsed-fields"></a>
- [amazon-awscloudtrail-sk4-app-activity-aws](CodeChanges/amazon-awscloudtrail-sk4-app-activity-aws.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-sk4-app-activity-aws&type=code)
- [amazon-awscloudtrail-sk4-app-activity-success-redshift](CodeChanges/amazon-awscloudtrail-sk4-app-activity-success-redshift.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-sk4-app-activity-success-redshift&type=code)
- [amazon-awscloudwatch-cef-network-traffic-success-cloudwatch](CodeChanges/amazon-awscloudwatch-cef-network-traffic-success-cloudwatch.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudwatch-cef-network-traffic-success-cloudwatch&type=code)
- [amazon-awscloudwatch-sk4-app-activity-aws](CodeChanges/amazon-awscloudwatch-sk4-app-activity-aws.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudwatch-sk4-app-activity-aws&type=code)
- [cisco-duo-json-endpoint-authentication-result-1](CodeChanges/cisco-duo-json-endpoint-authentication-result-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20cisco-duo-json-endpoint-authentication-result-1&type=code)
- [fortinet-utm-kv-http-session-webfilter](CodeChanges/fortinet-utm-kv-http-session-webfilter.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20fortinet-utm-kv-http-session-webfilter&type=code)
- [google-cloudplatform-json-app-database-success-database](CodeChanges/google-cloudplatform-json-app-database-success-database.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20google-cloudplatform-json-app-database-success-database&type=code)
- [microsoft-azuread-cef-app-login-clientappused](CodeChanges/microsoft-azuread-cef-app-login-clientappused.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-azuread-cef-app-login-clientappused&type=code)
- [microsoft-evsecurity-xml-endpoint-login-fail-4625](CodeChanges/microsoft-evsecurity-xml-endpoint-login-fail-4625.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-login-fail-4625&type=code)
- [microsoft-evsecurity-xml-endpoint-login-success-4624](CodeChanges/microsoft-evsecurity-xml-endpoint-login-success-4624.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-login-success-4624&type=code)
- [microsoft-m365auditlogs-json-app-activity-operationname](CodeChanges/microsoft-m365auditlogs-json-app-activity-operationname.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-m365auditlogs-json-app-activity-operationname&type=code)
- [microsoft-mssql-kv-database-login-fail-33205](CodeChanges/microsoft-mssql-kv-database-login-fail-33205.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-mssql-kv-database-login-fail-33205&type=code)
- [microsoft-mssql-kv-database-login-success-33205](CodeChanges/microsoft-mssql-kv-database-login-success-33205.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-mssql-kv-database-login-success-33205&type=code)
- [microsoft-mssql-kv-database-query-success-33205](CodeChanges/microsoft-mssql-kv-database-query-success-33205.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-mssql-kv-database-query-success-33205&type=code)
- [microsoft-mssql-kv-database-query-success-33205-1](CodeChanges/microsoft-mssql-kv-database-query-success-33205-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-mssql-kv-database-query-success-33205-1&type=code)
- [microsoft-mssql-kv-database-query-success-33205-2](CodeChanges/microsoft-mssql-kv-database-query-success-33205-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-mssql-kv-database-query-success-33205-2&type=code)
- [microsoft-mssql-xml-database-query-success-30205-2](CodeChanges/microsoft-mssql-xml-database-query-success-30205-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-mssql-xml-database-query-success-30205-2&type=code)
- [microsoft-mssql-xml-database-query-success-33205](CodeChanges/microsoft-mssql-xml-database-query-success-33205.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-mssql-xml-database-query-success-33205&type=code)
- [microsoft-mssql-xml-database-query-success-33205-1](CodeChanges/microsoft-mssql-xml-database-query-success-33205-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-mssql-xml-database-query-success-33205-1&type=code)

#### Edit Attribute
<a id="edit-attribute"></a>
- [barracuda-waf-str-app-notification-samltokenparsed](CodeChanges/barracuda-waf-str-app-notification-samltokenparsed.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20barracuda-waf-str-app-notification-samltokenparsed&type=code)
- [microsoft-evsecurity-cef-ds-object-create-success-5137](CodeChanges/microsoft-evsecurity-cef-ds-object-create-success-5137.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-ds-object-create-success-5137&type=code)
- [microsoft-evsecurity-cef-ds-object-create-success-5137-1](CodeChanges/microsoft-evsecurity-cef-ds-object-create-success-5137-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-ds-object-create-success-5137-1&type=code)
- [microsoft-evsecurity-cef-ds-object-delete-success-5141](CodeChanges/microsoft-evsecurity-cef-ds-object-delete-success-5141.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-ds-object-delete-success-5141&type=code)
- [microsoft-evsecurity-cef-ds-object-delete-success-5141-1](CodeChanges/microsoft-evsecurity-cef-ds-object-delete-success-5141-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-ds-object-delete-success-5141-1&type=code)
- [microsoft-evsecurity-cef-ds-object-modify-success-5136](CodeChanges/microsoft-evsecurity-cef-ds-object-modify-success-5136.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-ds-object-modify-success-5136&type=code)
- [microsoft-evsecurity-json-ds-object-delete-success-5141-1](CodeChanges/microsoft-evsecurity-json-ds-object-delete-success-5141-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-ds-object-delete-success-5141-1&type=code)
- [microsoft-evsecurity-json-ds-object-modify-success-5136](CodeChanges/microsoft-evsecurity-json-ds-object-modify-success-5136.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-ds-object-modify-success-5136&type=code)
- [microsoft-evsecurity-json-ds-object-modify-success-5136-1](CodeChanges/microsoft-evsecurity-json-ds-object-modify-success-5136-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-ds-object-modify-success-5136-1&type=code)
- [microsoft-evsecurity-json-ds-object-modify-success-5137](CodeChanges/microsoft-evsecurity-json-ds-object-modify-success-5137.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-ds-object-modify-success-5137&type=code)
- [microsoft-evsecurity-json-ds-object-modify-success-5141](CodeChanges/microsoft-evsecurity-json-ds-object-modify-success-5141.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-json-ds-object-modify-success-5141&type=code)
- [microsoft-evsecurity-kv-ds-object-activity-success-5136](CodeChanges/microsoft-evsecurity-kv-ds-object-activity-success-5136.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-ds-object-activity-success-5136&type=code)
- [microsoft-evsecurity-kv-ds-object-activity-success-5137](CodeChanges/microsoft-evsecurity-kv-ds-object-activity-success-5137.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-ds-object-activity-success-5137&type=code)
- [microsoft-evsecurity-kv-ds-object-activity-success-5137-1](CodeChanges/microsoft-evsecurity-kv-ds-object-activity-success-5137-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-ds-object-activity-success-5137-1&type=code)
- [microsoft-evsecurity-kv-ds-object-activity-success-5141](CodeChanges/microsoft-evsecurity-kv-ds-object-activity-success-5141.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-ds-object-activity-success-5141&type=code)
- [microsoft-evsecurity-kv-ds-object-activity-success-5141-1](CodeChanges/microsoft-evsecurity-kv-ds-object-activity-success-5141-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-ds-object-activity-success-5141-1&type=code)
- [microsoft-evsecurity-kv-ds-object-activity-success-5141-2](CodeChanges/microsoft-evsecurity-kv-ds-object-activity-success-5141-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-ds-object-activity-success-5141-2&type=code)
- [microsoft-evsecurity-kv-ds-object-create-success-5137](CodeChanges/microsoft-evsecurity-kv-ds-object-create-success-5137.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-ds-object-create-success-5137&type=code)
- [microsoft-evsecurity-kv-ds-object-create-success-5137-1](CodeChanges/microsoft-evsecurity-kv-ds-object-create-success-5137-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-ds-object-create-success-5137-1&type=code)
- [microsoft-evsecurity-kv-ds-object-delete-success-5141](CodeChanges/microsoft-evsecurity-kv-ds-object-delete-success-5141.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-ds-object-delete-success-5141&type=code)
- [microsoft-evsecurity-kv-ds-object-delete-success-5141-1](CodeChanges/microsoft-evsecurity-kv-ds-object-delete-success-5141-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-ds-object-delete-success-5141-1&type=code)
- [microsoft-evsecurity-kv-ds-object-modify-success-5136](CodeChanges/microsoft-evsecurity-kv-ds-object-modify-success-5136.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-ds-object-modify-success-5136&type=code)
- [microsoft-evsecurity-kv-ds-object-modify-success-5136-1](CodeChanges/microsoft-evsecurity-kv-ds-object-modify-success-5136-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-ds-object-modify-success-5136-1&type=code)
- [microsoft-evsecurity-mix-ds-object-modify-success-5136](CodeChanges/microsoft-evsecurity-mix-ds-object-modify-success-5136.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-ds-object-modify-success-5136&type=code)
- [microsoft-evsecurity-mix-ds-object-modify-success-5136-1](CodeChanges/microsoft-evsecurity-mix-ds-object-modify-success-5136-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-ds-object-modify-success-5136-1&type=code)
- [microsoft-evsecurity-sk4-ds-object-create-success-5137](CodeChanges/microsoft-evsecurity-sk4-ds-object-create-success-5137.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-sk4-ds-object-create-success-5137&type=code)
- [microsoft-evsecurity-sk4-ds-object-modify-success-5136](CodeChanges/microsoft-evsecurity-sk4-ds-object-modify-success-5136.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-sk4-ds-object-modify-success-5136&type=code)
- [microsoft-evsecurity-xml-ds-object-create-success-5137](CodeChanges/microsoft-evsecurity-xml-ds-object-create-success-5137.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-ds-object-create-success-5137&type=code)
- [microsoft-evsecurity-xml-ds-object-delete-success-5141](CodeChanges/microsoft-evsecurity-xml-ds-object-delete-success-5141.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-ds-object-delete-success-5141&type=code)
- [microsoft-evsecurity-xml-ds-object-delete-success-5141-1](CodeChanges/microsoft-evsecurity-xml-ds-object-delete-success-5141-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-ds-object-delete-success-5141-1&type=code)
- [microsoft-evsecurity-xml-ds-object-modify-success-5136](CodeChanges/microsoft-evsecurity-xml-ds-object-modify-success-5136.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-ds-object-modify-success-5136&type=code)

#### Edit Regex Field
<a id="edit-regex-field"></a>
- [amazon-awscloudtrail-cef-app-activity-awsapicall](CodeChanges/amazon-awscloudtrail-cef-app-activity-awsapicall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-cef-app-activity-awsapicall&type=code)
- [amazon-awscloudtrail-json-app-login-awsconsolesignin](CodeChanges/amazon-awscloudtrail-json-app-login-awsconsolesignin.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-app-login-awsconsolesignin&type=code)
- [amazon-awscloudtrail-json-role-assume-success-assumerole](CodeChanges/amazon-awscloudtrail-json-role-assume-success-assumerole.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-role-assume-success-assumerole&type=code)
- [crowdstrike-falcon-cef-alert-trigger-success-host](CodeChanges/crowdstrike-falcon-cef-alert-trigger-success-host.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20crowdstrike-falcon-cef-alert-trigger-success-host&type=code)
- [microsoft-evadfs-xml-network-notification-49152](CodeChanges/microsoft-evadfs-xml-network-notification-49152.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evadfs-xml-network-notification-49152&type=code)
- [microsoft-evadws-xml-endpoint-notification-success-catchall](CodeChanges/microsoft-evadws-xml-endpoint-notification-success-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evadws-xml-endpoint-notification-success-catchall&type=code)
- [microsoft-evapp-xml-app-activity-success-5973](CodeChanges/microsoft-evapp-xml-app-activity-success-5973.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-app-activity-success-5973&type=code)
- [microsoft-evapp-xml-certificate-request-fail-33370](CodeChanges/microsoft-evapp-xml-certificate-request-fail-33370.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-certificate-request-fail-33370&type=code)
- [microsoft-evapp-xml-certificate-request-fail-49754](CodeChanges/microsoft-evapp-xml-certificate-request-fail-49754.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-certificate-request-fail-49754&type=code)
- [microsoft-evapp-xml-endpoint-notification-10](CodeChanges/microsoft-evapp-xml-endpoint-notification-10.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-endpoint-notification-10&type=code)
- [microsoft-evapp-xml-endpoint-notification-1530](CodeChanges/microsoft-evapp-xml-endpoint-notification-1530.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-endpoint-notification-1530&type=code)
- [microsoft-evapp-xml-endpoint-notification-1534](CodeChanges/microsoft-evapp-xml-endpoint-notification-1534.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-endpoint-notification-1534&type=code)
- [microsoft-evapp-xml-endpoint-notification-3013](CodeChanges/microsoft-evapp-xml-endpoint-notification-3013.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-endpoint-notification-3013&type=code)
- [microsoft-evapp-xml-endpoint-notification-6398](CodeChanges/microsoft-evapp-xml-endpoint-notification-6398.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-endpoint-notification-6398&type=code)
- [microsoft-evapp-xml-network-notification-49152](CodeChanges/microsoft-evapp-xml-network-notification-49152.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-network-notification-49152&type=code)
- [microsoft-evapp-xml-process-close-5612](CodeChanges/microsoft-evapp-xml-process-close-5612.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evapp-xml-process-close-5612&type=code)
- [microsoft-evbferf-xml-network-notification-success-2003](CodeChanges/microsoft-evbferf-xml-network-notification-success-2003.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evbferf-xml-network-notification-success-2003&type=code)
- [microsoft-evcertsc-xml-certificate-expire-64](CodeChanges/microsoft-evcertsc-xml-certificate-expire-64.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evcertsc-xml-certificate-expire-64&type=code)
- [microsoft-evdfsrep-xml-network-notification-49152](CodeChanges/microsoft-evdfsrep-xml-network-notification-49152.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evdfsrep-xml-network-notification-49152&type=code)
- [microsoft-evdirservice-xml-network-notification-49152](CodeChanges/microsoft-evdirservice-xml-network-notification-49152.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evdirservice-xml-network-notification-49152&type=code)
- [microsoft-evdnsserver-xml-dns-traffic-success-5504](CodeChanges/microsoft-evdnsserver-xml-dns-traffic-success-5504.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evdnsserver-xml-dns-traffic-success-5504&type=code)
- [microsoft-evdnsserver-xml-dns_record-modify-fail-4011](CodeChanges/microsoft-evdnsserver-xml-dns_record-modify-fail-4011.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evdnsserver-xml-dns_record-modify-fail-4011&type=code)
- [microsoft-evntlm-xml-endpoint-login-success-8001](CodeChanges/microsoft-evntlm-xml-endpoint-login-success-8001.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evntlm-xml-endpoint-login-success-8001&type=code)
- [microsoft-evntlm-xml-endpoint-login-success-8002](CodeChanges/microsoft-evntlm-xml-endpoint-login-success-8002.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evntlm-xml-endpoint-login-success-8002&type=code)
- [microsoft-evntlm-xml-endpoint-login-success-8003](CodeChanges/microsoft-evntlm-xml-endpoint-login-success-8003.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evntlm-xml-endpoint-login-success-8003&type=code)
- [microsoft-evossh-xml-ssh-traffic-openssh](CodeChanges/microsoft-evossh-xml-ssh-traffic-openssh.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evossh-xml-ssh-traffic-openssh&type=code)
- [microsoft-evpowershell-xml-process-create-success-4103](CodeChanges/microsoft-evpowershell-xml-process-create-success-4103.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evpowershell-xml-process-create-success-4103&type=code)
- [microsoft-evpowershell-xml-script-execute-fail-4100](CodeChanges/microsoft-evpowershell-xml-script-execute-fail-4100.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evpowershell-xml-script-execute-fail-4100&type=code)
- [microsoft-evsecurity-cef-endpoint-login-success-4624-1](CodeChanges/microsoft-evsecurity-cef-endpoint-login-success-4624-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-endpoint-login-success-4624-1&type=code)
- [microsoft-evsecurity-cef-endpoint-logout-4634](CodeChanges/microsoft-evsecurity-cef-endpoint-logout-4634.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-cef-endpoint-logout-4634&type=code)
- [microsoft-evsecurity-kv-group-member-add-success-4756-2](CodeChanges/microsoft-evsecurity-kv-group-member-add-success-4756-2.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-kv-group-member-add-success-4756-2&type=code)
- [microsoft-evsecurity-mix-handle-close-4658](CodeChanges/microsoft-evsecurity-mix-handle-close-4658.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-mix-handle-close-4658&type=code)
- [microsoft-evsecurity-xml-app-activity-success](CodeChanges/microsoft-evsecurity-xml-app-activity-success.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-app-activity-success&type=code)
- [microsoft-evsecurity-xml-app-notification-success-5056](CodeChanges/microsoft-evsecurity-xml-app-notification-success-5056.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-app-notification-success-5056&type=code)
- [microsoft-evsecurity-xml-audit-policy-modify-success-4714](CodeChanges/microsoft-evsecurity-xml-audit-policy-modify-success-4714.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-audit-policy-modify-success-4714&type=code)
- [microsoft-evsecurity-xml-audit-policy-modify-success-5448](CodeChanges/microsoft-evsecurity-xml-audit-policy-modify-success-5448.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-audit-policy-modify-success-5448&type=code)
- [microsoft-evsecurity-xml-audit-policy-modify-success-5449](CodeChanges/microsoft-evsecurity-xml-audit-policy-modify-success-5449.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-audit-policy-modify-success-5449&type=code)
- [microsoft-evsecurity-xml-audit-policy-modify-success-5450](CodeChanges/microsoft-evsecurity-xml-audit-policy-modify-success-5450.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-audit-policy-modify-success-5450&type=code)
- [microsoft-evsecurity-xml-certificate-modify-success-5126](CodeChanges/microsoft-evsecurity-xml-certificate-modify-success-5126.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-certificate-modify-success-5126&type=code)
- [microsoft-evsecurity-xml-configuration-modify-success-4716](CodeChanges/microsoft-evsecurity-xml-configuration-modify-success-4716.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-configuration-modify-success-4716&type=code)
- [microsoft-evsecurity-xml-configuration-modify-success-4950](CodeChanges/microsoft-evsecurity-xml-configuration-modify-success-4950.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-configuration-modify-success-4950&type=code)
- [microsoft-evsecurity-xml-dns-record-create-fail-8015](CodeChanges/microsoft-evsecurity-xml-dns-record-create-fail-8015.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-dns-record-create-fail-8015&type=code)
- [microsoft-evsecurity-xml-dns-record-create-fail-8019](CodeChanges/microsoft-evsecurity-xml-dns-record-create-fail-8019.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-dns-record-create-fail-8019&type=code)
- [microsoft-evsecurity-xml-endpoint-authentication-6278](CodeChanges/microsoft-evsecurity-xml-endpoint-authentication-6278.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-authentication-6278&type=code)
- [microsoft-evsecurity-xml-endpoint-authentication-success-3000](CodeChanges/microsoft-evsecurity-xml-endpoint-authentication-success-3000.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-authentication-success-3000&type=code)
- [microsoft-evsecurity-xml-endpoint-domain-join-fail-16998](CodeChanges/microsoft-evsecurity-xml-endpoint-domain-join-fail-16998.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-domain-join-fail-16998&type=code)
- [microsoft-evsecurity-xml-endpoint-login-fail-1310](CodeChanges/microsoft-evsecurity-xml-endpoint-login-fail-1310.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-login-fail-1310&type=code)
- [microsoft-evsecurity-xml-endpoint-login-fail-16977](CodeChanges/microsoft-evsecurity-xml-endpoint-login-fail-16977.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-login-fail-16977&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-1101](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-1101.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-1101&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-4902-1](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-4902-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-4902-1&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-5033-1](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-5033-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-5033-1&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-success-30909](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-success-30909.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-success-30909&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-success-4802](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-success-4802.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-success-4802&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-success-4872](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-success-4872.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-success-4872&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-success-4876](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-success-4876.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-success-4876&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-success-4877](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-success-4877.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-success-4877&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-success-4944](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-success-4944.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-success-4944&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-success-4945](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-success-4945.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-success-4945&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-success-4953](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-success-4953.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-success-4953&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-success-4956](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-success-4956.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-success-4956&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-success-5440](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-success-5440.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-success-5440&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-success-5441](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-success-5441.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-success-5441&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-success-5442](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-success-5442.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-success-5442&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-success-5444](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-success-5444.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-success-5444&type=code)
- [microsoft-evsecurity-xml-endpoint-notification-success-5446](CodeChanges/microsoft-evsecurity-xml-endpoint-notification-success-5446.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-endpoint-notification-success-5446&type=code)
- [microsoft-evsecurity-xml-file-5058](CodeChanges/microsoft-evsecurity-xml-file-5058.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-file-5058&type=code)
- [microsoft-evsecurity-xml-file-permission-modify-4670-1](CodeChanges/microsoft-evsecurity-xml-file-permission-modify-4670-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-file-permission-modify-4670-1&type=code)
- [microsoft-evsecurity-xml-group-create-success-4759](CodeChanges/microsoft-evsecurity-xml-group-create-success-4759.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-group-create-success-4759&type=code)
- [microsoft-evsecurity-xml-group-create-success-4759-1](CodeChanges/microsoft-evsecurity-xml-group-create-success-4759-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-group-create-success-4759-1&type=code)
- [microsoft-evsecurity-xml-group-list-4798](CodeChanges/microsoft-evsecurity-xml-group-list-4798.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-group-list-4798&type=code)
- [microsoft-evsecurity-xml-group-member-add-4761](CodeChanges/microsoft-evsecurity-xml-group-member-add-4761.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-group-member-add-4761&type=code)
- [microsoft-evsecurity-xml-group-member-add-4761-1](CodeChanges/microsoft-evsecurity-xml-group-member-add-4761-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-group-member-add-4761-1&type=code)
- [microsoft-evsecurity-xml-group-member-add-success-4756](CodeChanges/microsoft-evsecurity-xml-group-member-add-success-4756.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-group-member-add-success-4756&type=code)
- [microsoft-evsecurity-xml-group-member-add-success-eventid47](CodeChanges/microsoft-evsecurity-xml-group-member-add-success-eventid47.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-group-member-add-success-eventid47&type=code)
- [microsoft-evsecurity-xml-group-modify-success-4750](CodeChanges/microsoft-evsecurity-xml-group-modify-success-4750.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-group-modify-success-4750&type=code)
- [microsoft-evsecurity-xml-group-modify-success-4755](CodeChanges/microsoft-evsecurity-xml-group-modify-success-4755.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-group-modify-success-4755&type=code)
- [microsoft-evsecurity-xml-group-modify-success-4760](CodeChanges/microsoft-evsecurity-xml-group-modify-success-4760.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-group-modify-success-4760&type=code)
- [microsoft-evsecurity-xml-handle-copy-4690](CodeChanges/microsoft-evsecurity-xml-handle-copy-4690.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-handle-copy-4690&type=code)
- [microsoft-evsecurity-xml-key-5061](CodeChanges/microsoft-evsecurity-xml-key-5061.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-key-5061&type=code)
- [microsoft-evsecurity-xml-key-5061-1](CodeChanges/microsoft-evsecurity-xml-key-5061-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-key-5061-1&type=code)
- [microsoft-evsecurity-xml-key-migrate-5059](CodeChanges/microsoft-evsecurity-xml-key-migrate-5059.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-key-migrate-5059&type=code)
- [microsoft-evsecurity-xml-log-clear-success-1102](CodeChanges/microsoft-evsecurity-xml-log-clear-success-1102.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-log-clear-success-1102&type=code)
- [microsoft-evsecurity-xml-member-remove-success-4762](CodeChanges/microsoft-evsecurity-xml-member-remove-success-4762.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-member-remove-success-4762&type=code)
- [microsoft-evsecurity-xml-member-remove-success-4762-1](CodeChanges/microsoft-evsecurity-xml-member-remove-success-4762-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-member-remove-success-4762-1&type=code)
- [microsoft-evsecurity-xml-network-session-success-5158](CodeChanges/microsoft-evsecurity-xml-network-session-success-5158.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-network-session-success-5158&type=code)
- [microsoft-evsecurity-xml-peripheral-storage-insert-success-6416](CodeChanges/microsoft-evsecurity-xml-peripheral-storage-insert-success-6416.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-peripheral-storage-insert-success-6416&type=code)
- [microsoft-evsecurity-xml-peripheral-storage-insert-success-6422](CodeChanges/microsoft-evsecurity-xml-peripheral-storage-insert-success-6422.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-peripheral-storage-insert-success-6422&type=code)
- [microsoft-evsecurity-xml-policy-modify-4946](CodeChanges/microsoft-evsecurity-xml-policy-modify-4946.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-policy-modify-4946&type=code)
- [microsoft-evsecurity-xml-user-delete-success-4743](CodeChanges/microsoft-evsecurity-xml-user-delete-success-4743.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-user-delete-success-4743&type=code)
- [microsoft-evsecurity-xml-user-unlock-success-4767-1](CodeChanges/microsoft-evsecurity-xml-user-unlock-success-4767-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-user-unlock-success-4767-1&type=code)
- [microsoft-evsecurity-xml-vpn-authentication-fail-6](CodeChanges/microsoft-evsecurity-xml-vpn-authentication-fail-6.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurity-xml-vpn-authentication-fail-6&type=code)
- [microsoft-evsecurityrds-xml-endpoint-time-modify-fail-129](CodeChanges/microsoft-evsecurityrds-xml-endpoint-time-modify-fail-129.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsecurityrds-xml-endpoint-time-modify-fail-129&type=code)
- [microsoft-evsetup-xml-app-activity-setup-1](CodeChanges/microsoft-evsetup-xml-app-activity-setup-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsetup-xml-app-activity-setup-1&type=code)
- [microsoft-evsmb-xml-endpoint-notification-success-catchall](CodeChanges/microsoft-evsmb-xml-endpoint-notification-success-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsmb-xml-endpoint-notification-success-catchall&type=code)
- [microsoft-evsystem-xml-driver-load-fail-225](CodeChanges/microsoft-evsystem-xml-driver-load-fail-225.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-xml-driver-load-fail-225&type=code)
- [microsoft-evsystem-xml-endpoint-login-fail-5805-1](CodeChanges/microsoft-evsystem-xml-endpoint-login-fail-5805-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-xml-endpoint-login-fail-5805-1&type=code)
- [microsoft-evsystem-xml-endpoint-notification-1085](CodeChanges/microsoft-evsystem-xml-endpoint-notification-1085.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-xml-endpoint-notification-1085&type=code)
- [microsoft-evsystem-xml-endpoint-notification-1196](CodeChanges/microsoft-evsystem-xml-endpoint-notification-1196.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-xml-endpoint-notification-1196&type=code)
- [microsoft-evsystem-xml-endpoint-time-modify-fail-129](CodeChanges/microsoft-evsystem-xml-endpoint-time-modify-fail-129.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-xml-endpoint-time-modify-fail-129&type=code)
- [microsoft-evsystem-xml-network-notification-49152](CodeChanges/microsoft-evsystem-xml-network-notification-49152.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-xml-network-notification-49152&type=code)
- [microsoft-evsystem-xml-network-session-fail-10028](CodeChanges/microsoft-evsystem-xml-network-session-fail-10028.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-xml-network-session-fail-10028&type=code)
- [microsoft-evsystem-xml-policy-apply-fail-1030](CodeChanges/microsoft-evsystem-xml-policy-apply-fail-1030.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-xml-policy-apply-fail-1030&type=code)
- [microsoft-evsystem-xml-policy-apply-fail-1096](CodeChanges/microsoft-evsystem-xml-policy-apply-fail-1096.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-xml-policy-apply-fail-1096&type=code)
- [microsoft-evsystem-xml-policy-apply-fail-1112](CodeChanges/microsoft-evsystem-xml-policy-apply-fail-1112.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-xml-policy-apply-fail-1112&type=code)
- [microsoft-evsystem-xml-policy-apply-fail-40](CodeChanges/microsoft-evsystem-xml-policy-apply-fail-40.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evsystem-xml-policy-apply-fail-40&type=code)
- [microsoft-evtaskscheduler-xml-endpoint-time-modify-fail-129](CodeChanges/microsoft-evtaskscheduler-xml-endpoint-time-modify-fail-129.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evtaskscheduler-xml-endpoint-time-modify-fail-129&type=code)
- [microsoft-evterminalservices-xml-endpoint-notification-success-catchall](CodeChanges/microsoft-evterminalservices-xml-endpoint-notification-success-catchall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-evterminalservices-xml-endpoint-notification-success-catchall&type=code)
- [microsoft-mssql-xml-database-login-success-33205](CodeChanges/microsoft-mssql-xml-database-login-success-33205.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-mssql-xml-database-login-success-33205&type=code)
- [microsoft-nps-xml-radius-traffic-fail-6273](CodeChanges/microsoft-nps-xml-radius-traffic-fail-6273.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-nps-xml-radius-traffic-fail-6273&type=code)
- [microsoft-o365-sk4-file-app-userkey](CodeChanges/microsoft-o365-sk4-file-app-userkey.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-o365-sk4-file-app-userkey&type=code)
- [microsoft-sysmon-xml-alert-trigger-success-25](CodeChanges/microsoft-sysmon-xml-alert-trigger-success-25.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-sysmon-xml-alert-trigger-success-25&type=code)
- [microsoft-sysmon-xml-dll-load-6](CodeChanges/microsoft-sysmon-xml-dll-load-6.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-sysmon-xml-dll-load-6&type=code)
- [microsoft-sysmon-xml-process-close-5-1](CodeChanges/microsoft-sysmon-xml-process-close-5-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-sysmon-xml-process-close-5-1&type=code)
- [microsoft-windows-xml-peripheral-storage-activity-success-devicewasdisable](CodeChanges/microsoft-windows-xml-peripheral-storage-activity-success-devicewasdisable.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-windows-xml-peripheral-storage-activity-success-devicewasdisable&type=code)
- [microsoft-windows-xml-peripheral-storage-activity-success-disable](CodeChanges/microsoft-windows-xml-peripheral-storage-activity-success-disable.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-windows-xml-peripheral-storage-activity-success-disable&type=code)
- [microsoft-windows-xml-peripheral-storage-activity-success-enableadevice](CodeChanges/microsoft-windows-xml-peripheral-storage-activity-success-enableadevice.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20microsoft-windows-xml-peripheral-storage-activity-success-enableadevice&type=code)

#### Removed Parser
<a id="removed-parser"></a>
- [amazon-ards-json-database-success-databaseactivity](CodeChanges/amazon-ards-json-database-success-databaseactivity.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-ards-json-database-success-databaseactivity&type=code)
- [amazon-awabastion-str-endpoint-login-success-logon](CodeChanges/amazon-awabastion-str-endpoint-login-success-logon.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awabastion-str-endpoint-login-success-logon&type=code)
- [amazon-awscloudtrail-cef-app-activity-assumedrole](CodeChanges/amazon-awscloudtrail-cef-app-activity-assumedrole.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-cef-app-activity-assumedrole&type=code)
- [amazon-awscloudtrail-json-app-activity-success-awsapicall](CodeChanges/amazon-awscloudtrail-json-app-activity-success-awsapicall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-json-app-activity-success-awsapicall&type=code)
- [amazon-awscloudtrail-sk4-user-create-createmembers](CodeChanges/amazon-awscloudtrail-sk4-user-create-createmembers.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudtrail-sk4-user-create-createmembers&type=code)
- [amazon-awscloudwatch-sk4-network-traffic-success-awss3bucket](CodeChanges/amazon-awscloudwatch-sk4-network-traffic-success-awss3bucket.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awscloudwatch-sk4-network-traffic-success-awss3bucket&type=code)
- [amazon-awsguardduty-sk4-alert-trigger-success-guardduty](CodeChanges/amazon-awsguardduty-sk4-alert-trigger-success-guardduty.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awsguardduty-sk4-alert-trigger-success-guardduty&type=code)
- [amazon-awsguardduty-sk4-alert-trigger-success-torclient](CodeChanges/amazon-awsguardduty-sk4-alert-trigger-success-torclient.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awsguardduty-sk4-alert-trigger-success-torclient&type=code)
- [amazon-awsssm-mix-app-notification-success-stop](CodeChanges/amazon-awsssm-mix-app-notification-success-stop.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-awsssm-mix-app-notification-success-stop&type=code)
- [amazon-rds-json-app-notification-auditevent](CodeChanges/amazon-rds-json-app-notification-auditevent.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-rds-json-app-notification-auditevent&type=code)
- [amazon-rds-json-app-notification-auditevent-1](CodeChanges/amazon-rds-json-app-notification-auditevent-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-rds-json-app-notification-auditevent-1&type=code)
- [amazon-rds-str-database-query-modify-success-auditevent](CodeChanges/amazon-rds-str-database-query-modify-success-auditevent.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-rds-str-database-query-modify-success-auditevent&type=code)
- [amazon-rds-str-database-query-modify-success-auditevent-1](CodeChanges/amazon-rds-str-database-query-modify-success-auditevent-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amazon-rds-str-database-query-modify-success-auditevent-1&type=code)
- [amd-p-csv-network-notification-success-flowdelete](CodeChanges/amd-p-csv-network-notification-success-flowdelete.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amd-p-csv-network-notification-success-flowdelete&type=code)
- [amd-p-csv-network-session-flowcreate](CodeChanges/amd-p-csv-network-session-flowcreate.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20amd-p-csv-network-session-flowcreate&type=code)
- [anywhere365-a-kv-app-activity-success-callreceive](CodeChanges/anywhere365-a-kv-app-activity-success-callreceive.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20anywhere365-a-kv-app-activity-success-callreceive&type=code)
- [anywhere365-a-kv-app-activity-success-conferencecreator](CodeChanges/anywhere365-a-kv-app-activity-success-conferencecreator.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20anywhere365-a-kv-app-activity-success-conferencecreator&type=code)
- [anywhere365-a-kv-app-activity-success-newconference](CodeChanges/anywhere365-a-kv-app-activity-success-newconference.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20anywhere365-a-kv-app-activity-success-newconference&type=code)
- [anywhere365-a-kv-app-activity-success-outboundcall](CodeChanges/anywhere365-a-kv-app-activity-success-outboundcall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20anywhere365-a-kv-app-activity-success-outboundcall&type=code)
- [anywhere365-a-kv-app-activity-success-ucccall](CodeChanges/anywhere365-a-kv-app-activity-success-ucccall.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20anywhere365-a-kv-app-activity-success-ucccall&type=code)
- [apache-a-json-http-session-chcomaccesslog](CodeChanges/apache-a-json-http-session-chcomaccesslog.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20apache-a-json-http-session-chcomaccesslog&type=code)
- [apache-guacamole-str-app-authentication-success-user](CodeChanges/apache-guacamole-str-app-authentication-success-user.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20apache-guacamole-str-app-authentication-success-user&type=code)
- [apache-guacamole-str-app-login-fail-authservice](CodeChanges/apache-guacamole-str-app-login-fail-authservice.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20apache-guacamole-str-app-login-fail-authservice&type=code)
- [apache-guacamole-str-app-login-fail-bindingerror](CodeChanges/apache-guacamole-str-app-login-fail-bindingerror.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20apache-guacamole-str-app-login-fail-bindingerror&type=code)
- [apache-subversion-mix-app-activity-headsvn-1](CodeChanges/apache-subversion-mix-app-activity-headsvn-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20apache-subversion-mix-app-activity-headsvn-1&type=code)
- [apache-subversion-mix-app-activity-optionssvn](CodeChanges/apache-subversion-mix-app-activity-optionssvn.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20apache-subversion-mix-app-activity-optionssvn&type=code)
- [apache-subversion-mix-app-activity-postsvn](CodeChanges/apache-subversion-mix-app-activity-postsvn.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20apache-subversion-mix-app-activity-postsvn&type=code)
- [apache-subversion-mix-app-activity-proppatchsvn](CodeChanges/apache-subversion-mix-app-activity-proppatchsvn.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20apache-subversion-mix-app-activity-proppatchsvn&type=code)
- [apache-subversion-mix-app-activity-putsvn](CodeChanges/apache-subversion-mix-app-activity-putsvn.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20apache-subversion-mix-app-activity-putsvn&type=code)
- [apache-subversion-mix-app-activity-reportsvn](CodeChanges/apache-subversion-mix-app-activity-reportsvn.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20apache-subversion-mix-app-activity-reportsvn&type=code)
- [appsense-am-leef-alert-trigger-success-appsenseapplicationmanager](CodeChanges/appsense-am-leef-alert-trigger-success-appsenseapplicationmanager.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20appsense-am-leef-alert-trigger-success-appsenseapplicationmanager&type=code)
- [assetview-av-str-alert-trigger-success-35131](CodeChanges/assetview-av-str-alert-trigger-success-35131.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20assetview-av-str-alert-trigger-success-35131&type=code)
- [bitglass-casb-kv-app-login-fail-login](CodeChanges/bitglass-casb-kv-app-login-fail-login.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20bitglass-casb-kv-app-login-fail-login&type=code)
- [bitglass-casb-kv-file-download-success-cloudstorage](CodeChanges/bitglass-casb-kv-file-download-success-cloudstorage.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20bitglass-casb-kv-file-download-success-cloudstorage&type=code)
- [bitglass-casb-kv-file-download-success-downloaded](CodeChanges/bitglass-casb-kv-file-download-success-downloaded.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20bitglass-casb-kv-file-download-success-downloaded&type=code)
- [bitglass-casb-sk4-alert-trigger-success-cloudsummary](CodeChanges/bitglass-casb-sk4-alert-trigger-success-cloudsummary.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20bitglass-casb-sk4-alert-trigger-success-cloudsummary&type=code)
- [blackberry-c-json-alert-trigger-success-cylancescore](CodeChanges/blackberry-c-json-alert-trigger-success-cylancescore.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20blackberry-c-json-alert-trigger-success-cylancescore&type=code)
- [checkpoint-ngfw-kv-app-login-success-smartdashboard](CodeChanges/checkpoint-ngfw-kv-app-login-success-smartdashboard.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20checkpoint-ngfw-kv-app-login-success-smartdashboard&type=code)
- [openai-oai-json-app-activity-success-apikeycreated](CodeChanges/openai-oai-json-app-activity-success-apikeycreated.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20openai-oai-json-app-activity-success-apikeycreated&type=code)
- [openai-oai-json-app-activity-success-apikeydeleted](CodeChanges/openai-oai-json-app-activity-success-apikeydeleted.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20openai-oai-json-app-activity-success-apikeydeleted&type=code)
- [sentinelone-s-cef-http-session-success-visibility-1](CodeChanges/sentinelone-s-cef-http-session-success-visibility-1.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20sentinelone-s-cef-http-session-success-visibility-1&type=code)

</details>

<details>
<summary><strong id="parsertemplate">ParserTemplate (4)</strong></summary>


### Change Types
- [Changed Parsed Fields](#changed-parsed-fields)
- [Edit Regex Field](#edit-regex-field)

#### Changed Parsed Fields
<a id="changed-parsed-fields"></a>
- [aws-cloudtrail-user-template](CodeChanges/aws-cloudtrail-user-template.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20aws-cloudtrail-user-template&type=code)

#### Edit Regex Field
<a id="edit-regex-field"></a>
- [s-xml-object-access](CodeChanges/s-xml-object-access.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20s-xml-object-access&type=code)
- [windows-events-3-dl](CodeChanges/windows-events-3-dl.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20windows-events-3-dl&type=code)
- [windows-xml-events](CodeChanges/windows-xml-events.md) [🔍](https://github.com/search?q=repo%3AExabeamLabs%2FContent-Library-CIM2%20windows-xml-events&type=code)

</details>