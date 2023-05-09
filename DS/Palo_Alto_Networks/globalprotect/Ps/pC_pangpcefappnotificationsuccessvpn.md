#### Parser Content
```Java
{
Name = pan-gp-cef-app-notification-success-vpn
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = ["""CEF:0|Palo Alto Networks|""", """|SYSTEM|vpn|""", ]
  Fields = [
    """\sdvchost=({host}[\w.-]+?)\s+(\w+=|$)""",
    """\srt=({time}\w{3}\s\d{2}\s\d{4}\s(\d{2}:){2}\d{2})\s""",
    """\sact=(|({result}[^=]+?))(\s+\w+=|\s*$)""",
    """\smsg=({additional_info}[^=]+?)\s+(\w+=|$)""",
  ]
  ParserVersion = "v1.0.0"


}
```