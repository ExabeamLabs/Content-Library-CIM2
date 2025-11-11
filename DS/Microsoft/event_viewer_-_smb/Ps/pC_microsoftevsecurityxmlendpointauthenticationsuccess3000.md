#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-authentication-success-3000
  Product = Event Viewer - SMB 
  Conditions = [ """<Channel>Microsoft-Windows-SMBServer""", """<Computer>""", """<EventID>3000</EventID>""" ]
  ParserVersion = "v1.0.0"
  Fields = ${WindowsParsersTemplates.windows-xml-events.Fields}[
    """<Computer>({host}[\w\.\-]+)<""",
    """<Data Name =('|")ClientName('|")>((({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)|({src_host}[\w.-]+))<"""
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