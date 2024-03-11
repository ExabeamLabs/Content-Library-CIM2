#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-alert-trigger-success-monitor-1
  ParserVersion = v1.0.0
  Product = Check Point NGFW
  Conditions = [ """product="VPN-1 & FireWall-1"""", """Action="monitor"""" ]

checkpoint-firewall-4 = {
  Vendor = Check Point
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """<\d+>\w+ \d\d \d\d:\d\d:\d\d\S*?\s+({host}[\w.\-]+)""",
    """\WAction="({action}[^"]+)""",
    """\Wrule="({rule}[^"]+)""",
    """\Wrule_uid="({rule_uid}[^"]+)""",
    """\Wservice_id="({app_protocol}[^"]+)""",
    """\Wsrc="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wproto="({protocol}[^"]+)""",
    """\Wpeer gateway="({src_translated_ip}[^"]+)""",
    """\Wservice="({dest_port}\d+)""",
    """\Ws_port="({src_port}\d+)""",
    """\Wsrc_machine_name="({src_host}[^"]+)""",
    """\Wsrc_machine_name="({src_host}[^"@]+)@({domain}[^"]+)""",
    """\Wdst_machine_name="({dest_host}[^"]+)""",
    """\Wdst_machine_name="({dest_host}[^"@]+)@({domain}[^"]+)""",
    """\W(user|dst_user_name)="({user}[^"]+)""",
    """\W(user|dst_user_name)="({full_name}[^"\(]+?)\s*\(({user}[^\)]+)""",
  ]
  DupFields = [ "action->event_name" 
}
```