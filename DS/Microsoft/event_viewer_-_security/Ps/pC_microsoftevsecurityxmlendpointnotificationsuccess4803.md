#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-success-4803
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>4803<""", """<Provider""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = [
  """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d+Z)"""
  """<Computer>({host}[\w\-\.]+)"""
  """<Data Name =('|")TargetUserName('|")>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<\/Data"""
  """<Data Name =('|")TargetLogonId('|")>({dest_login_id}({login_id}[^<]+))<\/Data"""
  """({event_code}4803)"""
  """<Data Name =('|")TargetDomainName('|")>({dest_domain}({domain}[^<]+))<\/Data"""
  """<Level>({run_level}[^<]+)<"""
  ]
  ParserVersion = "v1.0.0"


}
```