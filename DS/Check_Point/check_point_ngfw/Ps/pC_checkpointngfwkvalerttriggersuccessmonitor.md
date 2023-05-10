#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-alert-trigger-success-monitor
  ParserVersion = v1.0.0
  Product = Check Point NGFW
  Conditions = [ """product="VPN-1 & FireWall-1"""", """,i/f_name=""", """action=monitor""" ]

checkpoint-firewall-5 = {
  Vendor = Check Point
  TimeFormat = "dMMMyyyy HH:mm:ss"
  Fields = [
    """\Wtime="\s*({time}\d+\w+\d\d\d\d \d\d:\d\d:\d\d)""",
    """\Worig=({host}[^,]+)""",
    """\Waction=({action}[^,]+)""",
    """\Wrule=({rule}[^,]+)""",
    """\Wsrc=(?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^,]+))""",
    """\Ws_port=({src_port}\d+)""",
    """\Wdst=(?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^,]+))""",
    """\Wd_port=({dest_port}\d+)""",
    """\Wproto=({protocol}[^,]+)""",
    """\Wmessage_info="({alert_name}[^"]+)""",
  ]
  DupFields = [ "alert_name->alert_type" 
}
```