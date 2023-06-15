#### Parser Content
```Java
{
Name = infowatch-dlp-cef-file-write-success-externaldevice
  Vendor = InfoWatch
  Product = InfoWatch DLP
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|DLP TM""", """|External device|""" ]
  Fields = [
    """CEF:([^\|]*\|){5}({device_type}[^\|]+)""",
    """\Wrt=({time}\d{13})""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wshost=({src_host}.+?)(\s+[\w\.]+=|\s*$)""",
    """\Wact=({result}.+?)(\s+[\w\.]+=|\s*$)""",
    """\Wsntdom=({user}[^@]+?)@({domain}[^@]+?)(\s+[\w\.]+=|\s*$)""",
    """\Wsuser=({user}.+?)(\s+[\w\.]+=|\s*$)""",
    """\Wfname=({file_name}.+?(?:\.({file_ext}[^\.]+?))?)(\s+[\w\.]+=|\s*$)""",
    """\WfilePath=({file_path}({file_dir}[^=]*?[\\\/]+)?[^\\\/]+?)(\s+[\w\.]+=|\s*$)""",
    """\Wdvc=({host}.+?)(\s+[\w\.]+=|\s*$)""",
    """\Wdvchost=({host}.+?)(\s+[\w\.]+=|\s*$)""",
    """\Wsuid=({full_name}.+?)(\s+[\w\.]+=|\s*$)""",
  ]
ParserVersion = "v1.0.0"


}
```