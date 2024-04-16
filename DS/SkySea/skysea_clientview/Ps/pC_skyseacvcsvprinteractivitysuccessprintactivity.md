#### Parser Content
```Java
{
Name = skysea-cv-csv-printer-activity-success-printactivity
  Vendor = SkySea
  Product = SkySea ClientView
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ ",プリント," ]
  Fields = [
    """({host}[\w\-.]+),\d+,""",
    """^([^\,]*\,){2}({src_host}[^\,]+)\,""",
    """^([^\,]*\,){3}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\,""",
    """^([^\,]*\,){5}({user}[\w\.\-]{1,40}\$?)\,""",
    """^([^\,]*\,){7}({time}\d+\/\d+\/\d+ \d+:\d+:\d+)""",
    """^([^\,]*\,){8}({operation}[^\,]+)\,""",
    """^([^\,]*\,){12}\s*({object}[^\,]+?)\s*\,""",
    """^([^\,]*\,){32}(((?:[^,]+)?[\\\/])?({printer_name}[^\\\/,]+?))\,""",
    """^([^\,]*\,){33}({num_pages}\d+)\,""",
    """^([^\,]*\,){60}({file_path}[^\,]+)\,""",
    """^([^\,]*\,){57}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  ]
  ParserVersion = "v1.0.0"


}
```