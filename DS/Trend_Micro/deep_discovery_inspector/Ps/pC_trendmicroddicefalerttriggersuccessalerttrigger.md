#### Parser Content
```Java
{
Name = trendmicro-ddi-cef-alert-trigger-success-alerttrigger
  ParserVersion = v1.0.0
  Vendor = Trend Micro
  Product = Deep Discovery Inspector
  TimeFormat = "MMM dd yyyy HH:mm:ss zZ"
  Conditions = [ """CEF:""", """|Trend Micro|Deep Discovery Inspector|""", """dvc=""" ]
  Fields = [
    """CEF:([^\|]*\|){5}({alert_name}[^\|]+)\|({alert_severity}[^\|]+)""",
    """\WeventId=({alert_id}\d+)""",
    """\Wdvc=({host}[^=]+?)(\s+\w+=|\s*$)""",
    """\Wdvchost=({host}[^=]+?)(\s+\w+=|\s*$)""",
    """\Wrt=({time}\w+\s+\d\d \d\d\d\d \d\d:\d\d:\d\d \S+)""",
    """\Wshost=((\d{1,3}\.){3}\d{1,3}|({src_host}[^\s]+))""",
    """\Wdhost=((\d{1,3}\.){3}\d{1,3}|({dest_host}[^\s]+))""",
    """\Wapp=({app}[^=]+?)(\s+\w+=|\s*$)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wspt=({src_port}\d+)""",
    """\Wact=({action}[^=]+?)(\s+\w+=|\s*$)""",
    """\Wcn3=({threat_type}[^=]+?)(\s+\w+=|\s*$)""",
    """\Wcat=({alert_type}[^=]+?)(\s+\w+=|\s*$)""",
    """CEF:(?:[^\|]*\|){5}({alert_name}[^\|]+)\|(Unknown|({alert_severity}[^\|]+))\|\w+="""
  ]


}
```