#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-privilege-modify-fail-4673-1
    Vendor = Microsoft
    Product = Event Viewer - Security
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
    Conditions = [ "Exabeam Windows 4673", "summary_windows_4673_data" ]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+[+-]\d+)""",
      """({event_code}4763)""",
      """summary_windows_4673_data="+\d+:\d+:\d+\s*\d+-\d+-\d+:::(-|({host}[^:::]+))?:::(-|({event_code}[^:::]+))?:::(-|({result}[^:::]+))?:::(-|({process_dir}.+?))?:::(-|({process_name}.+?))?:::(-|({user}[^:::]+))?:::(-|({domain}[^:::]+))?:::(-|({login_id}[^:::]+))?:::(-|({object_server}[^:::]+))?:::(-|({privileges}.+?))""""
    ]
    DupFields=[ "host->dest_host" ]
  

}
```