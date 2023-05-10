#### Parser Content
```Java
{
Name = kaspersky-av-cef-alert-trigger-success-objnotprocessed
  ParserVersion = v1.0.0
  Vendor = Kaspersky
  Product = Kaspersky AV
  Conditions = [ """CEF:""", """|Kaspersky|""", """flexString1=Постоянная защита файлов""" ]
  TimeFormat = "epoch"
  Fields = [
    """\Wdvc=({host}[a-fA-F\d.:]+)""",
    """\Wrt=({time}\d{13})""",
    """\WdeviceNtDomain=(|({domain}.+?))(\s+\w+=|\s*$)""",
    """CEF:([^\|]*\|){5}({alert_name}[^\|]+)\|({alert_severity}[^\|]+)""",
    """\Wcat=(|({alert_type}.+?))(\s+\w+=|\s*$)""",
    """\Wdhost=(|({dest_host}.+?))(\s+\w+=|\s*$)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wmsg=(|({additional_info}.+?))(\s+\w+=|\s*$)""",
    """\Wmsg=[^=]*?Имя объекта:\s*({file_path}({src_file_name}[^=]*?[\\\/]+)?({file_name}[^=\\\/]*?(\.({file_ext}\w+))?)?)(\s+\w+=|\s*$)"""
   ]


}
```