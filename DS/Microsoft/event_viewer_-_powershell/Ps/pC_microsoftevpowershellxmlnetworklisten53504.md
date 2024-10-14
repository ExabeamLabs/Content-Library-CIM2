#### Parser Content
```Java
{
Name = microsoft-evpowershell-xml-network-listen-53504
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Product = Event Viewer - PowerShell
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """<EventID>53504</EventID>""", """Microsoft-Windows-PowerShell""", """<Provider Name =""" ]
  Fields = [
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d.\d{1,9}Z?)"""
    """<Computer>({host}[\w\-.]+)"""
    """({event_code}53504)"""
    """<Security UserID\\*=('|")({user_sid}.+?)('|")\/>""",
    """<Keywords>({result}[^<]+)</Keywords>"""
    """<Data Name =('|")param1('|")>({process_id}[^<]+)"""
    """<Data Name =('|")param2('|")>({domain}[^<]+)"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```