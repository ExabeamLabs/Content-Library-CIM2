#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-user-privilege-modify-4703
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = [ """<EventID>4703<""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = ${DLWindowsParsersTemplates.s-xml-events.Fields}[
    """<Computer>({host}[\w\-.]+?)<""",
    """Target Account:.*?Account Name:\s*(|({dest_user}.+?))\s*Account Domain:\s*(|({dest_domain}.+?))\s*Logon ID:""",
    """Process Name:\s*(-|({process_path}({process_dir}(?:[^<=]+)?[\\\/])?({process_name}[^\\\/<:]+?)))[\s\<\>\d]+\s+(.*?)?[\w\s]+:""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  ]

s-xml-events = {
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[\w\.\-]+)<""",
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