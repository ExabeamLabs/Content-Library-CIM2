#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-app-activity-authcrypt
  ParserVersion = "v1.0.0"
  Conditions = [ """product="VPN-1 & FireWall-1"""", """Action="authcrypt"""" ]

checkpoint-firewall-3 = {
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """<\d+>\w+ \d\d \d\d:\d\d:\d\d\S*?\s+({host}[\w.\-]+)""",
    """\WAction="({action}[^"]+)""",
    """\Wrule="({rule}[^"]+)""",
    """\Wrule_uid="({rule_uid}[^"]+)""",
    """\Wservice_id="({app_protocol}[^"]+)""",
    """\Wsrc="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wproto="({protocol}[^"]+)""",
    """\Wpeer gateway="({src_translated_ip}[^"]+)""",
    """\Wservice="({dest_port}\d+)""",
    """\Ws_port="({src_port}\d+)""",
    """\Wsrc_machine_name="({src_host}[^"]+)""",
    """\Wsrc_machine_name="({src_host}[^"@]+)@({domain}[^"]+)""",
    """\Wdst_machine_name="({dest_host}[^"]+)""",
    """\Wdst_machine_name="({dest_host}[^"@]+)@({domain}[^"]+)""",
    """\Wdst_user_name="({user}[^"\(]+?)\s*(\(|")""",
    """\Wuser="({user}[\w\.\-]{1,40}\$?)""",
  ]
  DupFields = [ "action->event_name" 
}
```