#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-http-response-404
  Product = Event Viewer - System
  ParserVersion = v1.0.0
  Conditions = [ """>404</EventID>""", """<TimeCreated SystemTime""","""<Channel>System</Channel>""" ]
  Fields = ${DLWindowsParsersTemplates.s-xml-events.Fields}[
    """<Data Name(\\)?=('|")SubjectDomainName('|")>(-|({domain}[^<]+?))<""",
    """Account Domain:\s*(NT AUTHORITY|-|({domain}\S+))\s+Logon ID:""",
    """<Data Name(\\)?=('|")SubjectUserName('|")>(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<""",
    """Account Name:\s*(LOCAL SERVICE|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:""",
    """Client IP: ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """<Computer>({host}[\w\-.]+?)<""",
    """Status Code:\s*({http_response_code}\d+)""",
    """<EventData><Data>({instance_id}[^<]+)"""
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w\-\.]+)"""
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