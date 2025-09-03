#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-user-lock-success-4740
ExtractionType = json
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""EventID":4740"""
"""Microsoft-Windows-Security-Auditing"""
""""TargetUserName":""""
""""SubjectUserName":""""
]
Fields = [
  """({event_name}A user account was locked out)"""
  """"TimeGenerated\\?":\\?"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""
  """"EventTime\\?":\s*\\?"({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})\""""
  """computer":"({host}[\w.\-]+)""""
  """"Hostname\\?":\\?"({host}[\w\-.]+)"""
  """"Computer(Name)?\\?":\\?"({host}[\w\-\.]+)"""
  """({event_code}4740)"""
  """Security ID:\s*(\\t|\\r|\\n)*({user_sid}[^\s\\"]+)\s*(\\t|\\r|\\n)*Account Name:\s*(\\t|\\r|\\n)*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(\\t|\\r|\\n)*Account Domain:\s*(\\t|\\r|\\n)*({domain}[^\s\\"]+)\s*(\\t|\\r|\\n)*Logon ID:\s*(\\t|\\r|\\n)*({login_id}[^\s"\\]+)\s*(\\t|\\r|\\n)*"""
  """"SubjectUserName\\?":\\?"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """"SubjectDomainName\":\"({domain}[^\\"]+)"""
  """"SubjectLogonId\\?":\\?"({login_id}[^\\"]+)"""
  """"TargetSid\\?":\\?"({user_sid}[^\\"]+)"""
  """"TargetUserName\\?":\\?"({account}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """Caller Computer Name:\s*([\\\/]+)?(::ffff:)?(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-\.]+))"""
  """Additional Information:(\\r|\\t|\\n)*Caller Computer Name:(\\r|\\t|\\n)*({src_host}[^\\"]+)"""
  """"TargetDomainName":"\\*({src_host}[^"]+)""""
  """exa_regex=({event_name}A user account was locked out)""",
  """exa_json_path=$.TimeGenerated,exa_field_name=time"""
  """exa_json_path=$.EventTime,exa_field_name=time"""
  """exa_json_path=$.computer,exa_field_name=host"""
  """exa_json_path=$.Hostname,exa_field_name=host"""
  """exa_json_path=$.ComputerName,exa_field_name=host"""
  """exa_regex=({event_code}4740)"""
  """exa_json_path=$.Message,exa_regex=Security ID:\s*(\\t|\\r|\\n)*({user_sid}[^\s\\"]+)\s*(\\t|\\r|\\n)*Account Name:\s*(\\t|\\r|\\n)*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(\\t|\\r|\\n)*Account Domain:\s*(\\t|\\r|\\n)*({domain}[^\s\\"]+)\s*(\\t|\\r|\\n)*Logon ID:\s*(\\t|\\r|\\n)*({login_id}[^\s"\\]+)\s*(\\t|\\r|\\n)*"""
  """exa_json_path=$.SubjectUserName,exa_field_name=user"""
  """exa_json_path=$.SubjectDomainName,exa_field_name=domain"""
  """exa_json_path=$.SubjectLogonId,exa_field_name=login_id"""
  """exa_json_path=$.TargetSid,exa_field_name=user_sid"""
  """exa_json_path=$.TargetUserName,exa_regex=({account}[\w\.\-\!\#\^\~]{1,40}\$?)$"""
  """exa_json_path=$.Message,exa_regex=Caller Computer Name:\s*([\\\/]+)?(::ffff:)?(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-\.]+))"""
  """exa_json_path=$.Message,exa_regex=Additional Information:(\\r|\\t|\\n)*Caller Computer Name:(\\r|\\t|\\n)*({src_host}[^\\"]+)"""
  """exa_json_path=$.TargetDomainName,exa_regex=\\*({src_host}[^"]+)$"""
]
ParserVersion = "v1.0.0"


}
```