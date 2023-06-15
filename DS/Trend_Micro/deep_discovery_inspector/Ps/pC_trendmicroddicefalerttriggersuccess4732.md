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
    """\Wrt=({time}\d{13})""",
    """\Wdst=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdpt=({src_port}\d+)""",
    """\Wsrc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wspt=({dest_port}\d+)""",
    """\Wshost=({dest_host}.+?)(\s+\w+=|\s*$)""",
    """\Wact=({action}.+?)(\s+\w+=|\s*$)""",
    """\Wcat=({alert_type}.+?)(\s+\w+=|\s*$)""",
  ]


}
```