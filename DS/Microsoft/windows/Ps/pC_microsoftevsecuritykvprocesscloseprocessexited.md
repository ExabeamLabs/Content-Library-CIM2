#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-close-processexited
  ParserVersion = v1.0.0
  Conditions = [ """A process has exited""" ]
  Fields = ${WindowsParsersTemplates.windows-events.Fields}[
    """"EventTime\\?":\s*\\?"({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})\\?""""
    """"Hostname\\?":\\?"({host}[\w\-.]*)"""
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})\s({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+))\s""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"Computer":"({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[^"]+))"""",
    """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)""",
    """\d+\s+({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[^\s]+))\sMSWinEventLog""",
    """"forwarder":"({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[^"]+))""",
    """({event_name}A process has exited)""",
    """"EventID":({event_code}\d{1,5})""",
    """Security ID:\s*(\\+[rnt])*({user_sid}[^\\\s]+)""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"SubjectUserName":"({user}[\w\.\-]{1,40}\$?)"""",
    """Account Name:\s*(\\+[srnt])*({src_host}[^\\\s]+)""",
    """Account Domain:\s*({domain}[^:]+?)\s+Logon ID:""",
    """Logon ID:\s*(\\+[rnt])*({login_id}[^\\\s]+)""",
    """Process ID:\s*(\\+[rnt])*({process_id}[^\\\s]+)""",
    """"ProcessName":"({process_path}(({process_dir}[^"]+?)\\+)?({process_name}[^"\\]+))"""",
    """Account Name:\s*[\\t\\r\\n]*({user}[\w\.\-]{1,40}\$?)""",
    """Exit Status:\s*(\\+[rnt])*({result}[^\s"]+)"""
    """Process Name:(\s|\\t|\\n|\\r)*({process_path}({process_dir}(?:[^\s]+)?[\\\/])?({process_name}[^\\\/\s]+))\s"""
  ]

windows-events = {
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)('|")""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Message>({event_name}[^<\.]+)""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task}[^<]+)"""
    """<Level>({run_level}[^<]+)<"""
  
}
```