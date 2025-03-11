#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-create-success-created-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "MM/dd/yyyy hh:mm:ss a", "yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd HH:mm:ss"]
  Conditions = [
"""A new process has been created""",
"""Account Name:"""
  ]
  Fields = [
    """hostname=({host}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+)),\s*\w+="""
    """"TimeCreated":"[\\\/]*Date\(({time}\d{13})"""
    """"timestamp":"({time}[^"]+)""",
    """"(host|MachineName|Computer)":"(::ffff:)?({host}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+))"""
    """HOSTNAME:\s*\\?"+\(({host}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+))"""
    """({event_name}A new process has been created)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,9})?Z)"""
    """Event Time\s+:\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))""",
    """\w+\s+({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s*""",
    """({event_code}4688)""",
    """ComputerName =({host}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+))\s"""
    """Success Audit(\s|\\t)+({host}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w\-.]+))(\s|\\t)"""
    """Process Name:(\\*[nrt]|\s)*({process_path}({process_dir}(\w+:)?[^:]+?[\\\/]+)?({process_name}[^:\\\/]+?))(\\*[nrt]|\s)+(Token Elevation Type:|Requested Operation:|%\{S-)"""
    """Target Subject:.+?Account Name:((\\)*(\\r|\\t|\\n))*\s*(-|SYSTEM|({dest_user}[^\\\s]+))((\\)*(\\r|\\t|\\n))*\s*""",
    """Subject:.+?Account Name:\s*(-|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\w+\s\w+:""",
    """Creator Subject:.+?Account Name:(\\+[rnt]|\s)*'?(-|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """Account Domain:(\\+[rnt]|\s)*(-|({domain}[^\s]+?))(\\+[rnt]|\s|;)*Logon ID:""",
    """Logon ID:(\\[nrt]|\s)*({login_id}[^\s\\;]+?)(\\[nrt]|\s)*(Target|Process)""",
    """Creator Subject:.+?Account Domain:(\\+[rnt]|\s)*(-|({domain}[^\s]+?))(\\+[rnt]|\s|;)*Logon ID:""",
    """Creator Subject:.+?Logon ID:(\\[nrt]|\s)*({login_id}[^\s\\;]+?)(\\[nrt]|\s)*(Target|Process)""",
    """New Process Name:(\\+[nrt]|\s)*({dest_process_path}({dest_process_dir}[^"=]+?)?[\\]*({dest_process_name}[^"\\=]+?))(\\+[nrt]|\s)+(Token Elevation Type:|%\{S-)""",
    """New Process ID:((\\)*(\\t|\\r|\\n))*\s*({process_guid}[^\\\s;]+)(\s|;|\\)""",
    """Creator Process ID:(\\+[rnt]|\s)*({parent_process_guid}[^\\\s;]+)(\s|\\+[rnt]|;|\\)""",
    """Creator Process Name:(\\*[nrt]|\s)*(|({parent_process_path}({parent_process_dir}[^"=]+?)?[\\]*?({parent_process_name}[^"\\=]+?)))(\\*[nrt]|\s)*(Process|%\{S-)""",
    """Process Command Line(:|=)\s{0,2}"?((?-i)\\+[rnt])*(|({process_command_line}\S[^";]*?))((\\)[\\r\\n\\t]+)*(\s*Token Elevation Type indicates|"+?\s*|;|\s*$)"""
    """Process Command Line:\s*"*(|-|(sc|((?:[^"]+)?[\\\/])?sc.exe)\s*(?:\\*[\w.\-]+)?\s*create\s*({service_name}.+?))\s+binPath= \s*(|-|({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/\s]+)))"*\s*Token Elevation Type""",
    """binPath=\s*({service_command_line}(?:\"(.+)\")|(?:(\S+)))\s*""",
    """Command\s*Line(:|=).*\s+({parameter_sct}\S+\.sct)""",
    """Command\s*Line(:|=).*\s+"({parameter_sct}.+\.sct)""",
    """Command\s*Line(:|=).*\s+({parameter_hta}\S+\.hta)""",
    """Command\s*Line(:|=).*\s+"({parameter_hta}.+\.hta)""",
    """Command\s*Line(:|=).*\s+({parameter_xml}\S+\.xml)""",
    """Command\s*Line(:|=).*\s+\s+"({parameter_xml}.+\.xml)""",
    """Command\s*Line(:|=).*\s+({parameter_csproj}\S+\.csproj)""",
    """Command\s*Line(:|=).*\s+"({parameter_csproj}.+\.csproj)""",
    """Command\s*Line(:|=).+?\/u\s*["\s]({parameter_exe}.+?\.exe)""",
    """Command\s*Line(:|=).+?\/u\s*["\s]({parameter_dll}.+?\.dll)"""
    """SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?""""
    """"NewProcessName\\?":\\?"({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+?))\s*\\?""""
    """SubjectLogonId\\?"+:\\?"+(\\[nrt]|\s)*({login_id}[^\\]+)(\\[nrt]|\s)*\\?""""
    """\"SubjectDomainName\\?":\\?"({domain}[^\\"]+)"""
  ]
  DupFields = [ "process_guid->process_id" ,"parent_process_guid->parent_process_id"]


}
```