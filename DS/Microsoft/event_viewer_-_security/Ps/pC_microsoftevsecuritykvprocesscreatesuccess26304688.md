#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-create-success-26304688
    Vendor = Microsoft
    Product = Event Viewer - Security
    ParserVersion = v1.0.0
    TimeFormat = "epoch"
    Conditions = [ """"|McAfee|ESM"""", """"43-26304688""""]
    Fields = [
      """({event_name}A new process has been created)""",
      """\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|""",
      """\srt=({time}\d{13})""",
      """shost=({host}[^\s]+)""",
      """sntdom=({domain}[^\s]+)""",
      """suser=({user}[\w\.\-]{1,40}\$?)\s+\w+=""",
      """nitroProcess_Name =({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+?))\s+\w+=""",
      """nitroProcess_Name =({path}.+?)\s+\w+=""",
      """nitroSource_Logon_ID=({login_id}.+?)(\s|0\|)"""
    ]
    DupFields=[ "host->dest_host" ]


}
```