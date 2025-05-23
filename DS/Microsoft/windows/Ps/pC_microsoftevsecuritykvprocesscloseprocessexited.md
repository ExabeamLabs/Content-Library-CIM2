#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-close-processexited
  ParserVersion = v1.0.0
  Conditions = [ """A process has exited""" ]
  Fields = ${WindowsParsersTemplates.windows-events.Fields}[
    """ComputerName =({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+))""",
    """Workstation Name\s*:\s*(-|({src_host_windows}[^\s]+))\s+Logon GUID:""",
    """Workstation Name\s*:\s*(-|({src_host}[\w\-\.]+))\s+Logon GUID:.*?Source Network Address:\s*-\s+""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d(\s*(\+|\-)[\d\:]+)?)"""",
    """"EventTime\\?":\s*\\?"({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})\\?""""
    """"Hostname\\?":\\?"({host}[\w\-.]*)"""
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})\s({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+))\s""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"Computer":"({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[^"]+))"""",
    """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)""",
    """\d+\s+({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[^\s]+))\sMSWinEventLog""",
    """"forwarder":"({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[^"]+))""",
    """({event_name}A process has exited)""",
    """"EventID":({event_code}\d{1,5})""",
    """Security ID:\s*(\\+[rnt])*({user_sid}[^\\\s]+)""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"SubjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """Account Name:\s*(\\+[srnt])*({src_host}[^\\\s]+)""",
    """Account Domain:\s*({domain}[^:]+?)\s+Logon ID:""",
    """Logon ID:\s*(\\+[rnt])*({login_id}[^\\\s]+)""",
    """Process ID:\s*(\\+[rnt])*({process_id}[^\\\s]+)""",
    """"ProcessName":"({process_path}(({process_dir}[^"]+?)\\+)?({process_name}[^"\\]+))"""",
    """Account Name:\s*[\\t\\r\\n]*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """Exit Status:\s*(\\+[rnt])*({result}[^\s"]+?)(?:\\t|\\n|\\r|\s)*("|\s)"""
    """Process Name:(\s|\\t|\\n|\\r)*({process_path}({process_dir}(?:[^\s]+?)?[\\\/])?({process_name}[^\\\/\s]+?))(?:\\t|\\n|\\r|\s)*Exit"""
  ]
  DupFields = ["user->src_user", "domain->src_domain"]

windows-events = {
  Vendor = Microsoft
  Product = Windows
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)('|")""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Message>({event_name}[^<\.]+)""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task_name}[^<]+)"""
    """<Level>({run_level}[^<]+)<"""
  
}
```