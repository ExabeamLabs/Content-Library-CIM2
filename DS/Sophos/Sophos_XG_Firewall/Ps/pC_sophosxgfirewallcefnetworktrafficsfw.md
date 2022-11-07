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
    """\Wrt=({time}\d+)""",
    """\Wdvc=({host}[A-Fa-f:\d.]+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wlog_component="({operation}[^"]+)"""",
    """\WcategoryOutcome=({action}[^"\s]+)""",
    """\Wstatus="({action}[^"]+)"""",
    """\Wsuser=({user}[^\s@"]+)@({email_domain}[^\s@"]+)"""",
    """\Wuser_name="({user}[^\s@"]+)"""",
    """\Wuser_name="({email_address}[^\s@"]+@[^\s@"]+)"""",
    """\Wsrc(_ip)?=({src_ip}[A-Fa-f:\d.]+)""",
    """\Wfw_rule_id=({rule}\d+)""",
    """\Win_interface=({src_interface}\d+)""",
    """\Wout_interface=({dest_interface}\d+)""",
    """\Wreason=({failure_reason}.+?)\s+(\w+=|$)""",
  ]


}
```