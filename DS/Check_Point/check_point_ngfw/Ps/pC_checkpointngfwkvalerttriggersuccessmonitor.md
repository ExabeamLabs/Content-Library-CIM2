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
    """\Wsrc=(?:({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^,]+))""",
    """\Ws_port=({src_port}\d+)""",
    """\Wdst=(?:({dest_ip}\d{1,3}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[^,]+))""",
    """\Wd_port=({dest_port}\d+)""",
    """\Wproto=({protocol}[^,]+)""",
    """\Wmessage_info="({alert_name}[^"]+)""",
  ]
  DupFields = [ "alert_name->alert_type" 
}
```