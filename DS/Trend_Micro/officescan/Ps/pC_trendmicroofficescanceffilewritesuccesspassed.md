#### Parser Content
```Java
{
Name = trendmicro-officescan-cef-file-write-success-passed
  Vendor = Trend Micro
  Product = OfficeScan
  TimeFormat = "epoch"
  Conditions = [ """|Trend Micro|""", """flexString1=Passed""", """flexString2=Removable storage""" ]
  Fields = [
    """\srt=({time}\d{13})""",
    """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdvchost=({host}[^\s]+)""",
    """\scs4=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)""",
    """({operation}File Copy)""",
    """\ssrc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sshost=({dest_host}.+?)\s+(\w+=|$)""",
    """\sfname=({file_name}.+?(\.({file_ext}[^.\s]+))?)\s+(\w+=|$)""",
    """\sfilePath=({file_dir}.+?)\s+(\w+=|$)""",
    """\sflexString2=({device_type}.+?)\s+(\w+=|$)""",
    """\sflexString1=({action}.+?)\s+(\w+=|$)""",
    """\scs5=({operation_details}.+?)\s+(\w+=|$)"""
  ]
 ParserVersion = "v1.0.0"


}
```