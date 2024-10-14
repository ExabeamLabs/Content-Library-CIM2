#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-create-success-mswineventlog4688
    Vendor = Microsoft
    Product = Event Viewer - Security
    ParserVersion = v1.0.0
    TimeFormat = "MMM dd HH:mm:ss yyyy"
    Conditions = [ """MSWinEventLog""", """ 4688 Microsoft-Windows-Security-Auditing""", """A new process has been created""" ]
    Fields = [
      """({event_name}A new process has been created)""",
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """({time}\w{3}\s\d{2}\s\d{2}:\d{2}:\d{2}\s\d{4})""",
      """({event_code}4688)""",
      """Information\s+({host}[\w.\-]+)\s+""",
      """(?:Success|Audit)\s+\w+\s+({host}[\w\-.]+)""",
      """New Process Name:\s+({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+?))\s+Token Elevation Type:""",
      """Process Name:\s+({path}.+?)\s+Token Elevation Type:""",
      """Creator Subject:.+?Account Name:\s+(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:\s+(?:-|({domain}.+?))\s+Logon ID:\s+({login_id}[^\s]+)""",
      """Target Subject:.+?Account Name:\s+(?:-|({dest_user}.+?))\s+Account Domain:""",
      """New Process ID:\s+({process_guid}[^\s]+)\s""",
      """Creator Process ID:\s+({parent_process_guid}[^\s]+)\s""",
      """Process Command Line:\s+"({process_command_line}[^"]+)"\s""",
      """Process Command Line:\s+"(|-|(sc|((?:[^"]+)?[\\\/])?sc.exe)\s*(?:\\*[\w.\-]+)?\s*create\s*({service_name}.+?))\s+binPath= ({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+?))"\s""",
      """TaskCategory=({operation_type}Process Creation)"""
      """Creator Process Name:\s*\"*(|({parent_process_path}({parent_process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({parent_process_name}[^\\\/\"]+?)))\"*\s"""
    ]
    DupFields = [ "process_guid->process_id" , "host->src_host" ]


}
```