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
    """\Wrt=({time}\d{13})""",
    """({event_name}Group Policy settings for Windows Firewall were changed, and the new settings were applied)""",
    """({event_code}4954)""",
    """ComputerName:\s*({host}[\w.\-]+)""",
    """\Wdhost=(|({dest_host}[\w\-.]+?))(\s+\w+=|\s*$)""",
    """\Wshost=(|({src_host}.+?))(\s+\w+=|\s*$)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdvc=({host}[a-fA-F\d.:]+)""",
    """\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)""",
  ]


}
```