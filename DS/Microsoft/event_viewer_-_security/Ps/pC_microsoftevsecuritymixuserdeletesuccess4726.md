#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-user-delete-success-4726"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
  """A user account was deleted"""
  """Security ID:"""
  """Account Name:"""
]
Fields = [
  """EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
  """({event_name}A user account was deleted)"""
  """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))"""
  """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
  """Security\s+({event_id}[\d]+)"""
  """Security,({event_id}[\d]+),(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)"""
  """({event_code}4726)"""
  """"agent_hostname":"({host}[^"]+)""""
  """"computer":"({host}[^"]+)""""
  """(?i)(((audit|success)( |_)(success|audit))|information)(\s+|,)({host}[^\s,=]+)(\s+|,)"""
  """({host}[^\/\s]+)\/Microsoft-Windows-Security-Auditing \(4726\)"""
  """"dhn":"({host}[^-"]+)"""
  """Computer(\w+)?["\s]*(:|=)\s*"?({host}.+?)("|\s)"""
  """"system_name":"({host}[^"]+)""""
  """Subject:\s+Security ID:\s*({user_sid}[^:]+?)\s+Account Name:\s*(?=\w)({user}[^:]+?)\s+Account Domain:\s*(?=\w)({domain}[^:]+?)\s+Logon ID"""
  """Logon ID:\s*({login_id}[^\s]+)"""
  """Target Account.+?Security ID:\s*(%\{)?({dest_user_sid}[\w\d\-]+?)\}?\s+Account Name:"""
  """Target Account.+?Account Name:\s*({dest_user}[^:]+?)\s+Account Domain:\s*({dest_domain}[^:]+?)\s+Additional"""
]
DupFields = [
  "host->dest_host"
  "dest_user->account_name"
]
ParserVersion = "v1.0.0"


}
```