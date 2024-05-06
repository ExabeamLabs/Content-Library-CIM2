#### Parser Content
```Java
{
Name = "microsoft-evpowershell-xml-endpoint-notification-40961"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - PowerShell"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """<EventID>40961<""", """Microsoft-Windows-PowerShell""", """<Provider Name =""" ]
  Fields = [
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z?)"""
    """<Computer>({host}[\w\-.]+)"""
    """({event_code}40961)"""
    """<Execution ProcessID\\*=('|")({process_id}\d+)"""
  ]


}
```