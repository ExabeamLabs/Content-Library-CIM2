#### Parser Content
```Java
{
Name = pan-gp-cef-app-notification-success-userid
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "MMM dd yyyy HH:mm:ss"]
  Conditions = ["""CEF:0|Palo Alto Networks|""", """|SYSTEM|userid|""", ]
  Fields = [
    """\sdvchost=({host}[\w.-]+?)\s+(\w+=|$)""",
    """\srt=({time}\w{3}\s\d{2}\s\d{4}\s(\d{2}:){2}\d{2})\s""",
    """\sact=(|({result}[^=]+?))(\s+\w+=|\s*$)""",
    """\smsg=({additional_info}[^=]+?)\s+(\w+=|$)""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]
  ParserVersion = "v1.0.0"


}
```