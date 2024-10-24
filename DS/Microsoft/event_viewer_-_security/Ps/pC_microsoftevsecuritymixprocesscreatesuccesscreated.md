#### Parser Content
```Java
{
Name = microsoft-evsecurity-mix-process-create-success-created
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [
"""A new process has been created"""
  ]
  Fields = [
    """"forwarder":"({host}[^"]+)""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))""",
    """({event_name}A new process has been created)""",
    """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
    """(?i)(((audit|success)( |_)(success|audit))|information)(\s+|,)(\s|\\[nrt])*ComputerName =({host}[\w\-.]+)""",
    """Computer(Name|_name)?\s*\\*"?(=|:|>)\s*"*({host}[\w\.-]+)(\s|,|"|<\/Computer>|$)""",
    """({host}[\w\-.]+)\s+({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(am|AM|pm|PM))""",
    """({event_code}4688)""",
    """Process Name(:|=)\s*({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+?))[\s;]*Token Elevation Type(:|=)""",
    """Process Name(:|=)\s*({path}.+?)[\s;]*Token Elevation Type(:|=)""",
    """Account Name(:|=)\s*(-|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))[\s;]*Account Domain(:|=)""",
    """Creator Subject(:|=).+?Account Name(:|=)\s*(-|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s""",
    """Target Subject(:|=).+?Account Name(:|=)\s*(-|SYSTEM|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))(;|\s)""",
    """Account Domain(:|=)\s*(-|({domain}[^\s]+?))[\s;]*Logon ID(:|=)""",
    """Logon ID(:|=)(\\[nrt]|\s)*({login_id}[^\s\\;]+)(\\[nrt]|\s)*""",
    """Creator Subject(:|=).+?Account Domain(:|=)\s*(-|({domain}[^\s]+?))[\s;]*Logon ID(:|=)""",
    """Creator Subject(:|=).+?Logon ID(:|=)(\\[nrt]|\s)*({login_id}[^\s;\\]+)(\\[nrt]|\s)*""",
    """New Process Name(:|=)(\\[nrt]|\s)*({process_path}({process_dir}[^:]+:[^";:\n]+)[\\\/]+?({process_name}[^\s\\:;]+))(\\[nrt]|\s)*""",
    """New Process ID(:|=)\s*({process_guid}[^\s;]+)(\s|;)""",
    """Creator Process ID(:|=)(\\[nrt]|\s)*({parent_process_guid}[^\s\\;]+)(\\[nrt]|\s)*(\s|;)""",
    """Creator Process Name(:|=)\s*({parent_process}([^:]+:[^";:\n]+)[\\\/]+?({parent_process_name}[^\\\/";]+?))[\s;]*Process""",
    """Creator Process Name(:|=)\s*(((?:[^";]+)?[\\\/])?({parent_process_name}[^\\\/";]+?))[\s;]*Process""",
    """Process Command Line(:|=)\s{0,2}"?(|({process_command_line}.+?))(\s*Token Elevation Type indicates|;|\s+$)""",
    """Process Command Line(:|=)\s{0,2}"?(|({process_command_line}\S[^";]*?))(\s*Token Elevation Type indicates|"\s|;|\s+$)""",
    """Process Command Line:\s*"*(|-|(sc|((?:[^"]+)?[\\\/])?sc.exe)\s*(?:\\*[\w.\-]+)?\s*create\s*({service_name}.+?))\s+binPath= \s*(|-|({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/\s]+)))"*\s*Token Elevation Type""",
    """TaskCategory=({operation_type}Process Creation)""",
    """"CommandLine":"({process_command_line}[^"]+?)\s*"""",
    """"NewProcessName":"(\\[nrt]|\s)*({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+?))(\\[nrt]|\s)*"""",
    """"ProcessId":"({process_id}[^"]+)""",
    """"SubjectAccount":"(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """"SubjectLogonId":"({login_id}[^"]+)""",
    """"NewProcessId":"({process_guid}[^"]+)""",
    """Command\s*Line(:|=)\s*(?:config)\s+({service_name}\S+)""",
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
    """"log_level":"({run_level}[^"]+)\s*""""
  ]
  DupFields = [ "process_guid->process_id" , "host->src_host", "parent_process_guid->parent_process_id" ]


}
```