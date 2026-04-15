#### Parser Content
```Java
{
Name = microsoft-mdhcplog-xml-configuration-modify-success-dhcpserver
  Vendor = Microsoft
  Product = Microsoft DHCP Log
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [""">Microsoft-Windows-Dhcp-Server/Operational<""", """<Event xmlns""", """<Provider Name""", """<Data Name ="""]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[\w\-.]+)""",
    """Provider Name\\*=('|")({provider_name}[^\'"]+)""",
    """Guid\\*=('|")\{({process_guid}[^\'"\}]+)""",
    """<EventRecordID>({event_id}\d+)<""",
    """<Keywords>({result_code}({result}[^<]+))""",
    """<EventID>({event_code}\d+)""",
    """<EventData>({additional_info}.+?)<\/EventData>""",
    """<Execution ProcessID\\*=('|")({process_id}\d+)""",
    """<Level>({run_level}[^<]+)<""",
    """<Channel>({channel}[^<]+)<"""
    """<Security UserID=('|")({user_sid}[^"'<]+)"""
    """"(IP_ScopeName|IP_Name)">\[\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """"ClientName">(({domain}[^\\<]+?)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)<"""
    """(Reservation|Scope|Option setting):\s+({action}[^<=]+)\s+<"""
  ]
  ParserVersion = "v1.0.0"


}
```