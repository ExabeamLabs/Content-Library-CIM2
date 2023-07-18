#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-create-success-created-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [
"""A new process has been created""",
"""Account Name:"""
  ]
  Fields = [
    """hostname=({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+)),\s*\w+="""
    """"timestamp":"({time}[^"]+)""",
    """"host":"(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))"""
    """HOSTNAME:\s*\\?"+\(({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))"""
    """({event_name}A new process has been created)""",
    """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))""",
    """\w+\s+({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s""",
    """({event_code}4688)""",
    """ComputerName =({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))\s"""
    """(Success Audit|information)\s+({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^\s]+))"""
    """Process Name:\s*({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/;\s\n]+))[\s\\n;]*Token Elevation Type:""",
    """Target Subject:.+?Account Name:((\\)*(\\r|\\t|\\n))*\s*(-|SYSTEM|({dest_user}[^\\\s]+))((\\)*(\\r|\\t|\\n))*\s*""",
    """Creator Subject:.+?Account Name:\s*(-|SYSTEM|({user}[^\s]+?))\s""",
    """Account Domain:((\\)*(\\t|\\r|\\n))*\s*(-|({domain}[^\s]+?))[\\n\s;]*((\\)*(\\t|\\r|\\n))*Logon ID:""",
    """Logon ID:\s*({login_id}[^\s;]+?)[\\n\s]*(Target|Process)""",
    """Creator Subject:.+?Account Domain:((\\)*(\\t|\\r|\\n))*\s*(-|({domain}[^\s]+?))[\\n\s;]*((\\)*(\\t|\\r|\\n))*Logon ID:""",
    """Creator Subject:.+?Logon ID:\s*({login_id}[^\s;]+?)[\\n\s]*(Target|Process)""",
    """New Process Name:\s*({dest_process_path}({dest_process_dir}[^"]+?[\\]*)?({dest_process_name}[^"\\]+?))[\s\\n]*Token Elevation Type:""",
    """New Process ID:((\\)*(\\t|\\r|\\n))*\s*({process_guid}[^\\\s;]+)(\s|;|\\)""",
    """Creator Process ID:\s*({parent_process_guid}[^\\\s;]+)(\s|;|\\)""",
    """Creator Process Name(:|=)\s*({parent_process_path}({parent_process_dir}[^:]+:[^";:\n]+)[\\\/]+?({parent_process_name}[^\\\/";]+?))[\s;]*Process""",
    """Process Command Line:\s+"?(\s*|({process_command_line}.+?))"?[\s\\n]*Token Elevation Type indicates""",
    """Process Command Line:\s*"*(|-|(sc|((?:[^"]+)?[\\\/])?sc.exe)\s*(?:\\*[\w.\-]+)?\s*create\s*({service_name}.+?))\s+binPath= \s*(|-|({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/\s]+)))"*\s*Token Elevation Type""",
    """binPath=\s*({service_command_line}(?:\"(.+)\")|(?:(\S+)))\s*""",
    """Command\s*Line(:|=).*\s+({parameter_sct}\S+\.sct)""",
    """Command\s*Line(:|=).*\s+"({parameter_sct}.+\.sct)"""",
    """Command\s*Line(:|=).*\s+({parameter_hta}\S+\.hta)""",
    """Command\s*Line(:|=).*\s+"({parameter_hta}.+\.hta)"""",
    """Command\s*Line(:|=).*\s+({parameter_xml}\S+\.xml)""",
    """Command\s*Line(:|=).*\s+\s+"({parameter_xml}.+\.xml)"""",
    """Command\s*Line(:|=).*\s+({parameter_csproj}\S+\.csproj)""",
    """Command\s*Line(:|=).*\s+"({parameter_csproj}.+\.csproj)"""",
    """Command\s*Line(:|=).+?\/u\s*["\s]({parameter_exe}.+?\.exe)""",
    """Command\s*Line(:|=).+?\/u\s*["\s]({parameter_dll}.+?\.dll)"""
    """SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[^"\\]+))\\?""""
    """"NewProcessName\\?":\\?"({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+?))\s*\\?""""
    """SubjectLogonId\\?"+:\\?"+({login_id}[^\\]+)\\?""""
    """\"SubjectDomainName\\?":\\?"({domain}[^\\"]+)"""
  ]
  DupFields = [ "host->dest_host","process_guid->process_id" ]


}
```