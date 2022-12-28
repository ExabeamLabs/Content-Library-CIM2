#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-endpoint-activity-4933
   ParserVersion = "v1.0.0"
   Vendor = Microsoft
   Product = Event Viewer - Security
   TimeFormat = "epoch"
   Conditions = [  """CEF:""", """|Microsoft|Microsoft Windows|""" ]
   Fields = [
      """CEF:([^\|]*\|){4}[^\|]*?({event_code}\d+)\|({event_name}[^\|]+)\|""",
      """\WcategoryOutcome=(|/({result}.+?))(\s+\w+=|\s*$)""",
      """\Wrt=({time}\d{13})""",
      """\Wdhost=(|({dest_host}.+?))(\s+\w+=|\s*$)""",
      """\Wdntdom=(|({domain}.+?))(\s+\w+=|\s*$)""",
      """\Wduser=(|({user}.+?))(\s+\w+=|\s*$)""",
      """\Wduid=(|({user_id}.+?))(\s+\w+=|\s*$)""",
      """\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)"""
   ]


}
```