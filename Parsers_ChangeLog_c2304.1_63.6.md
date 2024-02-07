 Parsers c2304.1_63.6 Changelog
========================================

This Changelog document  includes updates to Parsers  from content package c2206.2_97_63.5 to c2304.1_63.6.


Parsers
-----------------
|Type |Parser Name                                                                     |Type of Change       |Changed Field       |
|--------------|---------------------------------------------------------------------------------|---------------------|--------------------|
|Parser        |exabeam-aa-kv-rule-trigger-success-anomaly                                       |Changed fields|N/A                 |
|Parser        |exabeam-aa-kv-rule-trigger-success-anomaly                                       |Removed field  |additional_info     |
|Parser        |exabeam-aa-kv-rule-trigger-success-anomaly                                       |New field    |event_time          |
|Parser        |exabeam-aa-kv-rule-trigger-success-anomaly                                       |New field    |mitre_labels        |
|Parser        |checkpoint-avanan-json-email-receive-securityevent                               |Changed regex     |alert_severity      |
|Parser        |checkpoint-avanan-json-email-receive-securityevent                               |Changed regex     |dest_email_address  |
|Parser        |checkpoint-avanan-json-email-receive-securityevent                               |Changed regex     |dest_email_domain   |
|Parser        |checkpoint-avanan-json-email-receive-securityevent                               |Changed regex     |email_recipients    |
|Parser        |checkpoint-avanan-json-email-send-securityevent                                  |Changed regex     |alert_severity      |
|Parser        |checkpoint-avanan-json-email-send-securityevent                                  |Changed regex     |dest_email_address  |
|Parser        |checkpoint-avanan-json-email-send-securityevent                                  |Changed regex     |dest_email_domain   |
|Parser        |checkpoint-avanan-json-email-send-securityevent                                  |Changed regex     |email_recipients    |
|Parser        |checkpoint-avanan-json-email-send-receive-phishing                               |Changed regex     |alert_severity      |
|Parser        |checkpoint-avanan-json-email-send-receive-phishing                               |Changed regex     |dest_email_address  |
|Parser        |checkpoint-avanan-json-email-send-receive-phishing                               |Changed regex     |dest_email_domain   |
|Parser        |checkpoint-avanan-json-email-send-receive-phishing                               |Changed regex     |email_recipients    |
|Parser        |checkpoint-avanan-json-alert-trigger-success-dlp                                 |Changed regex     |alert_severity      |
|Parser        |checkpoint-avanan-json-alert-trigger-success-dlp                                 |Changed regex     |dest_email_address  |
|Parser        |checkpoint-avanan-json-alert-trigger-success-dlp                                 |Changed regex     |dest_email_domain   |
|Parser        |checkpoint-avanan-json-alert-trigger-success-dlp                                 |Changed regex     |email_recipients    |
|Parser        |checkpoint-avanan-json-alert-trigger-success-securityeventmalware                |Changed regex     |alert_severity      |
|Parser        |checkpoint-avanan-json-alert-trigger-success-securityeventmalware                |Changed regex     |dest_email_address  |
|Parser        |checkpoint-avanan-json-alert-trigger-success-securityeventmalware                |Changed regex     |dest_email_domain   |
|Parser        |checkpoint-avanan-json-alert-trigger-success-securityeventmalware                |Changed regex     |email_recipients    |
|Parser        |checkpoint-avanan-json-email-receive-avanansecurityevent                         |Changed regex     |alert_severity      |
|Parser        |checkpoint-avanan-json-email-receive-avanansecurityevent                         |Changed regex     |dest_email_address  |
|Parser        |checkpoint-avanan-json-email-receive-avanansecurityevent                         |Changed regex     |dest_email_domain   |
|Parser        |checkpoint-avanan-json-email-receive-avanansecurityevent                         |Changed regex     |email_recipients    |
|Parser        |checkpoint-avanan-json-email-send-avanansecurityevent                            |Changed regex     |alert_severity      |
|Parser        |checkpoint-avanan-json-email-send-avanansecurityevent                            |Changed regex     |dest_email_address  |
|Parser        |checkpoint-avanan-json-email-send-avanansecurityevent                            |Changed regex     |dest_email_domain   |
|Parser        |checkpoint-avanan-json-email-send-avanansecurityevent                            |Changed regex     |email_recipients    |
|Parser        |checkpoint-avanan-json-alert-trigger-success-avanansecurityeventdlp              |Changed regex     |alert_severity      |
|Parser        |checkpoint-avanan-json-alert-trigger-success-avanansecurityeventdlp              |Changed regex     |dest_email_address  |
|Parser        |checkpoint-avanan-json-alert-trigger-success-avanansecurityeventdlp              |Changed regex     |dest_email_domain   |
|Parser        |checkpoint-avanan-json-alert-trigger-success-avanansecurityeventdlp              |Changed regex     |email_recipients    |
|Parser        |checkpoint-avanan-json-alert-trigger-success-avanansecurityeventmalware          |Changed regex     |alert_severity      |
|Parser        |checkpoint-avanan-json-alert-trigger-success-avanansecurityeventmalware          |Changed regex     |dest_email_address  |
|Parser        |checkpoint-avanan-json-alert-trigger-success-avanansecurityeventmalware          |Changed regex     |dest_email_domain   |
|Parser        |checkpoint-avanan-json-alert-trigger-success-avanansecurityeventmalware          |Changed regex     |email_recipients    |
|Parser        |microsoft-evsecurity-kv-ds-object-modify-success-4742                            |Changed fields|N/A                 |
|Parser        |microsoft-evsecurity-kv-ds-object-modify-success-4742                            |Removed field  |object              |
|Parser        |microsoft-evsecurity-kv-ds-object-modify-success-4742                            |New field    |account_name        |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-3                             |Changed fields|N/A                 |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-3                             |Removed field  |dest_host           |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-3                             |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-3                             |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-3                             |Changed regex     |src_host            |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-3                             |Changed regex     |src_port            |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-3                             |New field    |src_ip              |
|Parser        |microsoft-mssql-json-database-activity-success-dbactivity                        |changed              |Conditions          |
|Parser        |microsoft-evsecurity-xml-user-enable-success-4722                                |Added attribute      |DupFields           |
|Parser        |microsoft-evsecurity-xml-share-access-success-5140                               |Changed regex     |dest_host           |
|Parser        |microsoft-evsecurity-xml-share-access-success-5140                               |Changed regex     |host                |
|Parser        |microsoft-evsystem-str-service-create-success-7045                               |Changed regex     |dest_host           |
|Parser        |microsoft-evsystem-str-service-create-success-7045                               |Changed regex     |dest_ip             |
|Parser        |microsoft-evsystem-str-service-create-success-7045                               |Changed regex     |host                |
|Parser        |microsoft-evsecurity-xml-scheduled-task-create-success-4700                      |Added attribute      |DupFields           |
|Parser        |microsoft-evsecurity-xml-scheduled-task-create-success-4700-1                    |Added attribute      |DupFields           |
|Parser        |microsoft-evsecurity-xml-scheduled-task-create-success-4700-2                    |Added attribute      |DupFields           |
|Parser        |microsoft-evsecurity-xml-ds-object-modify-success-5136                           |Changed regex     |dest_host           |
|Parser        |microsoft-evsecurity-xml-ds-object-modify-success-5136                           |Changed regex     |host                |
|Parser        |microsoft-evsecurity-xml-user-password-reset-success-4724                        |Changed regex     |dest_host           |
|Parser        |microsoft-evsecurity-xml-user-password-reset-success-4724                        |Changed regex     |host                |
|Parser        |microsoft-evsecurity-xml-endpoint-login-4769                                     |Changed regex     |dest_host           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4771                         |Changed fields|N/A                 |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4771                         |Removed field  |dest_host           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4771                         |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4771                         |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4771                         |Changed regex     |src_host            |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4771                         |New field    |src_ip              |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4771                         |New field    |src_port            |
|Parser        |microsoft-evsecurity-cef-endpoint-login-fail-4771                                |Changed regex     |dest_ip             |
|Parser        |microsoft-evsecurity-cef-endpoint-login-fail-4771                                |Changed regex     |dest_port           |
|Parser        |microsoft-evsecurity-cef-endpoint-login-fail-4771                                |Changed regex     |src_ip              |
|Parser        |microsoft-evsecurity-cef-endpoint-login-fail-4771                                |Changed regex     |src_port            |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771                               |Changed fields|N/A                 |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771                               |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771                               |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771                               |New field    |src_ip              |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771                               |New field    |src_port            |
|Parser        |microsoft-evsecurity-json-registry-create-success-4657                           |Added attribute      |DupFields           |
|Parser        |microsoft-evsecurity-str-registry-create-success-4657                            |Changed regex     |host                |
|Parser        |microsoft-evsecurity-str-registry-create-success-4657                            |Added attribute      |DupFields           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4625                                 |Changed regex     |dest_host           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4625                                 |Changed regex     |dest_ip             |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4625                                 |Changed regex     |host                |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771-1                              |Changed fields|N/A                 |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771-1                              |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771-1                              |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771-1                              |New field    |src_ip              |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771-1                              |New field    |src_port            |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771                                |Changed fields|N/A                 |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771                                |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771                                |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771                                |New field    |src_ip              |
|Parser        |microsoft-evsecurity-xml-endpoint-login-fail-4771                                |New field    |src_port            |
|Parser        |microsoft-evsecurity-kv-endpoint-login-failed-4771-jp                            |Changed fields|N/A                 |
|Parser        |microsoft-evsecurity-kv-endpoint-login-failed-4771-jp                            |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-kv-endpoint-login-failed-4771-jp                            |New field    |src_ip              |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-2                               |Changed fields|N/A                 |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-2                               |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-2                               |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-2                               |New field    |src_ip              |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-2                               |New field    |src_port            |
|Parser        |microsoft-evsecurity-xml-registry-create-success-4657                            |Added attribute      |DupFields           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Changed fields|N/A                 |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Changed regex     |domain              |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Changed regex     |event_code          |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Changed regex     |host                |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Changed regex     |result_code         |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Changed regex     |user                |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |Changed regex     |user_sid            |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |New field    |src_ip              |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771                                 |New field    |src_port            |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-4                             |Changed fields|N/A                 |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-4                             |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-4                             |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-4                             |New field    |src_ip              |
|Parser        |microsoft-evsecurity-json-endpoint-login-fail-4771-4                             |New field    |src_port            |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-1                               |Changed fields|N/A                 |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-1                               |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-1                               |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-1                               |New field    |src_ip              |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-1                               |New field    |src_port            |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-3                               |Changed fields|N/A                 |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-3                               |Removed field  |dest_ip             |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-3                               |Removed field  |dest_port           |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-3                               |New field    |src_ip              |
|Parser        |microsoft-evsecurity-kv-endpoint-login-fail-4771-3                               |New field    |src_port            |
|Parser        |microsoft-evsecurity-kv-share-access-5145-3                                      |Changed regex     |file_dir            |
|Parser        |microsoft-evsecurity-kv-share-access-5145-3                                      |Changed regex     |file_ext            |
|Parser        |microsoft-evsecurity-kv-share-access-5145-3                                      |Changed regex     |file_name           |
|Parser        |cisco-duo-cef-vpn-login-fail-loginfailure                                        |Changed fields|N/A                 |
|Parser        |cisco-duo-cef-vpn-login-fail-loginfailure                                        |Removed field  |operation           |
|Parser        |cisco-duo-cef-vpn-login-fail-loginfailure                                        |New field    |factor              |
|Parser        |cisco-duo-cef-vpn-login-fail-loginfailure                                        |removed_attribute    |DupFields           |
|Parser        |cisco-duo-sk4-vpn-login-success-newenrollment                                    |Changed fields|N/A                 |
|Parser        |cisco-duo-sk4-vpn-login-success-newenrollment                                    |Removed field  |operation           |
|Parser        |cisco-duo-sk4-vpn-login-success-newenrollment                                    |New field    |factor              |
|Parser        |cisco-duo-kv-app-activity-success-userupdate                                     |Changed fields|N/A                 |
|Parser        |cisco-duo-kv-app-activity-success-userupdate                                     |Removed field  |action              |
|Parser        |cisco-duo-kv-app-activity-success-userupdate                                     |New field    |factor              |
|Parser        |cisco-duo-json-endpoint-authentication-ip                                        |Changed fields|N/A                 |
|Parser        |cisco-duo-json-endpoint-authentication-ip                                        |Removed field  |auth_method         |
|Parser        |cisco-duo-json-endpoint-authentication-ip                                        |New field    |factor              |
|Parser        |cisco-duo-json-endpoint-authentication-result-1                                  |Changed fields|N/A                 |
|Parser        |cisco-duo-json-endpoint-authentication-result-1                                  |Removed field  |auth_method         |
|Parser        |cisco-duo-json-endpoint-authentication-result-1                                  |New field    |factor              |
|Parser        |cisco-duo-json-app-login-success-adminlogin-1                                    |Changed fields|N/A                 |
|Parser        |cisco-duo-json-app-login-success-adminlogin-1                                    |Removed field  |action              |
|Parser        |cisco-duo-json-app-login-success-adminlogin-1                                    |New field    |factor              |
|Parser        |cisco-duo-kv-app-activity-success-sendenrollcode                                 |Changed fields|N/A                 |
|Parser        |cisco-duo-kv-app-activity-success-sendenrollcode                                 |Removed field  |action              |
|Parser        |cisco-duo-kv-app-activity-success-sendenrollcode                                 |New field    |factor              |
|Parser        |cisco-duo-json-app-activity-success-usercreate-1                                 |Changed fields|N/A                 |
|Parser        |cisco-duo-json-app-activity-success-usercreate-1                                 |Removed field  |action              |
|Parser        |cisco-duo-json-app-activity-success-usercreate-1                                 |New field    |factor              |
|Parser        |cisco-duo-json-app-activity-success-userpending                                  |Changed fields|N/A                 |
|Parser        |cisco-duo-json-app-activity-success-userpending                                  |Removed field  |action              |
|Parser        |cisco-duo-json-app-activity-success-userpending                                  |New field    |factor              |
|Parser        |cisco-duo-json-app-activity-success-phoneupdate                                  |Changed fields|N/A                 |
|Parser        |cisco-duo-json-app-activity-success-phoneupdate                                  |Removed field  |action              |
|Parser        |cisco-duo-json-app-activity-success-phoneupdate                                  |New field    |factor              |
|Parser        |microsoft-o365-sk4-file-write-success-filemodified                               |Changed regex     |src_ip              |
|Parser        |microsoft-o365-sk4-file-write-success-filemodified                               |Changed regex     |src_port            |
|Parser        |microsoft-o365-cef-app-login-success-user                                        |Changed regex     |user_agent          |
|Parser        |microsoft-o365-cef-app-file-success-displayname                                  |Changed fields|N/A                 |
|Parser        |microsoft-o365-cef-app-file-success-displayname                                  |New field    |result_reason       |
|Parser        |microsoft-o365-mix-file-success-workload                                         |Changed regex     |src_ip              |
|Parser        |microsoft-o365-mix-file-success-workload                                         |Changed regex     |src_port            |
|Parser        |microsoft-o365-sk4-file-app-userkey                                              |Changed regex     |src_ip              |
|Parser        |microsoft-o365-sk4-file-app-userkey                                              |Changed regex     |src_port            |
|Parser        |microsoft-o365-sk4-file-app-userkey-1                                            |Changed regex     |src_ip              |
|Parser        |microsoft-o365-sk4-file-app-userkey-1                                            |Changed regex     |src_port            |
|Parser        |microsoft-o365-json-email-receive-success-emailreceive                           |Changed regex     |external_address    |
|Parser        |microsoft-azureadip-json-alert-trigger-success-graphsecurityalert                |Changed regex     |src_ip              |
|Parser        |microsoft-azureadip-json-alert-trigger-success-graphsecurityalert                |Changed regex     |src_port            |
|Parser        |microsoft-azureadip-json-alert-trigger-success-graphsecurityalert                |Changed regex     |time                |
|Parser        |microsoft-mcas-json-alert-trigger-success-velocity                               |Changed regex     |src_ip              |
|Parser        |microsoft-mcas-json-alert-trigger-success-velocity                               |Changed regex     |src_port            |
|Parser        |microsoft-mcas-json-alert-trigger-success-velocity                               |Changed regex     |time                |
|Parser        |microsoft-mcas-json-alert-trigger-success-login                                  |Changed regex     |src_ip              |
|Parser        |microsoft-mcas-json-alert-trigger-success-login                                  |Changed regex     |src_port            |
|Parser        |microsoft-mcas-json-alert-trigger-success-login                                  |Changed regex     |time                |
|Parser        |microsoft-mcas-json-alert-trigger-success-download                               |Changed regex     |src_ip              |
|Parser        |microsoft-mcas-json-alert-trigger-success-download                               |Changed regex     |src_port            |
|Parser        |microsoft-mcas-json-alert-trigger-success-download                               |Changed regex     |time                |
|Parser        |microsoft-mcas-json-alert-trigger-success-ransomware                             |Changed regex     |src_ip              |
|Parser        |microsoft-mcas-json-alert-trigger-success-ransomware                             |Changed regex     |src_port            |
|Parser        |microsoft-mcas-json-alert-trigger-success-ransomware                             |Changed regex     |time                |
|Parser        |microsoft-azureatp-json-alert-trigger-success-remoteexecutionsecurityalert-1     |Changed regex     |src_ip              |
|Parser        |microsoft-azureatp-json-alert-trigger-success-remoteexecutionsecurityalert-1     |Changed regex     |src_port            |
|Parser        |microsoft-azureatp-json-alert-trigger-success-remoteexecutionsecurityalert-1     |Changed regex     |time                |
|Parser        |microsoft-azureatp-json-alert-trigger-success-netlogonbypasssecurityalert-1      |Changed regex     |src_ip              |
|Parser        |microsoft-azureatp-json-alert-trigger-success-netlogonbypasssecurityalert-1      |Changed regex     |src_port            |
|Parser        |microsoft-azureatp-json-alert-trigger-success-netlogonbypasssecurityalert-1      |Changed regex     |time                |
|Parser        |microsoft-defenderep-json-alert-trigger-success-suspiciousactivity               |Changed regex     |src_ip              |
|Parser        |microsoft-defenderep-json-alert-trigger-success-suspiciousactivity               |Changed regex     |src_port            |
|Parser        |microsoft-defenderep-json-alert-trigger-success-suspiciousactivity               |Changed regex     |time                |
|Parser        |microsoft-defenderep-json-alert-trigger-success-collection                       |Changed regex     |src_ip              |
|Parser        |microsoft-defenderep-json-alert-trigger-success-collection                       |Changed regex     |src_port            |
|Parser        |microsoft-defenderep-json-alert-trigger-success-collection                       |Changed regex     |time                |
|Parser        |microsoft-defenderep-json-alert-trigger-success-malware-1                        |Changed regex     |src_ip              |
|Parser        |microsoft-defenderep-json-alert-trigger-success-malware-1                        |Changed regex     |src_port            |
|Parser        |microsoft-defenderep-json-alert-trigger-success-malware-1                        |Changed regex     |time                |
|Parser        |microsoft-defenderep-json-alert-trigger-success-lateralmovement-1                |Changed regex     |src_ip              |
|Parser        |microsoft-defenderep-json-alert-trigger-success-lateralmovement-1                |Changed regex     |src_port            |
|Parser        |microsoft-defenderep-json-alert-trigger-success-lateralmovement-1                |Changed regex     |time                |
|Parser        |microsoft-defenderep-json-alert-trigger-success-unwantedsoftware                 |Changed regex     |src_ip              |
|Parser        |microsoft-defenderep-json-alert-trigger-success-unwantedsoftware                 |Changed regex     |src_port            |
|Parser        |microsoft-defenderep-json-alert-trigger-success-unwantedsoftware                 |Changed regex     |time                |
|Parser        |microsoft-defenderep-json-alert-trigger-success-persistence-1                    |Changed regex     |src_ip              |
|Parser        |microsoft-defenderep-json-alert-trigger-success-persistence-1                    |Changed regex     |src_port            |
|Parser        |microsoft-defenderep-json-alert-trigger-success-persistence-1                    |Changed regex     |time                |
|Parser        |microsoft-defenderep-json-alert-trigger-success-exploit-1                        |Changed regex     |src_ip              |
|Parser        |microsoft-defenderep-json-alert-trigger-success-exploit-1                        |Changed regex     |src_port            |
|Parser        |microsoft-defenderep-json-alert-trigger-success-exploit-1                        |Changed regex     |time                |
|Parser        |crowdstrike-falcon-mix-file-write-success-directorycreate                        |Changed regex     |file_dir            |
|Parser        |crowdstrike-falcon-mix-file-write-success-directorycreate                        |Changed regex     |file_ext            |
|Parser        |crowdstrike-falcon-mix-file-write-success-directorycreate                        |Changed regex     |file_name           |
|Parser        |crowdstrike-falcon-mix-file-write-success-directorycreate                        |Changed regex     |file_path           |
|Parser        |cisco-duo-kv-app-login-success-adminlogin                                        |Changed fields|N/A                 |
|Parser        |cisco-duo-kv-app-login-success-adminlogin                                        |Removed field  |action              |
|Parser        |cisco-duo-kv-app-login-success-adminlogin                                        |New field    |factor              |
|Parser        |vmware-esxi-str-endpoint-login-success-loggedin                                  |Changed regex     |event_name          |
|Parser        |vmware-esxi-str-endpoint-login-success-loggedin                                  |Changed regex     |host                |
|Parser        |vmware-esxi-str-endpoint-login-success-loggedin                                  |Changed regex     |operation           |
|Parser        |vmware-esxi-str-endpoint-login-success-loggedin                                  |Changed regex     |time                |
|Parser        |zscaler-ia-cef-http-session-spriv                                                |Changed regex     |top_domain          |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Changed fields|N/A                 |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Changed regex     |additional_info     |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Changed regex     |email_address       |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Removed field  |event_name          |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Changed regex     |operation           |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Changed regex     |result              |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Changed regex     |src_ip              |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Changed regex     |src_port            |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Changed regex     |time                |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |Changed regex     |user                |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |New field    |app_type            |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |New field    |object              |
|Parser        |zscaler-ia-csv-app-activity-success-policyupdate                                 |New field    |resource            |
|Parser        |symantec-dlp-kv-email-send-incident                                              |Changed regex     |file_ext            |
|Parser        |symantec-dlp-kv-email-send-incident                                              |Changed regex     |file_name           |
|Parser        |f5-apm-str-vpn-success-01490005                                                  |Changed fields|N/A                 |
|Parser        |f5-apm-str-vpn-success-01490005                                                  |New field    |host                |
|Parser        |proofpoint-tappod-json-email-send-receive-rcpts                                  |Changed regex     |dest_email_address  |
|Parser        |proofpoint-tappod-json-email-send-receive-rcpts                                  |Changed regex     |email_recipients    |
|Parser        |proofpoint-tappod-json-email-send-receive-rcpts                                  |Changed regex     |email_subject       |
|Parser        |pingidentity-pi-kv-app-login-success-sso                                         |Changed fields|N/A                 |
|Parser        |pingidentity-pi-kv-app-login-success-sso                                         |Changed regex     |email_address       |
|Parser        |pingidentity-pi-kv-app-login-success-sso                                         |Changed regex     |user                |
|Parser        |pingidentity-pi-kv-app-login-success-sso                                         |New field    |email_domain        |
|Parser        |unix-unix-str-endpoint-login-fail-unablesshd                                     |Changed regex     |dest_host           |
|Parser        |unix-unix-str-endpoint-login-fail-unablesshd                                     |Changed regex     |dest_ip             |
|Parser        |unix-unix-str-endpoint-login-fail-unablesshd                                     |Changed regex     |host                |
|Parser        |unix-unix-str-endpoint-login-fail-unablesshd                                     |Changed regex     |src_host            |
|Parser        |unix-unix-str-endpoint-login-fail-unablesshd                                     |Changed regex     |src_ip              |
|Parser        |unix-unix-str-endpoint-login-fail-invaliduser                                    |Changed regex     |host                |
|Parser        |unix-unix-str-endpoint-login-fail-manyauthfail                                   |Changed regex     |src_ip              |
|Parser        |unix-unix-mix-ssh-traffic-success-ssh2accepted                                   |Changed regex     |additional_info     |
|Parser        |unix-unix-mix-ssh-traffic-success-ssh2accepted                                   |Changed regex     |dest_host           |
|Parser        |unix-unix-mix-ssh-traffic-success-ssh2accepted                                   |Changed regex     |host                |
|Parser        |unix-unix-mix-ssh-traffic-success-ssh2accepted                                   |Changed regex     |login_id            |
|Parser        |unix-unix-str-endpoint-login-sshdconnectionfrom                                  |Changed fields|N/A                 |
|Parser        |unix-unix-str-endpoint-login-sshdconnectionfrom                                  |Removed field  |dest_ip             |
|Parser        |unix-unix-str-endpoint-login-sshdconnectionfrom                                  |Removed field  |dest_port           |
|Parser        |unix-unix-str-endpoint-login-sshdconnectionfrom                                  |Changed regex     |host                |
|Parser        |unix-unix-str-endpoint-login-sshdconnectionfrom                                  |New field    |src_ip              |
|Parser        |unix-unix-str-endpoint-login-sshdconnectionfrom                                  |New field    |src_port            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Changed fields|N/A                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Changed regex     |alert_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Changed regex     |alert_type          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Changed regex     |dest_ip             |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Changed regex     |dest_port           |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Changed regex     |email_address       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Changed regex     |event_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Changed regex     |instance_id         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Changed regex     |location_city       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Changed regex     |src_ip              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Changed regex     |user                |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |New field    |alert_id            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |New field    |app                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |New field    |aws_account         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |New field    |result              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |New field    |src_port            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1                        |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Changed fields|N/A                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Changed regex     |alert_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Changed regex     |alert_type          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Changed regex     |dest_ip             |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Changed regex     |dest_port           |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Changed regex     |email_address       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Changed regex     |event_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Changed regex     |instance_id         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Changed regex     |location_city       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Changed regex     |src_ip              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Changed regex     |user                |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |New field    |alert_id            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |New field    |app                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |New field    |aws_account         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |New field    |result              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |New field    |src_port            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-toripcaller                        |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Changed fields|N/A                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Changed regex     |alert_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Changed regex     |alert_type          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Changed regex     |dest_ip             |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Changed regex     |dest_port           |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Changed regex     |email_address       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Changed regex     |event_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Changed regex     |instance_id         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Changed regex     |location_city       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Changed regex     |src_ip              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Changed regex     |user                |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |New field    |alert_id            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |New field    |app                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |New field    |aws_account         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |New field    |result              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |New field    |src_port            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-guardduty-2                        |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Changed fields|N/A                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Changed regex     |alert_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Changed regex     |alert_type          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Changed regex     |dest_ip             |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Changed regex     |dest_port           |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Changed regex     |email_address       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Changed regex     |event_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Changed regex     |instance_id         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Changed regex     |location_city       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Changed regex     |src_ip              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Changed regex     |user                |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |New field    |alert_id            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |New field    |app                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |New field    |aws_account         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |New field    |result              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |New field    |src_port            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage                |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Changed fields|N/A                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Changed regex     |alert_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Changed regex     |alert_type          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Changed regex     |dest_ip             |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Changed regex     |dest_port           |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Changed regex     |email_address       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Changed regex     |event_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Changed regex     |instance_id         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Changed regex     |location_city       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Changed regex     |src_ip              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Changed regex     |user                |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |New field    |alert_id            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |New field    |app                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |New field    |aws_account         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |New field    |result              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |New field    |src_port            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior                  |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Changed fields|N/A                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Changed regex     |alert_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Changed regex     |alert_type          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Changed regex     |dest_ip             |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Changed regex     |dest_port           |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Changed regex     |email_address       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Changed regex     |event_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Changed regex     |instance_id         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Changed regex     |location_city       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Changed regex     |src_ip              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Changed regex     |user                |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |New field    |alert_id            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |New field    |app                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |New field    |aws_account         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |New field    |result              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |New field    |src_port            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1                    |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Changed fields|N/A                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Changed regex     |alert_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Changed regex     |alert_type          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Changed regex     |dest_ip             |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Changed regex     |dest_port           |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Changed regex     |email_address       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Changed regex     |event_name          |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Changed regex     |instance_id         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Changed regex     |location_city       |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Changed regex     |src_ip              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Changed regex     |user                |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |New field    |alert_id            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |New field    |app                 |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |New field    |aws_account         |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |New field    |result              |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |New field    |src_port            |
|Parser        |amazon-awsguardduty-sk4-alert-trigger-success-bucketblockpublicaccessdisabled    |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Changed fields|N/A                 |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Changed regex     |alert_name          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Changed regex     |alert_type          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Changed regex     |dest_ip             |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Changed regex     |dest_port           |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Changed regex     |email_address       |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Changed regex     |event_name          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Changed regex     |instance_id         |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Changed regex     |location_city       |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Changed regex     |src_ip              |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Changed regex     |user                |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|New field    |alert_id            |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|New field    |app                 |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|New field    |aws_account         |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|New field    |result              |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|New field    |src_port            |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport|Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Changed fields|N/A                 |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Changed regex     |alert_name          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Changed regex     |alert_type          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Changed regex     |dest_ip             |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Changed regex     |dest_port           |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Changed regex     |email_address       |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Changed regex     |event_name          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Changed regex     |instance_id         |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Changed regex     |location_city       |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Changed regex     |src_ip              |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Changed regex     |user                |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |New field    |alert_id            |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |New field    |app                 |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |New field    |aws_account         |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |New field    |result              |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |New field    |src_port            |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-sshbruteforce                     |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Changed fields|N/A                 |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Changed regex     |alert_name          |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Changed regex     |alert_type          |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Changed regex     |dest_ip             |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Changed regex     |dest_port           |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Changed regex     |email_address       |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Changed regex     |event_name          |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Changed regex     |instance_id         |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Changed regex     |location_city       |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Changed regex     |src_ip              |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Changed regex     |user                |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |New field    |alert_id            |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |New field    |app                 |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |New field    |aws_account         |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |New field    |result              |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |New field    |src_port            |
|Parser        |amazon-awsguardduty-json-database-login-success-rdssuccessfullogin               |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Changed fields|N/A                 |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Changed regex     |alert_name          |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Changed regex     |alert_type          |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Changed regex     |dest_ip             |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Changed regex     |dest_port           |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Changed regex     |email_address       |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Changed regex     |event_name          |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Changed regex     |instance_id         |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Changed regex     |location_city       |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Changed regex     |src_ip              |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Changed regex     |user                |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |New field    |alert_id            |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |New field    |app                 |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |New field    |aws_account         |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |New field    |result              |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |New field    |src_port            |
|Parser        |amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin        |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Changed fields|N/A                 |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Changed regex     |alert_name          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Changed regex     |alert_type          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Changed regex     |dest_ip             |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Changed regex     |dest_port           |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Changed regex     |email_address       |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Changed regex     |event_name          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Changed regex     |instance_id         |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Changed regex     |location_city       |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Changed regex     |src_ip              |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Changed regex     |user                |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |New field    |alert_id            |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |New field    |app                 |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |New field    |aws_account         |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |New field    |result              |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |New field    |src_port            |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod               |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Changed fields|N/A                 |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Changed regex     |additional_info     |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Changed regex     |alert_name          |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Changed regex     |alert_severity      |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Changed regex     |alert_type          |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Removed field  |dest_host           |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Changed regex     |dest_ip             |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Changed regex     |dest_port           |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Changed regex     |email_address       |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Changed regex     |event_name          |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Changed regex     |src_ip              |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Changed regex     |src_port            |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Changed regex     |time                |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Changed regex     |user                |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |New field    |account_id          |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |New field    |domain              |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |New field    |email_domain        |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |New field    |instance_id         |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |New field    |location_city       |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |New field    |object              |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |New field    |region              |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |New field    |resource_type       |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |New field    |user_type           |
|Parser        |amazon-awsguardduty-cef-alert-trigger-success-catsecurity                        |Added attribute      |ExtractionType      |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Changed fields|N/A                 |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Changed regex     |alert_name          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Changed regex     |alert_type          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Changed regex     |dest_ip             |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Changed regex     |dest_port           |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Changed regex     |email_address       |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Changed regex     |event_name          |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Changed regex     |instance_id         |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Changed regex     |location_city       |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Changed regex     |src_ip              |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Changed regex     |user                |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |New field    |alert_id            |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |New field    |app                 |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |New field    |aws_account         |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |New field    |result              |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |New field    |src_port            |
|Parser        |amazon-awsguardduty-json-alert-trigger-success-catchall                          |Added attribute      |ExtractionType      |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |Changed fields|N/A                 |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |Changed regex     |account_domain      |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |Changed regex     |account_name        |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |Changed regex     |src_ip              |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |Changed regex     |src_port            |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |Changed regex     |time                |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |Changed regex     |user                |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |New field    |domain              |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |New field    |src_host            |
|Parser        |microsoft-azuremon-sk4-app-authentication-accounttokenlogin                      |Changed regex     |src_ip              |
|Parser        |microsoft-azuremon-sk4-app-authentication-accounttokenlogin                      |Changed regex     |src_port            |
|Parser        |microsoft-azuremon-sk4-app-logout-sshlogout                                      |Changed regex     |src_ip              |
|Parser        |microsoft-azuremon-sk4-app-logout-sshlogout                                      |Changed regex     |src_port            |
|Parser        |microsoft-azuremon-sk4-secret-read-getsecret                                     |Changed regex     |src_ip              |
|Parser        |microsoft-azuremon-sk4-secret-read-getsecret                                     |Changed regex     |src_port            |
|Parser        |microsoft-azuremon-sk4-app-notification-clusterstartresult                       |Changed regex     |src_ip              |
|Parser        |microsoft-azuremon-sk4-app-notification-clusterstartresult                       |Changed regex     |src_port            |
|Parser        |microsoft-azuremon-sk4-app-notification-clusterstart                             |Changed regex     |src_ip              |
|Parser        |microsoft-azuremon-sk4-app-notification-clusterstart                             |Changed regex     |src_port            |
|Parser        |pan-ngfw-json-app-activity-success-subtype                                       |Changed regex     |host                |
|Parser        |pan-ngfw-json-alert-trigger-success-hipmatch                                     |Changed regex     |host                |
|Parser        |pan-ngfw-json-app-notification-success-userid                                    |Changed regex     |host                |
|Parser        |pan-ngfw-json-vpn-authentication-success-subtypevpn                              |Changed regex     |host                |
|Parser        |pan-ngfw-json-app-notification-success-dhcp                                      |Changed regex     |host                |
|Parser        |vmware-esxi-str-app-activity-hostd                                               |Changed regex     |domain              |
|Parser        |vmware-esxi-str-app-activity-hostd                                               |Changed regex     |user                |
|Parser        |f5-f-kv-app-activity-common                                                      |Changed fields|N/A                 |
|Parser        |f5-f-kv-app-activity-common                                                      |New field    |host                |
|Parser        |unix-unix-str-endpoint-authentication-check                                      |Changed regex     |host                |
|Parser        |unix-unix-str-network-start-snmpd                                                |Changed regex     |dest_ip             |
|Parser        |unix-unix-str-network-start-snmpd                                                |Changed regex     |dest_port           |
|Parser        |unix-unix-str-network-start-snmpd                                                |Changed regex     |event_name          |
|Parser        |unix-unix-str-network-start-snmpd                                                |Changed regex     |host                |
|Parser        |unix-unix-str-network-start-snmpd                                                |Changed regex     |process_id          |
|Parser        |unix-unix-str-network-start-snmpd                                                |Changed regex     |protocol            |
|Parser        |unix-unix-str-network-start-snmpd                                                |Changed regex     |src_ip              |
|Parser        |unix-unix-str-network-start-snmpd                                                |Changed regex     |src_port            |
|Parser        |unix-unix-str-endpoint-activity-systemd                                          |Changed regex     |host                |
|Parser        |unix-unix-str-endpoint-logout-sshdreceiveddisconnect                             |Changed regex     |host                |
|Parser        |unix-unix-str-endpoint-logout-sshdconnectionclosed                               |Changed regex     |host                |
|Parser        |unix-unix-str-endpoint-logout-disconnected                                       |Changed regex     |host                |
|Parser        |unix-unix-str-endpoint-activity-crond                                            |Changed regex     |host                |
|Parser        |airlock-allowlisting-json-app-activity-success-fileactivity                      |Changed fields|N/A                 |
|Parser        |airlock-allowlisting-json-app-activity-success-fileactivity                      |New field    |process_command_line|
|Parser        |airlock-allowlisting-json-app-activity-success-fileactivity                      |Added attribute      |DupFields           |
|Parser        |microsoft-azuresc-json-alert-trigger-success-security                            |New Parser         |N/A                 |
|Parser        |microsoft-defenderep-json-alert-trigger-success-persistence-2                    |New Parser         |N/A                 |
|Parser        |azure-azuread-json-user-password-modify-success-selfservice-1                    |New Parser         |N/A                 |
|Parser        |microsoft-azure-json-app-activity-adduser                                        |New Parser         |N/A                 |
|Parser        |microsoft-azure-json-app-activity-deleteuser                                     |New Parser         |N/A                 |
|Parser        |microsoft-azure-json-app-activity-changeuserlicense                              |New Parser         |N/A                 |
|Parser        |microsoft-o365-json-app-file-success-inviteexternaluser                          |New Parser         |N/A                 |
|Parser        |microsoft-azure-json-group-member-remove-success-removefromgroup                 |New Parser         |N/A                 |
|Parser        |pan-ngfw-json-endpoint-authentication-success-authsuccess                        |New Parser         |N/A                 |
|Parser        |pan-ngfw-json-endpoint-authentication-fail-authfail                              |New Parser         |N/A                 |
|Parser        |pan-ngfw-json-endpoint-authentication-success-signvalidated                      |New Parser         |N/A                 |
|Parser        |zscaler-ia-csv-app-activity-success-nssupdate                                    |New Parser         |N/A                 |
|Parser        |zscaler-ia-csv-app-activity-success-nssdelete                                    |New Parser         |N/A                 |
|Parser        |pingidentity-pi-json-app-authentication-fail-authfail                            |New Parser         |N/A                 |
|Parser        |pingidentity-pi-json-app-login-success-ssoidp                                    |New Parser         |N/A                 |
|Parser        |pingidentity-pi-json-app-login-ssosession                                        |New Parser         |N/A                 |
|Parser        |pingidentity-pi-json-app-activity-success-deviceadded                            |New Parser         |N/A                 |
|Parser        |pingidentity-pi-json-app-activity-success-deviceunpaired                         |New Parser         |N/A                 |
|Parser        |microsoft-evsecurity-xml-endpoint-notification-success-4802                      |New Parser         |N/A                 |
|Parser        |pan-ngfw-json-app-notification-success-auth                                      |New Parser         |N/A                 |
|Parser        |pan-ngfw-json-app-activity-success-samlidpactivity                               |New Parser         |N/A                 |
|Parser        |crowdstrike-falcon-json-network-traffic-success-networkreceiveaccept             |New Parser         |N/A                 |
|Parser        |pingidentity-pingone-json-user-role-assign-success-roleassignmentcreated         |New Parser         |N/A                 |
|Parser        |pingidentity-pingone-json-user-role-revoke-success-roleassignmentdeleted         |New Parser         |N/A                 |
|Parser        |pingidentity-pingone-json-user-modify-success-userupdated                        |New Parser         |N/A                 |
|ParserTemplate|json-avanan-security-alert                                                       |Changed regex     |alert_severity      |
|ParserTemplate|json-avanan-security-alert                                                       |Changed regex     |dest_email_address  |
|ParserTemplate|json-avanan-security-alert                                                       |Changed regex     |dest_email_domain   |
|ParserTemplate|json-avanan-security-alert                                                       |Changed regex     |email_recipients    |
|ParserTemplate|json-pan-system                                                                  |Changed regex     |host                |
|ParserTemplate|q-duo-app-activity                                                               |Changed fields|N/A                 |
|ParserTemplate|q-duo-app-activity                                                               |Removed field  |action              |
|ParserTemplate|q-duo-app-activity                                                               |New field    |factor              |
|ParserTemplate|o365-file-app-activity                                                           |Changed regex     |src_ip              |
|ParserTemplate|o365-file-app-activity                                                           |Changed regex     |src_port            |
|ParserTemplate|defender-atp-security-alert-events                                               |Changed regex     |src_ip              |
|ParserTemplate|defender-atp-security-alert-events                                               |Changed regex     |src_port            |
|ParserTemplate|defender-atp-security-alert-events                                               |Changed regex     |time                |
|ParserTemplate|ping-events-1                                                                    |removed_attribute    |ParserVersion       |
|ParserTemplate|zscaler-ia-csv-events                                                            |New Parser_template|N/A                 |
|ParserTemplate|microsoft-azuread-json-events                                                    |New Parser_template|N/A                 |
|ParserTemplate|json-aws-guardduty-security-alert-template                                       |New Parser_template|N/A                 |
|ParserTemplate|json-ping-events                                                                 |New Parser_template|N/A                 |
|ParserTemplate|pingone-events                                                                   |New Parser_template|N/A                 |
|Parser        |vmware-esxi-str-endpoint-login-success-loggedin                                  |edit_attribute       |activity_type       |
|Parser        |vmware-esxi-str-endpoint-login-success-loggedin                                  |edit_attribute       |legacy_activity_type|
|Parser        |vmware-esxi-str-endpoint-login-success-loggedin-1                                |edit_attribute       |activity_type       |
|Parser        |vmware-esxi-str-endpoint-login-success-loggedin-1                                |edit_attribute       |legacy_activity_type|
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |edit_attribute       |activity_type       |
|Parser        |beyondtrust-bi-cef-user-create-success-add                                       |edit_attribute       |legacy_activity_type|
