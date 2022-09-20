#### Parser Content
```Java
{
Name = symantec-dlp-cef-file-write-success-usbdrives
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "epoch"
  Conditions = [ """Log files written to USB drives""", """File Write""", """|Symantec|Endpoint Protection|"""]
  Fields = [
    """\srt=({time}\d+)""",
    """\sdhost=({dest_host}[^\s]+)""",
    """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sduser=({user}.+?)\s\w+=""",
    """\sdproc=Process Name:\s+(?: |({process_path}({process_dir}(?:[^=]+)?[\\\/])?({process_name}[^\\\/]+?)))\s\w+=""",
    """\scs1=[^|]+?\| ({activity_details}.+?)\s\w+=""",
    """\sfilePath=({file_path}.+?)\s\w+=""",
    """\sfilePath=[^=]*\/({file_name}[^\/]*?)\s\w+=""",
    """({operation}File Write)""",
    """\sfsize=({bytes}\d+)""",
    """DEVICE__ID=({device_id}.*?)&\d+""",
    """({device_type}(CD-DVD|USB))"""
  ]
  ParserVersion = "v1.0.0"


}
```