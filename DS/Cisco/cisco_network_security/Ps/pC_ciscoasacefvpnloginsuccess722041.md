#### Parser Content
```Java
{
Name = cisco-asa-cef-vpn-login-success-722041
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = "epoch"
  Conditions = [ """|CISCO|ASA|""", """|722041|""" ]
  Fields = [
    """\srt=({time}\d{13})""",
    """\|({event_code}722041)""",
    """\sUser\s+<(({domain}[^\\]+)\\)?(?:({full_name}(\w+\s+)+\w+)|({email_address}[^@\s>]+@[^@\s>]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))>""",
    """\sIP\s+<({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})>""",
    """\sduser=<?(?:({domain}[^\s]+?)\\+)?(?:({full_name}(\w+\s+)+\w+)|({email_address}[^@\s>]+@[^@\s>]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))>?\s+([\w.]+=|$)""",
    """\sad\.Username=<?(?:({domain}[^\s]+?)\\+)?(?:({full_name}(\w+\s+)+\w+)|({email_address}[^@\s>]+@[^@\s>]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))>?\s+([\w.]+=|$)""",
    """\sdhost=<?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\-.]+?))>?\s+([\w.]+=|$)""",
    """\sdvchost=({host}[^\s]+)""",
    """\sc6a3=({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}).*?c6a3Label=Destination""",
  ]
  DupFields = ["user->account"]
  ParserVersion = "v1.0.0"


}
```