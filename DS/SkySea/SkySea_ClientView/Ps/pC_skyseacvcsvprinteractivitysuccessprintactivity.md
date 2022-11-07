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
    """^([^\,]*\,){5}({user}[^\s,]+)\,""",
    """^([^\,]*\,){7}({time}\d+\/\d+\/\d+ \d+:\d+:\d+)""",
    """^([^\,]*\,){8}({operation}[^\,]+)\,""",
    """^([^\,]*\,){12}\s*({object}[^\,]+?)\s*\,""",
    """^([^\,]*\,){32}(((?:[^,]+)?[\\\/])?({printer_name}[^\\\/,]+?))\,""",
    """^([^\,]*\,){33}({num_pages}\d+)\,""",
    """^([^\,]*\,){60}({file_path}[^\,]+)\,""",
    """^([^\,]*\,){57}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
  ]
  ParserVersion = "v1.0.0"


}
```