#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-privilege-modify-fail-4672
    Vendor = Microsoft
    Product = Event Viewer - Security 
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
    Conditions = [ "Exabeam Windows 4672", "summary_windows_4672_data" ]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+[+-]\d+)""",
      """({event_code}4762)""",
      """summary_windows_4672_data="+\d+:\d+:\d+\s*\d+-\d+-\d+:::(-|({host}[^:::]+))?:::(-|({event_code}[^:::]+))?:::(-|({result}[^:::]+))?:::(-|({user}[^:::]+))?:::(-|({domain}[^:::]+))?:::(-|({login_id}[^:::]+))?:::(-|([^:::]+))?:::(-|([^:::]+))?:::(-|([^:::]+))?:::(-|({user_sid}[^:::]+))?:::(-|({privileges}.+?))?""""
    ]
    DupFields=[ "host->dest_host" ]
  

}
```