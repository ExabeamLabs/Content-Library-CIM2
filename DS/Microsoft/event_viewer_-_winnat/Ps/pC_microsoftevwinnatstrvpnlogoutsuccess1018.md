#### Parser Content
```Java
{
Name = microsoft-evwinnat-str-vpn-logout-success-1018
  Vendor = Microsoft
  Product = "Event Viewer - WinNat"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  ParserVersion = "v1.0.0"
  Conditions = [ """ 1018 """, """session deleted""",""" MSWinEventLog """ ]
  Fields = [
    """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)\s+\d+\s+(({provider_name}[^\s]+))?""",
    """({event_code}1018)""",
    """Information\s+({host}[\w\.\-]+)\s+\w+\s+({event_name}[^\.]+)"""
	"""source transport addr ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
	"""dest transport addr ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  ]


}
```