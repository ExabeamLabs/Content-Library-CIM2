#### Parser Content
```Java
{
Name = catonetworks-cc-cef-alert-trigger-success-policy
  Vendor = CatoNetworks
  Product = Cato Cloud
  TimeFormat = "EEE MMM dd HH:mm:ss Z yyyy"
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|CatoNetworks|""", """|Security|IPS|""", """internalType=SECURITY""", """ act=""" ]
  Fields = [
    """CEF:([^\|]*\|){6}({alert_severity}[^\|]+)""",
    """\Wrt=({time}\w+\s+\w+\s+\d+\s+\d\d:\d\d:\d\d\s+\w+\s+\d\d\d\d)""",
    """\Wsuser=({user}[^\s]+)\s+(\w+=|$)""",
    """\Wmsg=({alert_name}.+?)\s+(\w+=|$)""",
    """\WinternalType=({alert_type}.+?)\s+(\w+=|$)""",
    """\WflexString2=({alert_type}.+?)\s+(\w+=|$)""",
    """\Wdst=({dest_ip}[A-Fa-f:\d.]+)""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wclient_port=({src_port}\d+)""",
    """\Wdhost=({dest_host}.+?)\s+(\w+=|$)""",
    """\Wshost=({full_name}.+?)\s+(\w+=|$)""",
    """\Wurl=({malware_url}.+?)\s+(\w+=|$)""",
  ]


}
```