#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-group-modify-success-4735-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """4735|A security-enabled local group was changed|""" ]
  Fields = [
    """({event_name}A security-enabled local group was changed)""",
    """({event_code}4735)""",
    """\scategoryOutcome=/({action}\S+)""",
    """\srt=({time}\d+)""",
    """\sdvc=({host}[a-fA-F\d.:]+)""",
    """\sdvchost=(|({host}.+?))(\s+\w+=|\s+$)""",
    """\ssuser=(|({user}.+?))(\s+\w+=|\s+$)""",
    """\sdhost=(|({dest_host}.+?))(\s+\w+=|\s+$)""",
    """\sdst=({dest_ip}[a-fA-F\d.:]+)""",
    """\ssrc=({src_ip}[a-fA-F\d.:]+)""",
    """\sduser=(|({dest_user}.+?))(\s+\w+=|\s+$)""",
  ]


}
```