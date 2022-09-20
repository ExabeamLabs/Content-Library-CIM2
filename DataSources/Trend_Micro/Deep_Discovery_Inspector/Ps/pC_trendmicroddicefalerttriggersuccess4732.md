#### Parser Content
```Java
{
Name = trendmicro-ddi-cef-alert-trigger-success-473-2
  ParserVersion = v1.0.0
  Vendor = Trend Micro
  Product = Deep Discovery Inspector
  TimeFormat = "epoch"
  Conditions = [ """|McAfee|ESM""", """|473-""" ]
  Fields = [
    """CEF:([^\|]*\|){5}({alert_name}[^\|]+)\|({alert_severity}[^\|]+)""",
    """\WeventId=({alert_id}\d+)""",
    """\WnitroDestination_Hostname=({host}.+?)(\s+\w+=|\s*$)""",
    """\Wrt=({time}\d+)""",
    """\Wdst=({src_ip}[a-fA-F\d.:]+)""",
    """\Wdpt=({src_port}\d+)""",
    """\Wsrc=({dest_ip}[a-fA-F\d.:]+)""",
    """\Wspt=({dest_port}\d+)""",
    """\Wshost=({dest_host}.+?)(\s+\w+=|\s*$)""",
    """\Wact=({action}.+?)(\s+\w+=|\s*$)""",
    """\Wcat=({alert_type}.+?)(\s+\w+=|\s*$)""",
  ]


}
```