#### Parser Content
```Java
{
Name = trendmicro-ddi-leef-alert-trigger-success-detection
  ParserVersion = v1.0.0
  Vendor = Trend Micro
  Product = Deep Discovery Inspector
  TimeFormat = "MMM dd yyyy HH:mm:ss zZ"
  Conditions = ["""Deep Discovery Inspector""" , """_DETECTION|"""]
  Fields = [
     """devTime=({time}\w+\s+\d\d \d\d\d\d \d\d:\d\d:\d\d \S+)""",
     """\Wdvc=({host}.+?)(\s+\w+=|\s*$)""",
    """\Wshost=(({src_ip}[A-Fa-f:\d.]+)|({src_host}[^\s]+))""",
    """\Wdhost=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdst=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\WdstPort=({src_port}\d+)""",
    """\Wsrc=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\WsrcPort=({dest_port}\d+)""",
    """deviceMacAddress=({src_mac}.+?)(\s+\w+=|\s*$)""",
    """msg=({alert_name}.+?)\s+\w+=""",
    """proto=({protocol}[^\s]+)""",
    """ptype=({alert_type}[^\s]+)""",
    """sev=({alert_severity}\d+)""",
    """act=({action}.+?)\s+\w+=""",
    """suid=([^\\\/]+(\\|\/))?(anonymous|({email_address}[^@]+@[^\s]+)|({user}[^\s]+))""",
    """d(U|u)ser(\d+)?=([^\\]+\\)?({user}[^\s]+)"""
    """s(U|u)ser(\d+)?=([^\\]+\\)?({user}[^\s]+)"""
  ]


}
```