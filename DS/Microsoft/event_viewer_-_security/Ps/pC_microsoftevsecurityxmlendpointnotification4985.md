#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-4985
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>4985<""", """The state of a transaction has changed""" ]
  Fields = ${DLWindowsParsersTemplates.s-xml-events.Fields}[
    """<Data Name(\\)?=('|")SubjectDomainName('|")>(-|({domain}[^<]+?))<""",
    """Account Domain:\s*(NT AUTHORITY|-|({domain}\S+))\s+Logon ID:""",
    """<Data Name(\\)?=('|")SubjectUserName('|")>(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<""",
    """Account Name:\s*(LOCAL SERVICE|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:""",
    """Client IP: ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """<Computer>({host}[\w\-.]+?)<""",
# new_state is removed
# resource_manager is removed
    """<Data Name[^<>]+?SubjectUserSid[^<>]+?>({user_sid}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectUserName[^<>]+?>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>""",
    """<Data Name[^<>]+?SubjectDomainName[^<>]+?>({src_domain}({domain}[^<>]+?))</Data>""",
    """<Data Name[^<>]+?SubjectLogonId[^<>]+?>({login_id}[^<>]+?)</Data>""",
# transation_id is removed
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  ]

s-xml-events = {
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