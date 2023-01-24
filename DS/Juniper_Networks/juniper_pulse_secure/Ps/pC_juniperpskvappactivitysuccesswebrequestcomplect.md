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
   """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
   """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
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