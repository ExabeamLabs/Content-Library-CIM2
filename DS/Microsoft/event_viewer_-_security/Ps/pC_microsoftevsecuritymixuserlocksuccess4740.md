#### Parser Content
```Java
{
Name = microsoft-evsecurity-mix-user-lock-success-4740
Vendor = "Microsoft"
Product = "Event Viewer - Security"
ExtractionType = json
TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss", "MM/dd/yyyy hh:mm:ss a", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
Conditions = [
"""Account That Was Locked Out"""
]
Fields = [
"""hostname=({host}[\w.\-]+),\s*\w+="""
""""agent_hostname":"({host}[\w.\-]+)""""
"""computer":"({host}[\w.\-]+)""""
"""<\d+>(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(am\s+|pm\s+)?(::ffff:)?({host}[\w\-.]+)\s"""
"""({event_name}A user account was locked out)"""
"""TimeGenerated=({time}\d{10})"""
"""({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""({event_code}4740)"""
"""(?i)(((audit|success)( |_)(success|audit))|information)(\s+|,)(::ffff:)?({host}[\w.\-]+)\s"""
"""({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\s({host}[\w.\-]+)"""
"""(::ffff:)?({host}[\w.\-]+)\/Microsoft-Windows-Security-Auditing \(4740\)"""
""""dhn":"(::ffff:)?({host}[^-"]+)"""
"""Computer : (::ffff:)?({host}[\w.\-]+)"""
"""Computer(\w+)?["\s]*(:|=)\s*"?(::ffff:)?({host}[\w.\-]+)("|\s)"""
""""system_name":"(::ffff:)?({host}[\w.\-]+)""""
"""Security,?(\srn=|\s+)?({event_id}\d+)"""
"""Subject:.+?Account Name:(\\t|\\r|\\n|\s)*({src_user}[^:]+?)(\\t|\\r|\\n|\s)*Account Domain:(\\t|\\r|\\n|\s)*(?=\w)({src_domain}[^:]+?)(\\t|\\r|\\n|\s)*Logon ID:(\\t|\\r|\\n|\s)*({login_id}[^\s\\]+)(\\t|\\r|\\n|\s)*"""
"""Locked Out:(\\[rnt]|\s)*Security ID:(\\[rnt]|\s)*(%\{)?({user_sid}([\w\d\-]+?)|([^\s]+?))\}?(\\[rnt]|\s)*Account Name:(\\[rnt]|\s)*(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\[rnt]|\s)*Additional""",
"""Account Name:(\\t|\\r|\\n|\s)*({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
""""targetUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
"""Caller Computer Name:\s*(\\[rnt]|\s)*([\\\/]+)?(::ffff:)?(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-\.]+))"""
"""\Weventrecordid="({event_id}\d+)""""
"""Subject(:|=).+?Logon ID(:|=)(\\t|\\r|\\n|\s)*({login_id}[^\s\\]+)(\\t|\\r|\\n|\s)*Account""",
"""Subject(:|=).+?Account Name(:|=)(\\[rnt]|\s)*({src_user}[^\s]*?)(\\[rnt]|\s)*[\s;]*Account Domain(:|=)""",
"""Locked Out:(\\n)*\s+Security ID:\s*(%\{)?({user_sid}([\w\d\-]+?)|([^\s]+))\}?(\\n)*\s+Account Name:\s*(?=\w)({account}[\w\.\-\!\#\^\~]{1,40}\$?)(\\n)*\s*Additional""",
"""\W__li_source_path="({host}[\w\.-]+)"""",

  """exa_json_path=$..SubjectUserName,exa_field_name=src_user"""
  """exa_json_path=$..SubjectDomainName,exa_field_name=src_domain"""
  """exa_json_path=$..SubjectLogonId,exa_field_name=login_id"""
  """exa_json_path=$..SubjectUserSid,exa_field_name=subject_sid"""
  """exa_json_path=$..TargetUserName,exa_field_name=user"""
  """exa_json_path=$..TargetSid,exa_field_name=user_sid"""
  """exa_json_path=$..TargetDomainName,exa_field_name=domain"""
  """exa_json_path=$..process.pid,exa_field_name=process_id"""
  """exa_json_path=$..provider_name,exa_field_name=provider_name"""
  """exa_json_path=$..task,exa_field_name=event_name"""
  """exa_json_path=$..computer_name,exa_field_name=host"""
  """exa_json_path=$..channel,exa_field_name=channel"""
  """exa_json_path=$..action,exa_field_name=action"""
  """exa_json_path=$..created,exa_field_name=time"""
  """exa_regex=({event_name}A user account was locked out)"""
  """exa_json_path=$..EventID,exa_field_name=event_code"""
  """exa_json_path=$..Computer,exa_field_name=host"""

]
ParserVersion = "v1.0.0"


}
```