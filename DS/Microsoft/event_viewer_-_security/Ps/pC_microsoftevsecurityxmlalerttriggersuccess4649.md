#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-alert-trigger-success-4649"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
  """<EventID>4649</EventID>"""
  """<Provider Name"""
  """Microsoft-Windows-Security-Auditing"""
]
Fields = [
  """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>"""
  """ThreadID\\*=('|")({thread_id}[^'"]+)"""
  """Account Domain:\s*(NT AUTHORITY|({domain}\S+))\s+Logon ID:"""
  """<Computer>({host}[^<>]+)<\/Computer>"""
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """<Execution ProcessID\\*=('|")({process_id}[^'"]+)"""
  """ProcessID\\*=('|")({process_id}\d+)"""
  """Name =('|")LogonProcessName'>({auth_process}[^<]+)"""
  """<Message>({event_name}.+?)\s*\.(\s|</Message>)"""
  """<Message>({event_name}.+?)\s+Subject:"""
  """<Keywords?>({result}[^<]+)<\/Keywords?>"""
  """<Provider>({provider_name}.+?)</Provider>"""
  """<Correlation ActivityID\\*=('|")\{({activity_id}[^\}'"]+)"""
  """ActivityID\\*=('|")\{?({activity_id}[^\}'"]+)"""
  """Security ID:\s*({user_sid}\S+)\s+Account Name:"""
  """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)"""
  """Logon ID:\s*({login_id}\S+)\s+"""
  """Account Name:\s*(LOCAL SERVICE|({user}[\w\.\-]{1,40}\$?))\s+Account Domain:"""
  """<EventID>({event_code}[^<]+)<\/EventID>"""
  """({additional_info}Credentials Which Were Replayed:.+)This event indicates that a Kerberos replay attack was detected"""
  """<Level>({run_level}[^<]+)"""
]
DupFields = [
  "event_name->alert_name"
  "auth_process->alert_type"
]
ParserVersion = "v1.0.0"


}
```