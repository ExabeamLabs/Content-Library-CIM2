#### Parser Content
```Java
{
Name = microsoft-evpowershell-xml-endpoint-activity-12039
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>12039</EventID>""", """<Provider Name""", """Microsoft-Windows-PowerShell""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)('|")""",
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task_name}[^<]+)"""
    """<security userid=('|")({user_sid}[^'"]+)('|")\/>""",
    """<Level>({run_level}[^<]+)<"""
  ]


}
```