#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-process-create-success-4688-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""<EventID>4688</EventID>""",
"""A new process has been created""",
"""Creator Subject:"""
  ]
  Fields = [
   """({event_name}A new process has been created)""",
   """SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
   """<Computer>({host}[\w\-.]+)<""",
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
   """<EventID>({event_code}[^<]+)<""",
   """Logon ID:\s*(|-|({login_id}[^:]+?))\s*Target Subject:""",
   """Creator Subject:\s*Security ID:\s*(|-|({user_sid}[^:]+?))\s*Account Name:""",
   """Account Name:\s*(|-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:""",
   """Account Domain:\s*(|-|NT AUTHORITY|({domain}[^:]+?))\s*Logon ID:""",
   """<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<]+)<""",
   """<Data Name\\*=('|")SubjectUserName('|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<""",
   """<Data Name\\*=('|")SubjectDomainName('|")>(NT AUTHORITY|({domain}[^<]+))<""",
   """<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)<""",
   """New Process ID:\s*({process_guid}[x\da-f]+)""",
   """<Data Name\\*=('|")NewProcessId('|")>\s*({process_guid}[x\da-f]+)<""",
   """New Process Name:\s*(|-|({process_path}({process_dir}(?:[^"]+?)?[\\\/]+)?({process_name}[^\\\/\s]+?)))\s*Token Elevation Type:""",
   """<Data Name\\*=('|")NewProcessName('|")>\s*(|-|({process_path}({process_dir}(?:[^"<]+?)?[\\\/]+)?({process_name}[^\\\/\s]+?)))\s*<\/Data>""",
   """New Process Name:\s*(|-|({path}.+?))\s*Token Elevation Type:""",
   """<Data Name\\*=('|")NewProcessName('|")>\s*(|-|({path}.+?))\s*<""",
   """Process Command Line:\s*(|-|({process_command_line}.+?))\s*Token Elevation Type""",
   """Process Command Line:\s*(|-|(sc|((?:[^"]+)?[\\\/])?sc.exe)\s*(?:\\*[\w.\-]+)?\s*create\s*({service_name}.+?))\s+binPath= \s*(|-|({process_path}({process_dir}(?:[^"]+?)?[\\\/]+)?({process_name}[^\\\/\s]+?)))\s*Token Elevation Type""",
   """<Data Name\\*=('|")CommandLine('|")>\s*(|-|({process_command_line}.+?))\s*<""",
   """Creator Process ID:\s*({parent_process_guid}[x\da-f]+)""",
   """<Data Name\\*=('|")ProcessId('|")>\s*({parent_process_guid}[x\da-f]+)<""",
   """({operation_type}Process Creation)""",
   """<Data Name\\*=('|")ParentProcessName('|")>({parent_process_path}({parent_process_dir}[^<]+[\\\/]+)?({parent_process_name}[^<]+))<"""
   """<Level>({run_level}[^<]+)<"""
   """<Data Name(\\)?\s*=('|")TargetUserName('|")>(-|({dest_user}[^<]+))"""
  ]
  DupFields = [ "process_guid->process_id" , "host->src_host" ]


}
```