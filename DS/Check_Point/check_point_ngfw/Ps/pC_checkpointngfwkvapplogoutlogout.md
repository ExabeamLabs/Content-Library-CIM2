#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-app-logout-logout
  ParserVersion = v1.0.0
  Conditions = [ """CheckPoint""", """product:""", """action:"Log Out"""" ]
  Fields = ${DLCheckpointParsersTemplates.checkpoint-firewall-2.Fields}[
    """\Wduration:"({duration}[^"]+?)\s*"""",
    """\Wdomain_name:"({domain}[^"]+?)\s*"""",
# termination_reason is removed
    """\Worigin_sic_name:"({origin_sic_name}[^"]+?)\s*""""
  ]

checkpoint-firewall-2 = {
  Vendor = Check Point 
  Product = Check Point NGFW
  TimeFormat = "dMMMyyyy HH:mm:ss"
  Fields = [
    """\Wtime="\s*({time}\d+\w+\d\d\d\d \d\d:\d\d:\d\d)""",
    """\Worig=({host}[^,]+)""",
    """\Waction=({action}[^,]+)""",
    """\Wrule=({rule}[^,]+)""",
    """\Wsrc=(?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^,]+))""",
    """\Ws_port=({src_port}\d+)""",
    """\Wdst=(?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^,]+))""",
    """\Wd_port=({dest_port}\d+)""",
    """\Wproto=({protocol}[^,]+)""",
    """\Wmessage_info="({alert_name}[^"]+)""",
  ]
  DupFields = [ "alert_name->alert_type" 
}
```