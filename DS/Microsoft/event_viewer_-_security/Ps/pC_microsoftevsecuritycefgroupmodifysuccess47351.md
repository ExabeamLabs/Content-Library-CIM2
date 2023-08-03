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
    """\srt=({time}\d{13})""",
    """\sdvc=({host}[a-fA-F\d.:]+)""",
    """\sdvchost=(|({host}.+?))(\s+\w+=|\s+$)""",
    """\ssuser=(|({user}[\w\.\-]{1,40}\$?))(\s+\w+=|\s+$)""",
    """\sdhost=(|({dest_host}.+?))(\s+\w+=|\s+$)""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sduser=(|({dest_user}.+?))(\s+\w+=|\s+$)""",
  ]


}
```