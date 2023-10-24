#### Parser Content
```Java
{
Name = "microsoft-windows-json-endpoint-login-authentication"
Conditions = [
""""service":"sso""""
""""authentication":{"""
]
ParserVersion = "v1.0.0"

account-password-activity.Fields}[
	"""<EventID>({event_code}30009)</EventID>"""

  ]
 },
${MicrosoftParserTemplates.account-password-activity}{
  Name = microsoft-azuread-xml-user-password-reset-success-30029
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>30029</EventID>""","""'Microsoft-AzureADPasswordProtection-DCAgent'""", """ UserName:""" ]
  Fields = ${MicrosoftParserTemplates.account-password-activity.Fields}[
      """<EventID>({event_code}30029)</EventID>"""
  ]
 },
{
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Fields = [
"""({time}\d+-\d+-\d+T\d+:\d+:\d+).+\sLogType"""
"""EventID="+({event_code}\d+)""""
"""Opcode.+ProcessName ="+(-|({process_path}({process_dir}(:?[\w:]+)?[^.]+[\\\/]+))({process_name}[^"]+))""""
"""ServiceName ="+({service_name}[^"]+)""""
"""ServiceType="+({service_type}[^"]+)""""
"""ServiceAccount="+({account_name}[^"]+)""""
"""SubjectUserName ="+(-|({user}[\w\.\-]{1,40}\$?))""""
"""SubjectDomainName ="+(-|({domain}[^"]+))""""
"""SubjectLogonId="+({login_id}[^"]+)""""
"""ProviderGuid="+({process_guid}[^"]+)""""
"""CommandLine="+({process_command_line}[^"]+)""""
"""SubjectUserSid="+({user_sid}[^"]+)""""
"""SubjectUserName ="+(-|({user}[\w\.\-]{1,40}\$?))""""
"""ObjectServer="+({object_server}[^"]+)""""
"""ProcessId="+({process_id}[^"]+)""""
"""Computer="+({dest_host}[\w\-.]+)""""
"""TargetDomainName ="+(-|({dest_domain}[^"]+))""""
"""TargetUserName ="+(-|({dest_user}[^"]+))""""
"""TargetLogonId="+({dest_user_sid}[^"]+)""""
"""TargetUserSid="+({dest_user_sid}[^"]+)""""
"""ExecutionProcessID="+({process_id}d+)""""
"""FailureReason="+({failure_reason}[^"]+)""""
"""WorkstationName ="+(-|({workstation}[^"]+))""""
"""MemberName ="+({user_dn}[^"]+)""""
"""MemberSid="+({account_id}[^"]+)""""
"""LogonType="+({login_type}\d+)""""
"""SubStatus="+({result_code}[^"]+)""""
"""LogonProcessName ="({auth_process}[^"]+)""""
"""KeyLength="({key_length}\d+)""""
"""AuthenticationPackageName ="({auth_package}[^"]+)""""
"""IpAddress="(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""""
]
DupFields = [
"dest_host->host"
]
Name = "microsoft-evsecurity-kv-user-password-reset-success-4724-1"
Conditions = [
"""LogType="WLS""""
"""EventID="4724""""
]
ParserVersion = "v1.0.0"
},
{
Vendor = "Microsoft"
Product = "Microsoft CAS"
TimeFormat = "epoch"
Fields = [
"""\|SIEM_Agent\|[^\|]*\|[^\|]*\|({operation}[^\|]+)\|"""
"""\|SIEM_Agent\|[^\|]*\|({event_name}[^\|]+)\|"""
"""\Wrt=({time}\d{13})"""
"""\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\WdestinationServiceName =({app}.+?)\s+(\w+=|$)"""
"""\Wsuser=({user}[\w\.\-]{1,40}\$?)\s+(\w+=|$)"""
"""\Wsuser=({email_address}[^@\s]+@[^@\s]+)\s+(\w+=|$)"""
"""\Wc6a1=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
"""\Wmsg=({additional_info}.*?)\s+(\w+=|$)"""
]
Name = "microsoft-mcas-cef-user-password-reset-success-resetpassword"
Conditions = [
"""CEF:"""
"""|MCAS|SIEM_Agent|"""
"""|Reset password|"""
]
ParserVersion = "v1.0.0"
},
{
Name = "microsoft-evsecurity-json-user-password-reset-success-4724-3"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy H:mm:ss a"
Conditions = [
""""InstanceId":"4724""""
]
Fields = [
"""({event_name}An attempt was made to reset an account's password)"""
""""MachineName":"({host}[\w\-.]+)"""
""""TimeGenerated":"({time}[^"]*)"""
""""InstanceId":"({event_code}[^"]+)"""
""""4":"({user}[\w\.\-]{1,40}\$?)"""
""""5":"({domain}[^"]+)"""
""""6":"({login_id}[^"]+)"""
""""3":"({user_sid}[^"]+)"""
""""2":"({dest_user_sid}[^"]+)"""
""""0":"({dest_user}[^"]+)"""
""""1":"({dest_domain}[^"]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"
},


{
Name = "microsoft-evsecurity-kv-user-privilege-use-success-data"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
Conditions = [
"""Exabeam Windows 4674"""
"""summary_windows_4674_data"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+[+-]\d+)"""
"""({event_code}4764)"""
"""summary_windows_4674_data=\"+\d+:\d+:\d+\s*\d+-\d+-\d+:::(-|({host}[\w\-.]+))?:::(-|({event_code}[^:::]+))?:::(-|({result}[^:::]+))?:::(-|({process_path}.+?))?:::(-|({process_dir}.+?))?:::(-|({process_name}.+?))?:::(-|({user}[\w\.\-]{1,40}\$?))?:::(-|({domain}[^:::]+))?:::(-|({login_id}[^:::]+))?:::(-|({object_server}[^:::]+))?:::(-|({object_type}[^:::]+))?:::(-|({object}.+?))?:::(-|({access}[^:::]+))?:::(-|({privileges}[^:::]+))?:::"""
]
DupFields = [
"host->dest_host"
"process_dir->directory"
]
ParserVersion = "v1.0.0"
},

{
Vendor = "SimpleSAMLphp"
Product = "SimpleSAMLphp"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Fields = [
""""@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
""""service":".+?","host":"({host}[^"]+)"""
""""host":"({host}[^"]+)","authentication"""
""""host":"({host}[^"]+)","service":""""
""""host":"({host}[^"]+)","ad""""
""""host":"({host}[^"]+)","index""""
""""user":\{[^\}]*?"uid":"({user}[\w\.\-]{1,40}\$?)"""
""""country_code2":"({src_external_country}[^"]+)"""
""""domain":"({domain}[^"]+)"""
""""source":\{([^\}]*?\{([^\}]*?\{[^\{\}]*?\})*[^\}]*?\})*[^\}]*?"host":"({src_host}[^"]+)"""
""""source":\{([^\}]*?\{([^\}]*?\{[^\{\}]*?\})*[^\}]*?\})*[^\}]*?"ipv4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""destination":\{([^\}]*?\{([^\}]*?\{[^\{\}]*?\})*[^\}]*?\})*[^\}]*?"host":"({dest_host}[\w\-.]+)"""
""""destination":\{([^\}]*?\{([^\}]*?\{[^\{\}]*?\})*[^\}]*?\})*[^\}]*?"ipv4":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""logon-type":({login_type}\d+)"""
""""logon-id":"({login_id}[^"]+)"""
""""event-type":"({result}[^"]+)"""
""""event-id":({event_code}\d+)"""
""""message":"({event_name}[^"]+)"""
""""user-sid":"({user_sid}[^"]+)"""
""""status":"({result_code}[^"]+)"""
""""service-name":"({dest_host}[\w\-.]+\$)"""
""""service-name":"({service_name}[^"]+)"""
"""auth-package":"({auth_package}[^"]+)""""
"""workstation-name":"(-|({src_host_windows}[^"]+))""""
""""key":"({result_reason}[^"]+)"""
""""status":"({result}[^"]+)"""
""""environment":"({realm}[^"]+)"""
""""host":"({host}[^"]+)","@version""""
]
Name = "microsoft-windows-json-endpoint-login-authentication"
Conditions = [
""""service":"sso""""
""""authentication":{"""
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-windows-str-user-privilege-use-success-privileged"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""     578     """
"""Privileged object operation:"""
]
Fields = [
"""({event_name}Privileged object operation)"""
"""\s+(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)\s+"""
"""\s+(Information|Audit Success|Success Audit)\s+({host}[\w\-.]+)"""
"""(?:Information|Audit Success|Success Audit).+?Primary User Name:\s+({user}[\w\.\-]{1,40}\$?)\s+Primary Domain"""
"""({event_code}578)"""
"""Security\t([^\s]+\t){2}({result}.+?)\t"""
"""\s+Primary Domain:\s+({domain}[^\s]+)"""
"""\s+Primary Logon ID:\s+\([^,]+,({login_id}[^)]+)"""
"""\s+Object Server:\s+(?:-|({object_server}.+?))\s+Object Handle"""
"""\s+Privileges:\s+({privileges}.+?)\s+\d+"""
"""\s+({ownership_privilege}SeTakeOwnershipPrivilege)"""
"""\s+({environment_privilege}SeSystemEnvironmentPrivilege)"""
"""\s+({debug_privilege}SeDebugPrivilege)"""
"""\s+({tcb_privilege}SeTcbPrivilege)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"
},
{
Name = "microsoft-evsecurity-kv-user-password-reset-success-4724-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|McAfee|ESM"""
"""43-26304724"""
]
Fields = [
"""\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|"""
"""({event_name}An attempt was made to reset an account's password)"""
"""\srt=({time}\d{13})"""
"""shost=({host}[\w\-.]+)"""
"""sntdom=({domain}[^\s]+)"""
"""dntdom=({dest_domain}[^\s]+)"""
"""suser=({user}[\w\.\-]{1,40}\$?)\s+\w+="""
"""duser=({dest_user}.+?)\s+\w+="""
"""nitroSource_Logon_ID=({login_id}.+?)(\s|0\|)"""
"""nitroSecurity_ID=({user_sid}[^\s]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-evsecurity-kv-user-password-reset-success-4724-3"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""LogType="WLS""""
"""EventID="4724""""
]
Fields = [
"""Computer="+({dest_host}[\w\-.]+)""""
"""EventID="+({event_code}[^"]+)""""
"""EventRecordID="+({event_id}[^"]+)""""
"""SubjectUserSid="+({user_sid}[^"]+)""""
"""SubjectUserName ="+({user}[\w\.\-]{1,40}\$?)""""
"""SubjectDomainName ="+({domain}[^"]+)""""
"""SubjectLogonId="+({login_id}[^"]+)""""
"""TargetSid="+({dest_user_sid}[^"]+)""""
"""TargetDomainName ="+({dest_domain}[^"]+)""""
"""TargetUserName ="+({dest_user}[^"]+)""""
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Fields = [
"""({time}\d+-\d+-\d+T\d+:\d+:\d+).+\sLogType"""
"""EventID="+({event_code}\d+)""""
"""Opcode.+ProcessName ="+(-|({process_path}({process_dir}(:?[\w:]+)?[^.]+[\\\/]+))({process_name}[^"]+))""""
"""ServiceName ="+({service_name}[^"]+)""""
"""ServiceType="+({service_type}[^"]+)""""
"""ServiceAccount="+({account_name}[^"]+)""""
"""SubjectUserName ="+(-|({user}[\w\.\-]{1,40}\$?))""""
"""SubjectDomainName ="+(-|({domain}[^"]+))""""
"""SubjectLogonId="+({login_id}[^"]+)""""
"""ProviderGuid="+({process_guid}[^"]+)""""
"""CommandLine="+({process_command_line}[^"]+)""""
"""SubjectUserSid="+({user_sid}[^"]+)""""
"""SubjectUserName ="+(-|({user}[\w\.\-]{1,40}\$?))""""
"""ObjectServer="+({object_server}[^"]+)""""
"""ProcessId="+({process_id}[^"]+)""""
"""Computer="+({dest_host}[\w\-.]+)""""
"""TargetDomainName ="+(-|({dest_domain}[^"]+))""""
"""TargetUserName ="+(-|({dest_user}[^"]+))""""
"""TargetLogonId="+({dest_user_sid}[^"]+)""""
"""TargetUserSid="+({dest_user_sid}[^"]+)""""
"""ExecutionProcessID="+({process_id}d+)""""
"""FailureReason="+({failure_reason}[^"]+)""""
"""WorkstationName ="+(-|({workstation}[^"]+))""""
"""MemberName ="+({user_dn}[^"]+)""""
"""MemberSid="+({account_id}[^"]+)""""
"""LogonType="+({login_type}\d+)""""
"""SubStatus="+({result_code}[^"]+)""""
"""LogonProcessName ="({auth_process}[^"]+)""""
"""KeyLength="({key_length}\d+)""""
"""AuthenticationPackageName ="({auth_package}[^"]+)""""
"""IpAddress="(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""""
]
DupFields = [
"dest_host->host"
]
Name = "microsoft-evsecurity-kv-user-enable-success-4722-1"
Conditions = [
"""LogType="WLS""""
"""EventID="4722""""
]
ParserVersion = "v1.0.0"
},
{
Vendor = "Microsoft"
Product = "Active Directory Federation Services"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Fields = [
"""({time}\d+-\d+-\d+T\d+:\d+:\d+).+\sLogType"""
"""EventID="+({event_code}\d+)""""
"""Opcode.+ProcessName ="+(-|({process_path}({process_dir}(:?[\w:]+)?[^.]+[\\\/]+))({process_name}[^"]+))""""
"""ServiceName ="+({service_name}[^"]+)""""
"""ServiceType="+({service_type}[^"]+)""""
"""ServiceAccount="+({account_name}[^"]+)""""
"""SubjectUserName ="+(-|({user}[\w\.\-]{1,40}\$?))""""
"""SubjectDomainName ="+(-|({domain}[^"]+))""""
"""SubjectLogonId="+({login_id}[^"]+)""""
"""ProviderGuid="+({process_guid}[^"]+)""""
"""CommandLine="+({process_command_line}[^"]+)""""
"""SubjectUserSid="+({user_sid}[^"]+)""""
"""SubjectUserName ="+(-|({user}[\w\.\-]{1,40}\$?))""""
"""ObjectServer="+({object_server}[^"]+)""""
"""ProcessId="+({process_id}[^"]+)""""
"""Computer="+({dest_host}[\w\-.]+)""""
"""TargetDomainName ="+(-|({dest_domain}[^"]+))""""
"""TargetUserName ="+(-|({dest_user}[^"]+))""""
"""TargetLogonId="+({dest_user_sid}[^"]+)""""
"""TargetUserSid="+({dest_user_sid}[^"]+)""""
"""ExecutionProcessID="+({process_id}d+)""""
"""FailureReason="+({failure_reason}[^"]+)""""
"""WorkstationName ="+(-|({workstation}[^"]+))""""
"""MemberName ="+({user_dn}[^"]+)""""
"""MemberSid="+({account_id}[^"]+)""""
"""LogonType="+({login_type}\d+)""""
"""SubStatus="+({result_code}[^"]+)""""
"""LogonProcessName ="({auth_process}[^"]+)""""
"""KeyLength="({key_length}\d+)""""
"""AuthenticationPackageName ="({auth_package}[^"]+)""""
"""IpAddress="(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""""
]
DupFields = [
"dest_host->host"
]
Name = "microsoft-windows-kv-user-enable-success-626"
Conditions = [
"""LogType="WLS""""
"""EventID="626""""
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-evsecurity-json-user-enable-success-auseraccountwasenabled"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""McAfee_SIEM:"""
"""A user account was enabled."""
]
Fields = [
"""({event_name}A user account was enabled)"""
""""src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""id":\d*({event_code}4722)"""
""""firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
""""DomainID":"({domain}[^"]+)"""
""""HostID":"({host}[^"]+)"""
""""UserIDSrc":"({user}[\w\.\-]{1,40}\$?)"""
""""Source_Logon_ID":"({login_id}[^"]+)"""
""""UserIDDst":"({dest_user}[^"]+)"""
]
ParserVersion = "v1.0.0"
},
{
Name = "microsoft-evsecurity-cef-user-enable-success-4722-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|McAfee|ESM"""
"""43-26304722"""
]
Fields = [
"""({event_name}A user account was enabled)"""
"""\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|"""
"""\srt=({time}\d{13})(\s|0\||$)"""
"""\ssrc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({dest_port}\d+))?(\s|0\||$)"""
"""\sshost=({dest_host}[\w\-.]+?)(\s|0\||$)"""
"""\ssntdom=({domain}[^\s]+?)(\s|0\||$)"""
"""\sdntdom=({dest_domain}[^\s]+?)(\s|0\||$)"""
"""\ssuser=({user}[\w\.\-]{1,40}\$?)(\s+\w+=|0\||\s*$)"""
"""\sduser=({dest_user}.+?)(\s+\w+=|0\||\s*$)"""
"""\snitroSource_Logon_ID=({login_id}.+?)(\s|0\||$)"""
]
DupFields = [
"dest_ip->host"
"dest_host->host"
]
ParserVersion = "v1.0.0"
},


{
Name = "microsoft-o365-json-email-send-fail-advancedhunting"
Vendor = "Microsoft"
Product = "Microsoft Defender for Endpoint"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """"category": "AdvancedHunting-EmailAttachmentInfo""""
  """"operationName": "Publish""""
  """"FileName":"""
  """"FileType":"""
]
Fields = [
  """"Timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""""
  """"RecipientEmailAddress":\s*"({dest_email_address}[^"@\s]+@[^"@\s]+?)""""
  """"SenderFromAddress":\s*"({email_address}[^"@\s]+@[^"@\s]+?)""""
  """"category":\s*"({category}[^"]+?)""""
  """"FileName":\s*"({file_name}[^"\.]+?(\.({file_ext}[^"]+?))?)""""
  """"FileType":\s*"({file_type}[^"]+?)""""
  """"NetworkMessageId":\s*"({message_id}[^"]+?)""""
]
DupFields = [
  "file_name->email_attachment"
]
ParserVersion = "v1.0.0"
},

${MicrosoftParserTemplates.cef-sysmon-file-write}{
  Name = microsoft-sysmon-cef-registry-modify-success-registryvalueset
  Conditions = [ """CEF:""", """|Microsoft Sysmon|Sysmon NXLog|""", """|SysmonTask-SYSMON_REG_SETVALUE|Registry value set|""" ]
  ParserVersion = "v1.0.0"
},

{
  Name = microsoft-o365-kv-app-login-fail-workload
  Vendor = Microsoft
  Product = Microsoft 365
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """SESSID=""", """RESULTCODE=""", """WORKLOAD=""", """COMMAND=UserLoginFailed""", """OBJECT=""" ]
  Fields = [
    """\sTS=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """USER=(Unknown|({email_address}[^@\s]+@[^\s\.]+?\.[^\s]+?)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^\s]+))?)\s+\w+=""",
    """DOMAIN=(|({domain}[^\s]+?))\s+\w+=""",
    """WORKLOAD=({app}[^=]+?)\s+\w+=""",
    """COMMAND=({event_name}[^=]+?)\s+\w+=""",
    """OBJECT=(Unknown|({object}[^=]+?))\s+\w+=""",
    """SIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """RESULTCODE=({result}[^=]+?)\s+\w+=""",
    """USERAGENT=\s*(|({user_agent}[^\n]+?))\s*(\w+=|$)"""
  
}
```