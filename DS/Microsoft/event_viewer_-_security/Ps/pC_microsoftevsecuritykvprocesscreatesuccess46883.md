#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-create-success-4688-3
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
    Conditions = [ """Exabeam Windows 4688""", """summary_windows_4688_data""" ]
    Fields = [
      """search_time=({time}\d+)"""
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+[+-]\d+)""",
      """({event_code}4688)""",
      """summary_windows_4688_data="+\d+:\d+:\d+\s*\d+-\d+-\d+:::({host}[^:::]+)?:::({user_sid}[^:::]+)?:::({user}[\w\.\-]{1,40}\$?)?:::({domain}[^:::]+)?:::({login_id}[^:::]+)?:::({process_guid}[^:::]+)?:::({process_path}({process_dir}(?:.+?)?[\\\/])?({process_name}[^\\\/:::]+))?:::({process_command_line}[^:::]+)?:::({parent_process_guid}[^:::]+)?:::({operation_type}[^:::]+)?""""
    ]
    DupFields = [ "process_guid->process_id" , "host->src_host" ]
	ParserVersion = "v1.0.0"
  

}
```