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
    """\Wrt=({time}\d+)""",
    """\Wdhost=(|({dest_host}.+?))(\s+\w+=|\s*$)""",
    """\Wdst=({dest_ip}[a-fA-F\d.:]+)""",
    """\Wdntdom=(|({domain}.+?))(\s+\w+=|\s*$)""",
    """\Wduser=(|({user}.+?))(\s+\w+=|\s*$)""",
    """\Wduid=(|({user_sid}.+?))(\s+\w+=|\s*$)""",
    """\Wdproc=(|({process_path}({process_dir}.*?[\\\/]+)?({process_name}[^\\\/]+?)))(\s+\w+=|\s*$)""",
    """\Wdvc=(|({host}.+?))(\s+\w+=|\s*$)""",
    """\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)""",
  ]


}
```