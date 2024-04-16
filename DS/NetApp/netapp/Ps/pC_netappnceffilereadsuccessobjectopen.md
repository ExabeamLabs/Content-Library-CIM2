#### Parser Content
```Java
{
Name = netapp-n-cef-file-read-success-objectopen
  Vendor = NetApp
  Product = NetApp
  TimeFormat = "epoch"
  ParserVersion = "v1.0.0"
  Conditions = [ """|NetApp|Filer|""", """|Object Open|""" ]
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wdvc=({host}[A-Fa-f:\d.]+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wdhost=({dest_host}[\w\-.]+)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdntdom=({user}[\w\.\-]{1,40}\$?)\s*(\w+=|$)""",
    """\Wduser=(NetApp Data ONTAP|({user}[\w\.\-]{1,40}\$?))\s*(\w+=|$)""",
    """\Wfname=({file_path}.+?)\s*(\w+=|$)""",
    """\Wfname=({file_dir}.+?)[^\\]+\s*(\w+=|$)""",
    """\Wfname=.*?({file_name}[^\\]+?)\s*(\w+=|$)""",
    """\Wfname=.*?(\.({file_ext}[^\\\.]+?))?\s*(\w+=|$)""",
    """\WfileId=(-|({file_id}\d+))""",
    """\WfileType=({file_type}.+?)\s*(\w+=|$)""",
    """CEF:([^\|]*\|){5}({access}[^\|]+)""",
    """\Wcs1=(-|({access}.+?))\s*(\w+=|$)"""
  ]


}
```