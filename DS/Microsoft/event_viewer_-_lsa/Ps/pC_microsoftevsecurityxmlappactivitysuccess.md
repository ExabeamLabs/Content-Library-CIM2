#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-app-activity-success
  Product = "Event Viewer - LSA"
  Conditions = [ """<Channel>Microsoft-Windows-LSA""", """<EventID>300</EventID>""", """<Computer>""" ]
  ParserVersion = "v1.0.0"
  Fields = ${WindowsParsersTemplates.windows-xml-events.Fields}[
    """<Computer>({host}[\w\.\-]+)<""",
    """Data Name(\\)?=('|")TargetUserName('|")>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<"""
    """Data Name(\\)?=('|")TargetDomainName('|")>({domain}({dest_domain}[^<]+))"""
    """Data Name(\\)?=('|")TargetLogonId('|")>({login_id}({dest_login_id}[^<]+))"""
    """Data Name(\\)?=('|")TargetUserSid('|")>({user_sid}({dest_user_sid}[^<]+))"""
  ]

windows-xml-events = {
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{9}Z)"""
    """>({event_code}\d+)</EventID>""",
    """<Security UserID=('|")({user_sid}[^'"]+)('|")\/>""",
    """<Execution ProcessID=('|")({process_id}\d+)('|") ThreadID=('|")({thread_id}\d+)('|")\/>""",
    """<Level>({run_level}[^<]+)<""",
    """<Provider Name =('|")({provider_name}[^'"]+)('|")""",
    """Guid=('|")\{({process_guid}[^\}'"]+?)\}('|")""",
    """<Task>({task_name}[^<]+)""",
    """<Opcode>(0|({opcode}[^<]+))<""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<EventRecordID>({event_id}[^<]+)""",
    """<Channel>({channel}[^<]+)<"""
  
}
```