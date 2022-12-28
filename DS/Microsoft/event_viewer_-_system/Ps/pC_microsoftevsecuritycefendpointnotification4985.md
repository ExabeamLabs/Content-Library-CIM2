#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-endpoint-notification-4985
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Product = Event Viewer - System
  TimeFormat = "epoch"
  Conditions = [ """The state of a transaction has changed""", """4985""", """CEF:""" ]
  Fields = [
    """({event_name}The state of a transaction has changed)""",
    """({event_code}4985)""",
    """\WcategoryOutcome=/({result}[^\s]+)""",
    """\Wrt=({time}\d{13})""",
    """\Wdhost=(|({dest_host}.+?))(\s+\w+=|\s*$)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdntdom=(|({domain}.+?))(\s+\w+=|\s*$)""",
    """\Wduser=(|({user}.+?))(\s+\w+=|\s*$)""",
    """\Wduid=(|({user_sid}.+?))(\s+\w+=|\s*$)""",
    """\Wdproc=(|({process_path}({process_dir}.*?[\\\/]+)?({process_name}[^\\\/]+?)))(\s+\w+=|\s*$)""",
    """\Wdvc=(|({host}.+?))(\s+\w+=|\s*$)""",
    """\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)""",
  ]


}
```