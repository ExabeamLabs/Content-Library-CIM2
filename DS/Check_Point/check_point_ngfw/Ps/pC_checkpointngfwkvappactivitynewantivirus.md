#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-app-activity-newantivirus
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """CheckPoint""", """product:"New Anti Virus"""" ]
  Fields = ${DLCheckpointParsersTemplates.checkpoint-firewall-2.Fields}[
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) ({host}[\w.\-]+) CheckPoint """,
    """\Wupdate_status:"({result}[^"]+)""",
    """\Wseverity:"({severity}[^"]+)""",
    """\Wdsecription:"({alert_name}[^"]+)""",
    """\Wnext_update_desc:"({additional_info}[^"]+)""",
    """\Wifname:"({src_interface}[^"]+)""",
  ]
  DupFields = [ "origin_name->user_ou" ]

checkpoint-firewall-2 = {
  Vendor = Check Point 
  Product = Check Point NGFW
  TimeFormat = "dMMMyyyy HH:mm:ss"
  Fields = [
    """\Wtime="\s*({time}\d+\w+\d\d\d\d \d\d:\d\d:\d\d)""",
    """\Worig=({host}[^,]+)""",
    """\Waction=({action}[^,]+)""",
    """\Wrule=({rule}[^,]+)""",
    """\Wsrc=(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^,]+))""",
    """\Ws_port=({src_port}\d+)""",
    """\Wdst=(?:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({src_host}[^,]+))""",
    """\Wd_port=({dest_port}\d+)""",
    """\Wproto=({protocol}[^,]+)""",
    """\Wmessage_info="({alert_name}[^"]+)""",
  ]
  DupFields = [ "alert_name->alert_type" 
}
```