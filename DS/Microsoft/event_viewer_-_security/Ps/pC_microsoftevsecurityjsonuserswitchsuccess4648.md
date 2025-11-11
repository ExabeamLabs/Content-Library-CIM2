#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-switch-success-4648"
  ExtractionType = json
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [
"""4648""",
""""TargetServerName":"""
  ]
  Fields = [
""""TimeGenerated\\?":\\?"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""({event_name}A logon was attempted using explicit credentials)""",
""""EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
"""\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s""",
""""EventReceivedTime":\s*({time}\d+)""",
""""timestamp":\s*({time}\d+)""",
"""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)"""",
""""(Hostname|MachineName|Computer)":"({dest_host}({host}[\w\-.]*))""",
"""({event_code}4648)""",
""""SubjectUserSid":"({user_sid}[^"]*)""",
""""SubjectUserName":"(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
""""SubjectDomainName":"(-|({src_domain}({domain}[^"]*)))""",
""""SubjectLogonId":"({login_id}[^"]*)""",
""""TargetUserName":"({account}({dest_user}[^"]*))""",
""""TargetDomainName":"({account_domain}({dest_domain}[^\s"]*))""",
""""TargetServerName":"(localhost|({dest_host}[\w\-.]*))""",
""""TargetInfo":"({dest_service_name}[^"]*)""",
""""(?i)(ProcessId)":"*({process_id}[^",]*)""",
""""ProcessName":"(?: |({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+?)))"""",
""""IpAddress":"(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""

      """exa_json_path=$.TimeGenerated,exa_field_name=time"""
      """exa_json_path=$.@timestamp,exa_field_name=time"""
      """exa_regex=({event_name}A logon was attempted using explicit credentials)"""
      """exa_json_path=$.EventTime,exa_field_name=time"""
      """exa_json_path=$.EventReceivedTime,exa_field_name=time"""
      """exa_json_path=$.timestamp,exa_field_name=time"""
      """exa_regex="(Hostname|MachineName|Computer)":"({dest_host}({host}[\w\-.]*))""",
      """exa_regex=({event_code}4648)""",
      """exa_json_path=$..SubjectUserSid,exa_field_name=user_sid"""
      """exa_json_path=$..SubjectUserName,exa_field_name=user"""
      """exa_json_path=$..SubjectUserName,exa_field_name=src_user"""
      """exa_json_path=$.SubjectDomainName,exa_field_name=domain"""
      """exa_json_path=$.SubjectDomainName,exa_field_name=src_domain"""
      """exa_json_path=$..SubjectLogonId,exa_field_name=login_id"""
      """exa_json_path=$..TargetUserName,exa_field_name=dest_user"""
      """exa_json_path=$..TargetDomainName,exa_field_name=dest_domain"""
      """exa_json_path=$..TargetUserName,exa_field_name=account"""
      """exa_json_path=$..TargetDomainName,exa_field_name=account_domain"""
      """exa_json_path=$..TargetServerName,exa_field_name=dest_host"""
      """exa_json_path=$.host,exa_field_name=host"""
      """exa_json_path=$..TargetInfo,exa_field_name=dest_service_name"""
      """exa_json_path=$..ProcessID,exa_regex=({process_id}[^",]*)"""
      """exa_json_path=$..ProcessName,exa_regex=(?: |({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+?)))$"""
      """exa_json_path=$.IpAddress,exa_regex=(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""

  ]


}
```