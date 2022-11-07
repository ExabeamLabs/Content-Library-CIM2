#### Parser Content
```Java
{
Name = trendmicro-officescan-cef-file-write-success-passed
  Vendor = Trend Micro
  Product = OfficeScan
  TimeFormat = "epoch"
  Conditions = [ """|Trend Micro|""", """flexString1=Passed""", """flexString2=Removable storage""" ]
  Fields = [
    """\srt=({time}\d+)""",
    """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdvchost=({host}[^\s]+)""",
    """\scs4=({user}.+?)\s+(\w+=|$)""",
    """({operation}File Copy)""",
    """\ssrc=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sshost=({src_host}.+?)\s+(\w+=|$)""",
    """\sfname=({file_name}.+?(\.({src_file_ext}[^.\s]+))?)\s+(\w+=|$)""",
    """\sfilePath=({file_dir}.+?)\s+(\w+=|$)""",
    """\sflexString2=({device_type}.+?)\s+(\w+=|$)""",
    """\sflexString1=({action}.+?)\s+(\w+=|$)""",
    """\scs5=({activity_details}.+?)\s+(\w+=|$)"""
  ]
 ParserVersion = "v1.0.0"


}
```