#### Parser Content
```Java
{
Name = "cisco-asa-str-file-download-success-filedirection"
  Vendor = "Cisco"
  Product = Cisco Network Security
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ "-303002", "%FTD-", ": FTP connection from inside:" ]
  Fields = [
    """({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)\s+({host}[\w\-.]+)\s*:\s*%FTD""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD\-({priority}\d+)\-({event_code}\d+)""",
    """ from Inside:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({src_port}\d+)""",
    """ to Outside:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({dest_port}\d+)""",
    """user (({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """Retrieved file\s*({file_path}({file_dir}[^,]*?[\\\/]+)?({file_name}[^,\\\/]*?(\.({file_ext}\w+))?))\s+""",
   ]


}
```