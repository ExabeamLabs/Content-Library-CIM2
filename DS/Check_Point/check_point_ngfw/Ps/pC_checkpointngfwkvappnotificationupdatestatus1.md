#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-app-notification-updatestatus-1
  ParserVersion = v1.0.0
  Conditions = [ """ CheckPoint """, """product:"IPS"""", """update_status:""" ]
  Fields = ${DLCheckpointParsersTemplates.checkpoint-firewall-2.Fields} [
    """\Wupdate_status:"({result}[^"]+)""",
    """\Wdescription:"({additional_info}[^;]+)";"""
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