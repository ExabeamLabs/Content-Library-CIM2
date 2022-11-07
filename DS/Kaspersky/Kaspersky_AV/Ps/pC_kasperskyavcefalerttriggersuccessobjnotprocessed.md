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
    """\Wrt=({time}\d+)""",
    """\WdeviceNtDomain=(|({domain}.+?))(\s+\w+=|\s*$)""",
    """CEF:([^\|]*\|){5}({alert_name}[^\|]+)\|({alert_severity}[^\|]+)""",
    """\Wcat=(|({alert_type}.+?))(\s+\w+=|\s*$)""",
    """\Wdhost=(|({dest_host}.+?))(\s+\w+=|\s*$)""",
    """\Wdst=({dest_ip}[a-fA-F\d.:]+)""",
    """\Wmsg=(|({additional_info}.+?))(\s+\w+=|\s*$)""",
    """\Wmsg=[^=]*?Имя объекта:\s*({file_path}({src_file_name}[^=]*?[\\\/]+)?({file_name}[^=\\\/]*?(\.({file_ext}\w+))?)?)(\s+\w+=|\s*$)"""
   ]


}
```