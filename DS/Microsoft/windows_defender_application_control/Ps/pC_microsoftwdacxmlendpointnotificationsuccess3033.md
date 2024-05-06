#### Parser Content
```Java
{
Name = microsoft-wdac-xml-endpoint-notification-success-3033
  Vendor = Microsoft
  Product = Windows Defender Application Control
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>3033</EventID>""", """<Provider Name =""", """Microsoft-Windows-CodeIntegrity""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d.\d{1,9}Z)"""
    """<EventID>({event_code}\d+)"""
    """<Computer>({host}[\w\-.]+)"""
    """<Data Name =('|")ProcessNameBuffer('|")>\\*(({process_path}({process_dir}[^<]+[\\\\*])({process_name}[^<]+)))"""
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task_name}[^<]+)"""
    """<security userid=('|")({user_sid}[^'"]+)('|")\/>"""
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "host->dest_host" ]


}
```