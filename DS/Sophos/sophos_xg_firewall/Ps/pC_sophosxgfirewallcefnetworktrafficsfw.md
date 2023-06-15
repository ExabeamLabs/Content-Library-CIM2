#### Parser Content
```Java
{
Name = sophos-xgfirewall-cef-network-traffic-sfw
  ParserVersion = v1.0.0
  Vendor = Sophos
  ParserVersion = v1.0.0
  Product = Sophos XG Firewall
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Sophos|SFW|""", """Firewall""" ]
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wdvc=({host}[A-Fa-f:\d.]+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wlog_component="({operation}[^"]+)"""",
    """\WcategoryOutcome=({result}[^"\s]+)""",
    """\Wstatus="({result}[^"]+)"""",
    """\Wsuser=({user}[^\s@"]+)@({email_domain}[^\s@"]+)"""",
    """\Wuser_name="({user}[^\s@"]+)"""",
    """\Wuser_name="({email_address}[^\s@"]+@[^\s@"]+)"""",
    """\Wsrc(_ip)?=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wfw_rule_id=({rule}\d+)""",
    """\Win_interface=({src_interface}\d+)""",
    """\Wout_interface=({dest_interface}\d+)""",
    """\Wreason=({failure_reason}.+?)\s+(\w+=|$)""",
  ]


}
```