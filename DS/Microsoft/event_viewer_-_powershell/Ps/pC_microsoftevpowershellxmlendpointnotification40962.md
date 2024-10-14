#### Parser Content
```Java
{
Name = microsoft-evpowershell-xml-endpoint-notification-40962
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Product = Event Viewer - PowerShell
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """<EventID>40962</EventID>""", """Microsoft-Windows-PowerShell""", """<Provider Name =""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)('|")""",
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task_name}[^<]+)"""
    """<security userid=('|")({user_sid}[^'"]+)('|")\/>"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```