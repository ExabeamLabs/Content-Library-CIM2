#### Parser Content
```Java
{
Name = juniper-ps-kv-app-activity-success-webrequestcomplect
 Vendor = Juniper Networks
 Product = Juniper Pulse Secure
 TimeFormat = "yyyy-MM-dd HH:mm:ss"
 ParserVersion = "v1.0.0"
 Conditions = [ """WEB20174""", """WebRequest completed""" ]
 Fields = [
   """\stime="({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)"""",
   """\s+vpn=({host}[^\s]+)\s"""
   """\d\d:\d\d:\d\d ({host}[^\s]+)\s+""",
   """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
   """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
   """\ssuser=({user}[^\s]+)""",
   """\sdstname=({app}.+?)\s+\w+=""",
   """\sdstname=({dest_host}[^\s]+)""",
   """\ssent\\*=({bytes}\d+)""",
   """Cmd\\*=({operation}[^\s&"]+)""",
   """User\\*=({user}[^\s&"]+)""",
   """DeviceType\\*=({src_host}[^"&]+)""",
   """agent="({user_agent}[^"]+)"""",
 ]


}
```