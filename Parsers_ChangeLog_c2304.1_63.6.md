 Parsers c2304.1_63.6 Changelog
========================================

This Changelog document  includes updates to Parsers  from content package c2206.2_97_63.5 to c2304.1_63.6.


Parsers
-----------------
Added 25

Removed 0

Modified 121


|Type |Parser Name                                                                     |Type of Change       |Modified Field       |
|--------------|---------------------------------------------------------------------------------|---------------------|--------------------|
|Parser        |exabeam-aa-kv-rule-trigger-success-anomaly                                       |Modified fields|N/A                 |
|Parser        |exabeam-aa-kv-rule-trigger-success-anomaly                                       |Removed field  |additional_info     |
|Parser        |exabeam-aa-kv-rule-trigger-success-anomaly                                       |Added field    |event_time          |
|Parser        |exabeam-aa-kv-rule-trigger-success-anomaly                                       |Added field    |mitre_labels        |
|Parser        |checkpoint-avanan-json-email-receive-securityevent                               |Modified regex     |alert_severity      |
|Parser        |checkpoint-avanan-json-email-receive-securityevent                               |Modified regex     |dest_email_address  |
|Parser        |checkpoint-avanan-json-email-receive-securityevent                               |Modified regex     |dest_email_domain   |
|Parser        |checkpoint-avanan-json-email-receive-securityevent                               |Modified regex     |email_recipients    |
|Parser        |checkpoint-avanan-json-email-send-securityevent                                  |Modified regex     |alert_severity      |
|Parser        |checkpoint-avanan-json-email-send-securityevent                                  |Modified regex     |dest_email_address  |
|Parser        |checkpoint-avanan-json-email-send-securityevent                                  |Modified regex     |dest_email_domain   |
|Parser        |checkpoint-avanan-json-email-send-securityevent                                  |Modified regex     |email_recipients    |
|Parser        |checkpoint-avanan-json-email-send-receive-phishing                               |Modified regex     |alert_severity      |
|Parser        |checkpoint-avanan-json-email-send-receive-phishing                               |Modified regex     |dest_email_address  |
|Parser        |checkpoint-avanan-json-email-send-receive-phishing                               |Modified regex     |dest_email_domain   |
|Parser        |checkpoint-avanan-json-email-send-receive-phishing                               |Modified regex     |email_recipients    |
|Parser        |checkpoint-avanan-json-alert-trigger-success-dlp                                 |Modified regex     |alert_severity      |
|Parser        |checkpoint-avanan-json-alert-trigger-success-dlp                                 |Modified regex     |dest_email_address  |
|Parser        |checkpoint-avanan-json-alert-trigger-success-dlp                                 |Modified regex     |dest_email_domain   |
|Parser        |checkpoint-avanan-json-alert-trigger-success-dlp                                 |Modified regex     |email_recipients    |
|Parser        |checkpoint-avanan-json-alert-trigger-success-securityeventmalware                |Modified regex     |alert_severity      |
|Parser        |checkpoint-avanan-json-alert-trigger-success-securityeventmalware                |Modified regex     |dest_email_address  |
|Parser        |checkpoint-avanan-json-alert-trigger-success-securityeventmalware                |Modified regex     |dest_email_domain   |
|Parser        |checkpoint-avanan-json-alert-trigger-success-securityeventmalware                |Modified regex     |email_recipients    |
|Parser        |checkpoint-avanan-json-email-receive-avanansecurityevent                         |Modified regex     |alert_severity      |
|Parser        |checkpoint-avanan-json-email-receive-avanansecurityevent                         |Modified regex     |dest_email_address  |
|Parser        |checkpoint-avanan-json-email-receive-avanansecurityevent                         |Modified regex     |dest_email_domain   |
|Parser        |checkpoint-avanan-json-email-receive-avanansecurityevent                         |Modified regex     |email_recipients    |
|Parser        |checkpoint-avanan-json-email-send-avanansecurityevent                            |Modified regex     |alert_severity      |
|Parser        |checkpoint-avanan-json-email-send-avanansecurityevent                            |Modified regex     |dest_email_address  |
|Parser        |checkpoint-avanan-json-email-send-avanansecurityevent                            |Modified regex     |dest_email_domain   |
|Parser        |checkpoint-avanan-json-email-send-avanansecurityevent                            |Modified regex     |email_recipients    |
|Parser        |checkpoint-avanan-json-alert-trigger-success-avanansecurityeventdlp              |Modified regex     |alert_severity      |
|Parser        |checkpoint-avanan-json-alert-trigger-success-avanansecurityeventdlp              |Modified regex     |dest_email_address  |
|Parser        |checkpoint-avanan-json-alert-trigger-success-avanansecurityeventdlp              |Modified regex     |dest_email_domain   |
|Parser        |checkpoint-avanan-json-alert-trigger-success-avanansecurityeventdlp              |Modified regex     |email_recipients    |
|Parser        |checkpoint-avanan-json-alert-trigger-success-avanansecurityeventmalware          |Modified regex     |alert_severity      |
|Parser        |checkpoint-avanan-json-alert-trigger-success-avanansecurityeventmalware          |Modified regex     |dest_email_address  |
|Parser        |checkpoint-avanan-json-alert-trigger-success-avanansecurityeventmalware          |Modified regex     |dest_email_domain   |
|Parser        |checkpoint-avanan-json-alert-trigger-success-avanansecurityeventmalware          |Modified regex     |email_recipients    |
|Parser        |microsoft-evsecurity-kv-ds-object-modify-success-4742                            |Modified fields|N/A                 |
|Parser        |microsoft-evsecurity-kv-ds-object-modify-success-4742                            |Removed field  |object              |
|Parser        |microsoft-evsecurity-kv-ds-object-modify-success-4742                            |Added field    |account_name        |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-3                             |Modified fields|N/A                 |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-3                             |Removed field  |dest_host           |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-3                             |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-3                             |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-3                             |Modified regex     |src_host            |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-3                             |Modified regex     |src_port            |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-3                             |Added field    |src_ip              |
|Parser        |microsoft-mssql-json-database-activity-success-dbactivity                        |Modified              |Conditions          |
|Parser        |microsoft-evsecurity-xml-user-enable-success-4722                                |Added attribute      |DupFields           |
|Parser        |microsoft-evsecurity-xml-share-access-success-5140                               |Modified regex     |dest_host           |
|Parser        |microsoft-evsecurity-xml-share-access-success-5140                               |Modified regex     |host                |
|Parser        |microsoft-evsystem-str-service-create-success-7045                               |Modified regex     |dest_host           |
|Parser        |microsoft-evsystem-str-service-create-success-7045                               |Modified regex     |dest_ip             |
|Parser        |microsoft-evsystem-str-service-create-success-7045                               |Modified regex     |host                |
|Parser        |microsoft-evsecurity-xml-scheduled-task-create-success-4700                      |Added attribute      |DupFields           |
|Parser        |microsoft-evsecurity-xml-scheduled-task-create-success-4700-1                    |Added attribute      |DupFields           |
|Parser        |microsoft-evsecurity-xml-scheduled-task-create-success-4700-2                    |Added attribute      |DupFields           |
|Parser        |microsoft-evsecurity-xml-ds-object-modify-success-5136                           |Modified regex     |dest_host           |
|Parser        |microsoft-evsecurity-xml-ds-object-modify-success-5136                           |Modified regex     |host                |
|Parser        |microsoft-evsecurity-xml-user-password-reset-success-4724                        |Modified regex     |dest_host           |
|Parser        |microsoft-evsecurity-xml-user-password-reset-success-4724                        |Modified regex     |host                |
|Parser        |microsoft-evsecurity-xml-endpoint-login-4769                                     |Modified regex     |dest_host           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4771                         |Modified fields|N/A                 |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4771                         |Removed field  |dest_host           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4771                         |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4771                         |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4771                         |Modified regex     |src_host            |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4771                         |Added field    |src_ip              |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4771                         |Added field    |src_port            |
|Parser        |microsoft-evsecurity-cef-endpoint-login-fail-4771                                |Modified regex     |dest_ip             |
|Parser        |microsoft-evsecurity-cef-endpoint-login-fail-4771                                |Modified regex     |dest_port           |
|Parser        |microsoft-evsecurity-cef-endpoint-login-fail-4771                                |Modified regex     |src_ip              |
|Parser        |microsoft-evsecurity-cef-endpoint-login-fail-4771                                |Modified regex     |src_port            |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771                               |Modified fields|N/A                 |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771                               |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771                               |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771                               |Added field    |src_ip              |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771                               |Added field    |src_port            |
|Parser        |microsoft-evsecurity-json-registry-create-success-4657                           |Added attribute      |DupFields           |
|Parser        |microsoft-evsecurity-str-registry-create-success-4657                            |Modified regex     |host                |
|Parser        |microsoft-evsecurity-str-registry-create-success-4657                            |Added attribute      |DupFields           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4625                                 |Modified regex     |dest_host           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4625                                 |Modified regex     |dest_ip             |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4625                                 |Modified regex     |host                |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771-1                              |Modified fields|N/A                 |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771-1                              |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771-1                              |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771-1                              |Added field    |src_ip              |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771-1                              |Added field    |src_port            |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771                                |Modified fields|N/A                 |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771                                |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771                                |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771                                |Added field    |src_ip              |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771                                |Added field    |src_port            |
|Parser        |microsoft-evsecurity-kv-endpoint-login-failed-4771-jp                            |Modified fields|N/A                 |
|Parser        |microsoft-evsecurity-kv-endpoint-login-failed-4771-jp                            |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-kv-endpoint-login-failed-4771-jp                            |Added field    |src_ip              |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-2                               |Modified fields|N/A                 |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-2                               |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-2                               |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-2                               |Added field    |src_ip              |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-2                               |Added field    |src_port            |
|Parser        |microsoft-evsecurity-xml-registry-create-success-4657                            |Added attribute      |DupFields           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Modified fields|N/A                 |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Modified regex     |domain              |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Modified regex     |event_code          |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Modified regex     |host                |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Modified regex     |result_code         |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Modified regex     |user                |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Modified regex     |user_sid            |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Added field    |src_ip              |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Added field    |src_port            |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-4                             |Modified fields|N/A                 |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-4                             |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-4                             |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-4                             |Added field    |src_ip              |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-4                             |Added field    |src_port            |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-1                               |Modified fields|N/A                 |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-1                               |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-1                               |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-1                               |Added field    |src_ip              |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-1                               |Added field    |src_port            |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-3                               |Modified fields|N/A                 |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-3                               |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-3                               |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-3                               |Added field    |src_ip              |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-3                               |Added field    |src_port            |
|Parser        |microsoft-evsecurity-kv-share-access-5145-3                                      |Modified regex     |file_dir            |
|Parser        |microsoft-evsecurity-kv-share-access-5145-3                                      |Modified regex     |file_ext            |
|Parser        |microsoft-evsecurity-kv-share-access-5145-3                                      |Modified regex     |file_name           |
|Parser        |cisco-duo-cef-vpn-login-fail-loginfailure                                        |Modified fields|N/A                 |
|Parser        |cisco-duo-cef-vpn-login-fail-loginfailure                                        |Removed field  |operation           |
|Parser        |cisco-duo-cef-vpn-login-fail-loginfailure                                        |Added field    |factor              |
|Parser        |cisco-duo-cef-vpn-login-fail-loginfailure                                        |removed_attribute    |DupFields           |
|Parser        |cisco-duo-sk4-vpn-login-success-newenrollment                                    |Modified fields|N/A                 |
|Parser        |cisco-duo-sk4-vpn-login-success-newenrollment                                    |Removed field  |operation           |
|Parser        |cisco-duo-sk4-vpn-login-success-newenrollment                                    |Added field    |factor              |
|Parser        |cisco-duo-kv-app-activity-success-userupdate                                     |Modified fields|N/A                 |
|Parser        |cisco-duo-kv-app-activity-success-userupdate                                     |Removed field  |action              |
|Parser        |cisco-duo-kv-app-activity-success-userupdate                                     |Added field    |factor              |
|Parser        |cisco-duo-json-endpoint-authentication-ip                                        |Modified fields|N/A                 |
|Parser        |cisco-duo-json-endpoint-authentication-ip                                        |Removed field  |auth_method         |
|Parser        |cisco-duo-json-endpoint-authentication-ip                                        |Added field    |factor              |
|Parser        |cisco-duo-json-endpoint-authentication-result-1                                  |Modified fields|N/A                 |
|Parser        |cisco-duo-json-endpoint-authentication-result-1                                  |Removed field  |auth_method         |
|Parser        |cisco-duo-json-endpoint-authentication-result-1                                  |Added field    |factor              |
|Parser        |cisco-duo-json-app-login-success-adminlogin-1                                    |Modified fields|N/A                 |
|Parser        |cisco-duo-json-app-login-success-adminlogin-1                                    |Removed field  |action              |
|Parser        |cisco-duo-json-app-login-success-adminlogin-1                                    |Added field    |factor              |
|Parser        |cisco-duo-kv-app-activity-success-sendenrollcode                                 |Modified fields|N/A                 |
|Parser        |cisco-duo-kv-app-activity-success-sendenrollcode                                 |Removed field  |action              |
|Parser        |cisco-duo-kv-app-activity-success-sendenrollcode                                 |Added field    |factor              |
|Parser        |cisco-duo-json-app-activity-success-usercreate-1                                 |Modified fields|N/A                 |
|Parser        |cisco-duo-json-app-activity-success-usercreate-1                                 |Removed field  |action              |
|Parser        |cisco-duo-json-app-activity-success-usercreate-1                                 |Added field    |factor              |
|Parser        |cisco-duo-json-app-activity-success-userpending                                  |Modified fields|N/A                 |
|Parser        |cisco-duo-json-app-activity-success-userpending                                  |Removed field  |action              |
|Parser        |cisco-duo-json-app-activity-success-userpending                                  |Added field    |factor              |
|Parser        |cisco-duo-json-app-activity-success-phoneupdate                                  |Modified fields|N/A                 |
|Parser        |cisco-duo-json-app-activity-success-phoneupdate                                  |Removed field  |action              |
|Parser        |cisco-duo-json-app-activity-success-phoneupdate                                  |Added field    |factor              |
|Parser        |microsoft-o365-sk4-file-write-success-filemodified                               |Modified regex     |src_ip              |
|Parser        |microsoft-o365-sk4-file-write-success-filemodified                               |Modified regex     |src_port            |
|Parser        |microsoft-o365-cef-app-login-success-user                                        |Modified regex     |user_agent          |
|Parser        |microsoft-o365-cef-app-file-success-displayname                                  |Modified fields|N/A                 |
|Parser        |microsoft-o365-cef-app-file-success-displayname                                  |Added field    |result_reason       |
|Parser        |microsoft-o365-mix-file-success-workload                                         |Modified regex     |src_ip              |
|Parser        |microsoft-o365-mix-file-success-workload                                         |Modified regex     |src_port            |
|Parser        |microsoft-o365-sk4-file-app-userkey                                              |Modified regex     |src_ip              |
|Parser        |microsoft-o365-sk4-file-app-userkey                                              |Modified regex     |src_port            |
|Parser        |microsoft-o365-sk4-file-app-userkey-1                                            |Modified regex     |src_ip              |
|Parser        |microsoft-o365-sk4-file-app-userkey-1                                            |Modified regex     |src_port            |
|Parser        |microsoft-o365-json-email-receive-success-emailreceive                           |Modified regex     |external_address    |
|Parser        |microsoft-azureadip-json-alert-trigger-success-graphsecurityalert                |Modified regex     |src_ip              |
|Parser        |microsoft-azureadip-json-alert-trigger-success-graphsecurityalert                |Modified regex     |src_port            |
|Parser        |microsoft-azureadip-json-alert-trigger-success-graphsecurityalert                |Modified regex     |time                |
|Parser        |microsoft-mcas-json-alert-trigger-success-velocity                               |Modified regex     |src_ip              |
|Parser        |microsoft-mcas-json-alert-trigger-success-velocity                               |Modified regex     |src_port            |
|Parser        |microsoft-mcas-json-alert-trigger-success-velocity                               |Modified regex     |time                |
|Parser        |microsoft-mcas-json-alert-trigger-success-login                                  |Modified regex     |src_ip              |
|Parser        |microsoft-mcas-json-alert-trigger-success-login                                  |Modified regex     |src_port            |
|Parser        |microsoft-mcas-json-alert-trigger-success-login                                  |Modified regex     |time                |
|Parser        |microsoft-mcas-json-alert-trigger-success-download                               |Modified regex     |src_ip              |
|Parser        |microsoft-mcas-json-alert-trigger-success-download                               |Modified regex     |src_port            |
|Parser        |microsoft-mcas-json-alert-trigger-success-download                               |Modified regex     |time                |
|Parser        |microsoft-mcas-json-alert-trigger-success-ransomware                             |Modified regex     |src_ip              |
|Parser        |microsoft-mcas-json-alert-trigger-success-ransomware                             |Modified regex     |src_port            |
|Parser        |microsoft-mcas-json-alert-trigger-success-ransomware                             |Modified regex     |time                |
|Parser        |microsoft-azureatp-json-alert-trigger-success-remoteexecutionsecurityalert-1     |Modified regex     |src_ip              |
|Parser        |microsoft-azureatp-json-alert-trigger-success-remoteexecutionsecurityalert-1     |Modified regex     |src_port            |
|Parser        |microsoft-azureatp-json-alert-trigger-success-remoteexecutionsecurityalert-1     |Modified regex     |time                |
|Parser        |microsoft-azureatp-json-alert-trigger-success-netlogonbypasssecurityalert-1      |Modified regex     |src_ip              |
|Parser        |microsoft-azureatp-json-alert-trigger-success-netlogonbypasssecurityalert-1      |Modified regex     |src_port            |
|Parser        |microsoft-azureatp-json-alert-trigger-success-netlogonbypasssecurityalert-1      |Modified regex     |time                |
|Parser        |microsoft-defenderep-json-alert-trigger-success-suspiciousactivity               |Modified regex     |src_ip              |
|Parser        |microsoft-defenderep-json-alert-trigger-success-suspiciousactivity               |Modified regex     |src_port            |
|Parser        |microsoft-defenderep-json-alert-trigger-success-suspiciousactivity               |Modified regex     |time                |
|Parser        |microsoft-defenderep-json-alert-trigger-success-collection                       |Modified regex     |src_ip              |
|Parser        |microsoft-defenderep-json-alert-trigger-success-collection                       |Modified regex     |src_port            |
|Parser        |microsoft-defenderep-json-alert-trigger-success-collection                       |Modified regex     |time                |
|Parser        |microsoft-defenderep-json-alert-trigger-success-malware-1                        |Modified regex     |src_ip              |
|Parser        |microsoft-defenderep-json-alert-trigger-success-malware-1                        |Modified regex     |src_port            |
|Parser        |microsoft-defenderep-json-alert-trigger-success-malware-1                        |Modified regex     |time                |
|Parser        |microsoft-defenderep-json-alert-trigger-success-lateralmovement-1                |Modified regex     |src_ip              |
|Parser        |microsoft-defenderep-json-alert-trigger-success-lateralmovement-1                |Modified regex     |src_port            |
|Parser        |microsoft-defenderep-json-alert-trigger-success-lateralmovement-1                |Modified regex     |time                |
|Parser        |microsoft-defenderep-json-alert-trigger-success-unwantedsoftware                 |Modified regex     |src_ip              |
|Parser        |microsoft-defenderep-json-alert-trigger-success-unwantedsoftware                 |Modified regex     |src_port            |
|Parser        |microsoft-defenderep-json-alert-trigger-success-unwantedsoftware                 |Modified regex     |time                |
|Parser        |microsoft-defenderep-json-alert-trigger-success-persistence-1                    |Modified regex     |src_ip              |
|Parser        |microsoft-defenderep-json-alert-trigger-success-persistence-1                    |Modified regex     |src_port            |
|Parser        |microsoft-defenderep-json-alert-trigger-success-persistence-1                    |Modified regex     |time                |
|Parser        |microsoft-defenderep-json-alert-trigger-success-exploit-1                        |Modified regex     |src_ip              |
|Parser        |microsoft-defenderep-json-alert-trigger-success-exploit-1                        |Modified regex     |src_port            |
|Parser        |microsoft-defenderep-json-alert-trigger-success-exploit-1                        |Modified regex     |time                |
|Parser        |crowdstrike-falcon-mix-file-write-success-directorycreate                        |Modified regex     |file_dir            |
|Parser        |crowdstrike-falcon-mix-file-write-success-directorycreate                        |Modified regex     |file_ext            |
|Parser        |crowdstrike-falcon-mix-file-write-success-directorycreate                        |Modified regex     |file_name           |
|Parser        |crowdstrike-falcon-mix-file-write-success-directorycreate                        |Modified regex     |file_path           |
|Parser        |cisco-duo-kv-app-login-success-adminlogin                                        |Modified fields|N/A                 |
|Parser        |cisco-duo-kv-app-login-success-adminlogin                                        |Removed field  |action              |
|Parser        |cisco-duo-kv-app-login-success-adminlogin                                        |Added field    |factor              |
|Parser        |vmware-esxi-str-endpoint-login-success-loggedin                                  |Modified regex     |event_name          |
|Parser        |vmware-esxi-str-endpoint-login-success-loggedin                                  |Modified regex     |host                |
|Parser        |vmware-esxi-str-endpoint-login-success-loggedin                                  |Modified regex     |operation           |
|Parser        |vmware-esxi-str-endpoint-login-success-loggedin                                  |Modified regex     |time                |
|Parser        |zscaler-ia-cef-http-session-spriv                                                |Modified regex     |top_domain          |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Modified fields|N/A                 |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Modified regex     |additional_info     |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Modified regex     |email_address       |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Removed field  |event_name          |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Modified regex     |operation           |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Modified regex     |result              |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Modified regex     |src_ip              |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Modified regex     |src_port            |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Modified regex     |time                |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Modified regex     |user                |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Added field    |app_type            |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Added field    |object              |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Added field    |resource            |
|Parser        |symantec-dlp-kv-email-send-incident                                              |Modified regex     |file_ext            |
|Parser        |symantec-dlp-kv-email-send-incident                                              |Modified regex     |file_name           |
|Parser        |f5-apm-str-vpn-success-01490005                                                  |Modified fields|N/A                 |
|Parser        |f5-apm-str-vpn-success-01490005                                                  |Added field    |host                |
|Parser        |proofpoint-tappod-json-email-send-receive-rcpts                                  |Modified regex     |dest_email_address  |
|Parser        |proofpoint-tappod-json-email-send-receive-rcpts                                  |Modified regex     |email_recipients    |
|Parser        |proofpoint-tappod-json-email-send-receive-rcpts                                  |Modified regex     |email_subject       |
|Parser        |pingidentity-pi-kv-app-login-success-sso                                         |Modified fields|N/A                 |
|Parser        |pingidentity-pi-kv-app-login-success-sso                                         |Modified regex     |email_address       |
|Parser        |pingidentity-pi-kv-app-login-success-sso                                         |Modified regex     |user                |
|Parser        |pingidentity-pi-kv-app-login-success-sso                                         |Added field    |email_domain        |
|Parser        |unix-unix-str-endpoint-login-fail-unablesshd                                     |Modified regex     |dest_host           |
|Parser        |unix-unix-str-endpoint-login-fail-unablesshd                                     |Modified regex     |dest_ip             |
|Parser        |unix-unix-str-endpoint-login-fail-unablesshd                                     |Modified regex     |host                |
|Parser        |unix-unix-str-endpoint-login-fail-unablesshd                                     |Modified regex     |src_host            |
|Parser        |unix-unix-str-endpoint-login-fail-unablesshd                                     |Modified regex     |src_ip              |
|Parser        |unix-unix-str-endpoint-login-fail-invaliduser                                    |Modified regex     |host                |
|Parser        |unix-unix-str-endpoint-login-fail-manyauthfail                                   |Modified regex     |src_ip              |
|Parser        |unix-unix-mix-ssh-traffic-success-ssh2accepted                                   |Modified regex     |additional_info     |
|Parser        |unix-unix-mix-ssh-traffic-success-ssh2accepted                                   |Modified regex     |dest_host           |
|Parser        |unix-unix-mix-ssh-traffic-success-ssh2accepted                                   |Modified regex     |host                |
|Parser        |unix-unix-mix-ssh-traffic-success-ssh2accepted                                   |Modified regex     |login_id            |
|Parser        |unix-unix-str-endpoint-login-sshdconnectionfrom                                  |Modified fields|N/A                 |
|Parser        |unix-unix-str-endpoint-login-sshdconnectionfrom                                  |Removed field  |dest_ip             |
|Parser        |unix-unix-str-endpoint-login-sshdconnectionfrom                                  |Removed field  |dest_port           |
|Parser        |unix-unix-str-endpoint-login-sshdconnectionfrom                                  |Modified regex     |host                |
|Parser        |unix-unix-str-endpoint-login-sshdconnectionfrom                                  |Added field    |src_ip              |
|Parser        |unix-unix-str-endpoint-login-sshdconnectionfrom                                  |Added field    |src_port            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Modified fields|N/A                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Modified regex     |alert_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Modified regex     |alert_type          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Modified regex     |dest_ip             |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Modified regex     |dest_port           |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Modified regex     |email_address       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Modified regex     |event_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Modified regex     |instance_id         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Modified regex     |location_city       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Modified regex     |src_ip              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Modified regex     |user                |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Added field    |alert_id            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Added field    |app                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Added field    |aws_account         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Added field    |result              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Added field    |src_port            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Modified fields|N/A                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Modified regex     |alert_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Modified regex     |alert_type          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Modified regex     |dest_ip             |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Modified regex     |dest_port           |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Modified regex     |email_address       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Modified regex     |event_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Modified regex     |instance_id         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Modified regex     |location_city       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Modified regex     |src_ip              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Modified regex     |user                |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Added field    |alert_id            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Added field    |app                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Added field    |aws_account         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Added field    |result              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Added field    |src_port            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Modified fields|N/A                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Modified regex     |alert_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Modified regex     |alert_type          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Modified regex     |dest_ip             |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Modified regex     |dest_port           |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Modified regex     |email_address       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Modified regex     |event_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Modified regex     |instance_id         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Modified regex     |location_city       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Modified regex     |src_ip              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Modified regex     |user                |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Added field    |alert_id            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Added field    |app                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Added field    |aws_account         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Added field    |result              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Added field    |src_port            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Modified fields|N/A                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Modified regex     |alert_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Modified regex     |alert_type          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Modified regex     |dest_ip             |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Modified regex     |dest_port           |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Modified regex     |email_address       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Modified regex     |event_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Modified regex     |instance_id         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Modified regex     |location_city       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Modified regex     |src_ip              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Modified regex     |user                |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Added field    |alert_id            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Added field    |app                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Added field    |aws_account         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Added field    |result              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Added field    |src_port            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Modified fields|N/A                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Modified regex     |alert_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Modified regex     |alert_type          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Modified regex     |dest_ip             |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Modified regex     |dest_port           |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Modified regex     |email_address       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Modified regex     |event_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Modified regex     |instance_id         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Modified regex     |location_city       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Modified regex     |src_ip              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Modified regex     |user                |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Added field    |alert_id            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Added field    |app                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Added field    |aws_account         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Added field    |result              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Added field    |src_port            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Modified fields|N/A                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Modified regex     |alert_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Modified regex     |alert_type          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Modified regex     |dest_ip             |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Modified regex     |dest_port           |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Modified regex     |email_address       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Modified regex     |event_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Modified regex     |instance_id         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Modified regex     |location_city       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Modified regex     |src_ip              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Modified regex     |user                |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Added field    |alert_id            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Added field    |app                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Added field    |aws_account         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Added field    |result              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Added field    |src_port            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Modified fields|N/A                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Modified regex     |alert_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Modified regex     |alert_type          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Modified regex     |dest_ip             |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Modified regex     |dest_port           |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Modified regex     |email_address       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Modified regex     |event_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Modified regex     |instance_id         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Modified regex     |location_city       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Modified regex     |src_ip              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Modified regex     |user                |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Added field    |alert_id            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Added field    |app                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Added field    |aws_account         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Added field    |result              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Added field    |src_port            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Modified fields|N/A                 |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Modified regex     |alert_name          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Modified regex     |alert_type          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Modified regex     |dest_ip             |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Modified regex     |dest_port           |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Modified regex     |email_address       |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Modified regex     |event_name          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Modified regex     |instance_id         |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Modified regex     |location_city       |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Modified regex     |src_ip              |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Modified regex     |user                |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Added field    |alert_id            |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Added field    |app                 |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Added field    |aws_account         |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Added field    |result              |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Added field    |src_port            |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Modified fields|N/A                 |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Modified regex     |alert_name          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Modified regex     |alert_type          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Modified regex     |dest_ip             |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Modified regex     |dest_port           |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Modified regex     |email_address       |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Modified regex     |event_name          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Modified regex     |instance_id         |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Modified regex     |location_city       |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Modified regex     |src_ip              |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Modified regex     |user                |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Added field    |alert_id            |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Added field    |app                 |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Added field    |aws_account         |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Added field    |result              |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Added field    |src_port            |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Modified fields|N/A                 |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Modified regex     |alert_name          |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Modified regex     |alert_type          |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Modified regex     |dest_ip             |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Modified regex     |dest_port           |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Modified regex     |email_address       |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Modified regex     |event_name          |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Modified regex     |instance_id         |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Modified regex     |location_city       |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Modified regex     |src_ip              |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Modified regex     |user                |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Added field    |alert_id            |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Added field    |app                 |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Added field    |aws_account         |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Added field    |result              |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Added field    |src_port            |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Modified fields|N/A                 |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Modified regex     |alert_name          |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Modified regex     |alert_type          |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Modified regex     |dest_ip             |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Modified regex     |dest_port           |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Modified regex     |email_address       |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Modified regex     |event_name          |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Modified regex     |instance_id         |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Modified regex     |location_city       |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Modified regex     |src_ip              |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Modified regex     |user                |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Added field    |alert_id            |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Added field    |app                 |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Added field    |aws_account         |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Added field    |result              |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Added field    |src_port            |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Modified fields|N/A                 |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Modified regex     |alert_name          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Modified regex     |alert_type          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Modified regex     |dest_ip             |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Modified regex     |dest_port           |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Modified regex     |email_address       |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Modified regex     |event_name          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Modified regex     |instance_id         |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Modified regex     |location_city       |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Modified regex     |src_ip              |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Modified regex     |user                |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Added field    |alert_id            |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Added field    |app                 |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Added field    |aws_account         |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Added field    |result              |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Added field    |src_port            |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Modified fields|N/A                 |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Modified regex     |additional_info     |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Modified regex     |alert_name          |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Modified regex     |alert_severity      |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Modified regex     |alert_type          |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Removed field  |dest_host           |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Modified regex     |dest_ip             |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Modified regex     |dest_port           |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Modified regex     |email_address       |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Modified regex     |event_name          |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Modified regex     |src_ip              |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Modified regex     |src_port            |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Modified regex     |time                |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Modified regex     |user                |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Added field    |account_id          |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Added field    |domain              |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Added field    |email_domain        |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Added field    |instance_id         |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Added field    |location_city       |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Added field    |object              |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Added field    |region              |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Added field    |resource_type       |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Added field    |user_type           |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Modified fields|N/A                 |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Modified regex     |alert_name          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Modified regex     |alert_type          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Modified regex     |dest_ip             |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Modified regex     |dest_port           |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Modified regex     |email_address       |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Modified regex     |event_name          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Modified regex     |instance_id         |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Modified regex     |location_city       |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Modified regex     |src_ip              |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Modified regex     |user                |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Added field    |alert_id            |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Added field    |app                 |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Added field    |aws_account         |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Added field    |result              |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Added field    |src_port            |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Added attribute      |ExtractionType      |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |Modified fields|N/A                 |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |Modified regex     |account_domain      |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |Modified regex     |account_name        |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |Modified regex     |src_ip              |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |Modified regex     |src_port            |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |Modified regex     |time                |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |Modified regex     |user                |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |Added field    |domain              |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |Added field    |src_host            |
|Parser        |microsoft-azuremon-sk4-app-authentication-accounttokenlogin                      |Modified regex     |src_ip              |
|Parser        |microsoft-azuremon-sk4-app-authentication-accounttokenlogin                      |Modified regex     |src_port            |
|Parser        |microsoft-azuremon-sk4-app-logout-sshlogout                                      |Modified regex     |src_ip              |
|Parser        |microsoft-azuremon-sk4-app-logout-sshlogout                                      |Modified regex     |src_port            |
|Parser        |microsoft-azuremon-sk4-secret-read-getsecret                                     |Modified regex     |src_ip              |
|Parser        |microsoft-azuremon-sk4-secret-read-getsecret                                     |Modified regex     |src_port            |
|Parser        |microsoft-azuremon-sk4-app-notification-clusterstartresult                       |Modified regex     |src_ip              |
|Parser        |microsoft-azuremon-sk4-app-notification-clusterstartresult                       |Modified regex     |src_port            |
|Parser        |microsoft-azuremon-sk4-app-notification-clusterstart                             |Modified regex     |src_ip              |
|Parser        |microsoft-azuremon-sk4-app-notification-clusterstart                             |Modified regex     |src_port            |
|Parser        |pan-ngfw-json-app-activity-success-subtype                                       |Modified regex     |host                |
|Parser        |pan-ngfw-json-alert-trigger-success-hipmatch                                     |Modified regex     |host                |
|Parser        |pan-ngfw-json-app-notification-success-userid                                    |Modified regex     |host                |
|Parser        |pan-ngfw-json-vpn-authentication-success-subtypevpn                              |Modified regex     |host                |
|Parser        |pan-ngfw-json-app-notification-success-dhcp                                      |Modified regex     |host                |
|Parser        |vmware-esxi-str-app-activity-hostd                                               |Modified regex     |domain              |
|Parser        |vmware-esxi-str-app-activity-hostd                                               |Modified regex     |user                |
|Parser        |f5-f-kv-app-activity-common                                                      |Modified fields|N/A                 |
|Parser        |f5-f-kv-app-activity-common                                                      |Added field    |host                |
|Parser        |unix-unix-str-endpoint-authentication-check                                      |Modified regex     |host                |
|Parser        |unix-unix-str-network-start-snmpd                                                |Modified regex     |dest_ip             |
|Parser        |unix-unix-str-network-start-snmpd                                                |Modified regex     |dest_port           |
|Parser        |unix-unix-str-network-start-snmpd                                                |Modified regex     |event_name          |
|Parser        |unix-unix-str-network-start-snmpd                                                |Modified regex     |host                |
|Parser        |unix-unix-str-network-start-snmpd                                                |Modified regex     |process_id          |
|Parser        |unix-unix-str-network-start-snmpd                                                |Modified regex     |protocol            |
|Parser        |unix-unix-str-network-start-snmpd                                                |Modified regex     |src_ip              |
|Parser        |unix-unix-str-network-start-snmpd                                                |Modified regex     |src_port            |
|Parser        |unix-unix-str-endpoint-activity-systemd                                          |Modified regex     |host                |
|Parser        |unix-unix-str-endpoint-logout-sshdreceiveddisconnect                             |Modified regex     |host                |
|Parser        |unix-unix-str-endpoint-logout-sshdconnectionclosed                               |Modified regex     |host                |
|Parser        |unix-unix-str-endpoint-logout-disconnected                                       |Modified regex     |host                |
|Parser        |unix-unix-str-endpoint-activity-crond                                            |Modified regex     |host                |
|Parser        |airlock-allowlisting-json-app-activity-success-fileactivity                      |Modified fields|N/A                 |
|Parser        |airlock-allowlisting-json-app-activity-success-fileactivity                      |Added field    |process_command_line|
|Parser        |airlock-allowlisting-json-app-activity-success-fileactivity                      |Added attribute      |DupFields           |
|Parser        |microsoft-azuresc-json-alert-trigger-success-security                            |Added Parser         |N/A                 |
|Parser        |microsoft-defenderep-json-alert-trigger-success-persistence-2                    |Added Parser         |N/A                 |
|Parser        |azure-azuread-json-user-password-modify-success-selfservice-1                    |Added Parser         |N/A                 |
|Parser        |microsoft-azure-json-app-activity-adduser                                        |Added Parser         |N/A                 |
|Parser        |microsoft-azure-json-app-activity-deleteuser                                     |Added Parser         |N/A                 |
|Parser        |microsoft-azure-json-app-activity-changeuserlicense                              |Added Parser         |N/A                 |
|Parser        |microsoft-o365-json-app-file-success-inviteexternaluser                          |Added Parser         |N/A                 |
|Parser        |microsoft-azure-json-group-member-remove-success-removefromgroup                 |Added Parser         |N/A                 |
|Parser        |pan-ngfw-json-endpoint-authentication-success-authsuccess                        |Added Parser         |N/A                 |
|Parser        |pan-ngfw-json-endpoint-authentication-fail-authfail                              |Added Parser         |N/A                 |
|Parser        |pan-ngfw-json-endpoint-authentication-success-signvalidated                      |Added Parser         |N/A                 |
|Parser        |zscaler-ia-csv-app-activity-success-nssupdate                                    |Added Parser         |N/A                 |
|Parser        |zscaler-ia-csv-app-activity-success-nssdelete                                    |Added Parser         |N/A                 |
|Parser        |pingidentity-pi-json-app-authentication-fail-authfail                            |Added Parser         |N/A                 |
|Parser        |pingidentity-pi-json-app-login-success-ssoidp                                    |Added Parser         |N/A                 |
|Parser        |pingidentity-pi-json-app-login-ssosession                                        |Added Parser         |N/A                 |
|Parser        |pingidentity-pi-json-app-activity-success-deviceadded                            |Added Parser         |N/A                 |
|Parser        |pingidentity-pi-json-app-activity-success-deviceunpaired                         |Added Parser         |N/A                 |
|Parser        |microsoft-evsecurity-xml-endpoint-notification-success-4802                      |Added Parser         |N/A                 |
|Parser        |pan-ngfw-json-app-notification-success-auth                                      |Added Parser         |N/A                 |
|Parser        |pan-ngfw-json-app-activity-success-samlidpactivity                               |Added Parser         |N/A                 |
|Parser        |crowdstrike-falcon-json-network-traffic-success-networkreceiveaccept             |Added Parser         |N/A                 |
|Parser        |pingidentity-pingone-json-user-role-assign-success-roleassignmentcreated         |Added Parser         |N/A                 |
|Parser        |pingidentity-pingone-json-user-role-revoke-success-roleassignmentdeleted         |Added Parser         |N/A                 |
|Parser        |pingidentity-pingone-json-user-modify-success-userupdated                        |Added Parser         |N/A                 |
|ParserTemplate|json-avanan-security-alert                                                       |Modified regex     |alert_severity      |
|ParserTemplate|json-avanan-security-alert                                                       |Modified regex     |dest_email_address  |
|ParserTemplate|json-avanan-security-alert                                                       |Modified regex     |dest_email_domain   |
|ParserTemplate|json-avanan-security-alert                                                       |Modified regex     |email_recipients    |
|ParserTemplate|json-pan-system                                                                  |Modified regex     |host                |
|ParserTemplate|q-duo-app-activity                                                               |Modified fields|N/A                 |
|ParserTemplate|q-duo-app-activity                                                               |Removed field  |action              |
|ParserTemplate|q-duo-app-activity                                                               |Added field    |factor              |
|ParserTemplate|o365-file-app-activity                                                           |Modified regex     |src_ip              |
|ParserTemplate|o365-file-app-activity                                                           |Modified regex     |src_port            |
|ParserTemplate|defender-atp-security-alert-events                                               |Modified regex     |src_ip              |
|ParserTemplate|defender-atp-security-alert-events                                               |Modified regex     |src_port            |
|ParserTemplate|defender-atp-security-alert-events                                               |Modified regex     |time                |
|ParserTemplate|ping-events-1                                                                    |removed_attribute    |ParserVersion       |
|ParserTemplate|zscaler-ia-csv-events                                                            |Added Parser_template|N/A                 |
|ParserTemplate|microsoft-azuread-json-events                                                    |Added Parser_template|N/A                 |
|ParserTemplate|json-aws-guardduty-security-alert-template                                       |Added Parser_template|N/A                 |
|ParserTemplate|json-ping-events                                                                 |Added Parser_template|N/A                 |
|ParserTemplate|pingone-events                                                                   |Added Parser_template|N/A                 |
|Parser        |vmware-esxi-str-endpoint-login-success-loggedin                                  |edit_attribute       |activity_type       |
|Parser        |vmware-esxi-str-endpoint-login-success-loggedin                                  |edit_attribute       |legacy_activity_type|
|Parser        |vmware-esxi-str-endpoint-login-success-loggedin-1                                |edit_attribute       |activity_type       |
|Parser        |vmware-esxi-str-endpoint-login-success-loggedin-1                                |edit_attribute       |legacy_activity_type|
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |edit_attribute       |activity_type       |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |edit_attribute       |legacy_activity_type|
