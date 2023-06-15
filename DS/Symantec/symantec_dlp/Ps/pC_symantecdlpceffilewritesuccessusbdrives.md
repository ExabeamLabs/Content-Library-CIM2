#### Parser Content
```Java
{
Name = symantec-dlp-cef-file-write-success-usbdrives
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "epoch"
  Conditions = [ """Log files written to USB drives""", """File Write""", """|Symantec|Endpoint Protection|"""]
  Fields = [
    """\srt=({time}\d{13})""",
    """\sdhost=({dest_host}[^\s]+)""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sduser=({user}.+?)\s\w+=""",
    """\sdproc=Process Name:\s+(?: |({process_path}({process_dir}(?:[^=]+)?[\\\/])?({process_name}[^\\\/]+?)))\s\w+=""",
    """\scs1=[^|]+?\| ({operation_details}.+?)\s\w+=""",
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