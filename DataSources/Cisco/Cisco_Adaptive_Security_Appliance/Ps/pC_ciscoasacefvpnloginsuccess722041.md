#### Parser Content
```Java
{
Name = cisco-asa-cef-vpn-login-success-722041
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "epoch"
  Conditions = [ """|CISCO|ASA|""", """|722041|""" ]
  Fields = [
    """\srt=({time}\d*)""",
    """\|({event_code}722041)""",
    """\sUser\s+<(({domain}[^\\]+)\\)?(?:({full_name}(\w+\s+)+\w+)|({email_address}[^@\s>]+@[^@\s>]+?)|({user}[^>@\s]+))>""",
    """\sIP\s+<({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})>""",
    """\sduser=<?(?:({domain}[^\s]+?)\\+)?(?:({full_name}(\w+\s+)+\w+)|({email_address}[^@\s>]+@[^@\s>]+?)|({user}[^>@\s]+))>?\s+([\w.]+=|$)""",
    """\sad\.Username=<?(?:({domain}[^\s]+?)\\+)?(?:({full_name}(\w+\s+)+\w+)|({email_address}[^@\s>]+@[^@\s>]+?)|({user}[^>@\s]+))>?\s+([\w.]+=|$)""",
    """\sdhost=<?({dest_host}.+?)>?\s+([\w.]+=|$)""",
    """\sdvchost=({host}[^\s]+)""",
    """\sc6a3=({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}).*?c6a3Label=Destination""",
  ]
  DupFields = ["user->account"]
  ParserVersion = "v1.0.0"


}
```