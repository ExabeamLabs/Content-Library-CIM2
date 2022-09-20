#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-policy-apply-success-snare
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat =  "epoch"
  Conditions = [ """CEF:""", """|Snare|""", """Group Policy settings for Windows Firewall were changed, and the new settings were applied""" ]
  Fields = [
    """\Wrt=({time}\d+)""",
    """({event_name}Group Policy settings for Windows Firewall were changed, and the new settings were applied)""",
    """({event_code}4954)""",
    """ComputerName:\s*({host}[\w.\-]+)""",
    """\Wdhost=(|({dest_host}.+?))(\s+\w+=|\s*$)""",
    """\Wshost=(|({src_host}.+?))(\s+\w+=|\s*$)""",
    """\Wdst=({dest_ip}[a-fA-F\d.:]+)""",
    """\Wsrc=({src_ip}[a-fA-F\d.:]+)""",
    """\Wdvc=({host}[a-fA-F\d.:]+)""",
    """\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)""",
  ]


}
```