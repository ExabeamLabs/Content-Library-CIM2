#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-process-create-success-592
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "MMM dd HH:mm:ss yyyy"
    Conditions = ["""A new process has been created:""", """Detailed Tracking""", """592""" ]
    Fields = [
      """({event_name}A new process has been created)""",
      """Security\s*\d+\s+(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)""",
      """({event_code}592)""",
      """(Information|Audit Success|Success Audit)\s+({host}[^\s]+)""",
      """Image File Name:\s+({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+?))\s+Creator Process ID:""",
      """Image File Name:\s+({path}.+?)\s+Creator Process ID:""",
      """User Name:\s+({user}.+?)\s+Domain:\s+({domain}.+?)\s+Logon ID:\s+\([^,]+,({login_id}[^)]+)""",
      """New Process ID:\s+({process_guid}[^\s]+)\s""",
      """Creator Process ID:\s+({parent_process_guid}[^\s]+)\s"""
    ]
    DupFields = [ "host->dest_host","process_guid->process_id" ]
        ParserVersion = "v1.0.0"
  

}
```