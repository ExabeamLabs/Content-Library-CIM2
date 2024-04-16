#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-process-create-success-4688
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Conditions = [
"""<EventID>4688</EventID>""",
"""SubjectUserSid""",
"""<Data Name"""
  ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(.\d+Z)?)""",
    """({event_name}A new process has been created)""",
    """<Computer>({src_host}({host}[^<]+))<""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({event_code}4688)""",
    """<Data Name(\\)?=('|")SubjectUserSid('|")>({user_sid}[^<]+?)<""",
    """<Data Name(\\)?=('|")SubjectUserName('|")>(-|LOCAL SERVICE|({full_name}[^<\s]+\s[^<]+)|({user}[\w\.\-]{1,40}\$?))<""",
    """<Data Name(\\)?=('|")SubjectDomainName('|")>(-|NT AUTHORITY|NT-AUTORITÄT|({domain}[^<]+?))<""",
    """<Data Name(\\)?=('|")SubjectLogonId('|")>({login_id}[^<]+?)<""",
    """<Data Name(\\)?=('|")NewProcessId('|")>({process_guid}[x\da-f]+)<""",
    """<Data Name(\\)?=('|")NewProcessName('|")>({process_path}({process_dir}(?:[^<>]+)?[\\\/])?({process_name}[^\\\/<>]+))<""",
    """<Data Name(\\)?=('|")CommandLine('|")>"?\s*({process_command_line}[^<]+?)\s*"?<""",
    """<Data Name(\\)?=('|")CommandLine('|")>\s*(|-|(sc|((?:[^"]+)?[\\\/])?sc.exe)\s*(?:\\*[\w.\-]+)?\s*create\s*({service_name}.+?))\s+binPath= ({process_path}({process_dir}(?:[^<>]+)?[\\\/])?({process_name}[^\\\/<>]+))<""",
    """<Data Name(\\)?=('|")ProcessId('|")>({parent_process_guid}[x\da-f]+)<""",
    """<Data Name(\\)?=('|")ParentProcessName('|")>({parent_process_path}({parent_process_dir}[^<]+[\\\/]+)?({parent_process_name}[^<]+))<\/Data>""",
    """Creator Process Name:\s*\"*(|({parent_process_path}({parent_process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({parent_process_name}[^\\\/\"]+?)))\"*\s""",
    """<Data Name(\\)?=('|")NewProcessName('|")>({dest_process_path}({dest_process_dir}(?:[^<>]+)?[\\\/])?({dest_process_name}[^\\\/<>]+))<"""
    """<Data Name(\\)?=('|")NewProcessId('|")>({parent_process_id}[^<]+)<"""
    """New Process Name:\s*\"*(|({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}[^\\\/\"]+?)))\"*\s"""
    """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = [ "process_guid->process_id","parent_process_guid->parent_process_id" ]


}
```