#### Parser Content
```Java
{
Name = "microsoft-evapplocker-xml-alert-trigger-success-policyname"
Vendor = "Microsoft"
Product = "Event Viewer - Applocker"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
Conditions = [
  """<Channel>Microsoft-Windows-AppLocker"""
  """<PolicyName>"""
  """<Message>"""
]
Fields = [
  """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
  """<Computer>({host}.+?)</Computer>"""
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """<Data Name\\*='User'>(({domain}[^\\<]+?)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>"""
  """<Security UserID\\*='({user_sid}.+?)'/>"""
  """<Level>({alert_severity}[^"<]+)"""
  """<FilePath>({malware_url}[^"<]+)"""
  """<PolicyName>({alert_type}[^"<]+)"""
  """<PolicyName>({alert_name}[^"<]+)"""
  """<Message>({additional_info}[^"<]+)"""
  """<FileHash>({hash_md5}[^"<]+)"""
  """<EventID>({event_code}[^<]+)<"""
]
DupFields = [
  "malware_url->process_name"
]
ParserVersion = "v1.0.0"


}
```