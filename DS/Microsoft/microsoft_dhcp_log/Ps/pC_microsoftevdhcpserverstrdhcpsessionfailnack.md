#### Parser Content
```Java
{
Name = microsoft-evdhcpserver-str-dhcp-session-fail-nack
  Vendor = Microsoft
  Product = Microsoft DHCP Log
  ParserVersion = "v1.0.0"
  TimeFormat = "MM/dd/yy,HH:mm:ss"
  Conditions = [ """,NACK,""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d,\d\d:\d\d:\d\d)""",
    """<leaf>\S+\s+({host}[^\s<]+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\d\d:\d\d:\d\d\s(({dest_host}[\w-\.]+))\s+\w""",
    """NACK,(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),(|({dest_host}[\w\-.]+)),(|({src_mac}[\w]{12})),"""
  ]


}
```