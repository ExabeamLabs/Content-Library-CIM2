#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-user-delete-success-4726"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["epoch_sec", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "MM/dd/yyyy hh:mm:ss a", "MMM dd HH:mm:ss yyyy"]
Conditions = [
  """A user account was deleted"""
  """Security ID:"""
  """Account Name:"""
]
Fields = [
  """EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
  """({event_name}A user account was deleted)"""
  """TimeGenerated=({time}\d{10})""",
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,9})?Z)"""
  """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))"""
  """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
  """Security\s+({event_id}[\d]+)"""
  """Security,({event_id}[\d]+),(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)"""
  """({event_code}4726)"""
  """"agent_hostname":"({host}[\w\-.]+)""""
  """"computer":"({host}[\w\-.]+)""""
  """(?i)(((audit|success)( |_)(success|audit))|information)(\s+|,)({host}[^\s,=]+)(\s+|,)"""
  """({host}[^\/\s]+)\/Microsoft-Windows-Security-Auditing \(4726\)"""
  """"dhn":"({host}[^-"]+)"""
  """Computer(\w+)?["\s]*(:|=)\s*"?({host}[\w\-.]+?)("|\s)"""
  """"system_name":"({host}[\w\-.]+)""""
  """Subject:\s+Security ID:\s*({user_sid}[^:]+?)\s+Account Name:\s*(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:\s*(?=\w)({domain}[^:]+?)\s+Logon ID"""
  """Logon ID:\s+(\\t)?({login_id}.+?)\s*(\\n\\n|\\r\s\\r\s\\n)*?Target Account:"""
  """Target Account.+?Security ID:\s*(%\{)?({dest_user_sid}[\w\d\-]+?)\}?\s+Account Name:"""
  """Target Account.+?Account Name:\s*((?-i)\\+[rnt])*({account_name}({dest_user}[^:].+?))((?-i)\\+[rnt])*\s*(\\n|\\r\s\\t)?\s*Account Domain:\s*((?-i)\\+[rnt])*({dest_domain}[^:].+?)\s*(\\n\\n|\\r\s\\r\s\\n)?Additional Information:"""
]
ParserVersion = "v1.0.0"


}
```