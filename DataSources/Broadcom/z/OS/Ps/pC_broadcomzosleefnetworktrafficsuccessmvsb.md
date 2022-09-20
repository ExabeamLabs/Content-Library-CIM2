#### Parser Content
```Java
{
Name = broadcom-zos-leef-network-traffic-success-mvsb
  Vendor = Broadcom
  Product = z/OS
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """LEEF:""", """|IBM|z/OS|""", """job=""", """sum=""" ]
  Fields = [
    """\WdevTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+\-]\d+)""",
    """\WusrName =({user}[^\s]+)""",
    """\Wname=({last_name}[^,=]+),\s*({first_name}[^,=]+?)\s+(\w+=|$)""",
    """\Wdst=(::FFFF:)?({dest_ip}[A-Fa-f:\d.]+)""",
    """\Wsrc=(::FFFF:)?({src_ip}[A-Fa-f:\d.]+)""",
    """\WsrcPort=({src_port}\d+)""",
    """\WdstPort=({dest_port}\d+)""",
    """\WsrcBytes=({bytes_in}\d+)""",
    """\WdstBytes=({bytes_out}\d+)""",
    """\Wjob=(|({operation}.+?))\s+(\w+=|$)""",
    """\Wsum=({protocol}TCP|FTP|SMTP)""",
    """\Wsum=\s*({event_name}.+?)\s+(\w+=|$)""",
  ]


}
```