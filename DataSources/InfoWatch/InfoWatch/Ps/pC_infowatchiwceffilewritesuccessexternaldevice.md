#### Parser Content
```Java
{
Name = infowatch-iw-cef-file-write-success-externaldevice
  Vendor = InfoWatch
  Product = InfoWatch
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|DLP TM""", """|External device|""" ]
  Fields = [
    """CEF:([^\|]*\|){5}({device_type}[^\|]+)""",
    """\Wrt=({time}\d+)""",
    """\Wsrc=({src_ip}[a-fA-F\d.:]+)""",
    """\Wshost=({src_host}.+?)(\s+[\w\.]+=|\s*$)""",
    """\Wact=({result}.+?)(\s+[\w\.]+=|\s*$)""",
    """\Wsntdom=({user}[^@]+?)@({domain}[^@]+?)(\s+[\w\.]+=|\s*$)""",
    """\Wsuser=({user}.+?)(\s+[\w\.]+=|\s*$)""",
    """\Wfname=({file_name}.+?(?:\.({src_file_ext}[^\.]+?))?)(\s+[\w\.]+=|\s*$)""",
    """\WfilePath=({src_file_path}({file_dir}[^=]*?[\\\/]+)?[^\\\/]+?)(\s+[\w\.]+=|\s*$)""",
    """\Wdvc=({host}.+?)(\s+[\w\.]+=|\s*$)""",
    """\Wdvchost=({host}.+?)(\s+[\w\.]+=|\s*$)""",
    """\Wsuid=({full_name}.+?)(\s+[\w\.]+=|\s*$)""",
  ]
ParserVersion = "v1.0.0"


}
```