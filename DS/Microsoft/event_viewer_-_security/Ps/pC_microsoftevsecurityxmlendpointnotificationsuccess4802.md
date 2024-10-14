#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-success-4802
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
  Conditions = [ """<EventID>4802<""", """<Provider""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = [
  """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d+Z)"""
  """<Computer>({host}[\w\-\.]+)"""
  """({event_name}The screen saver was invoked)"""
  """Security ID:\s*({user_sid}[^\s]+)"""
  """<Data Name ='TargetUserName'>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data"""
  """<Data Name ='TargetLogonId'>({login_id}[^<]+)<\/Data"""
  """({event_code}4802)"""
  """<Data Name ='TargetDomainName'>({domain}[^<]+)<\/Data"""
  """<Level>({run_level}[^<]+)<"""
  ]
  ParserVersion = "v1.0.0"


}
```