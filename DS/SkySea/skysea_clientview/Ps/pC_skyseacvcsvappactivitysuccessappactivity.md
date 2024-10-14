#### Parser Content
```Java
{
Name = skysea-cv-csv-app-activity-success-appactivity
  ParserVersion = v1.0.0
  Vendor = SkySea
  Product = SkySea ClientView
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """,起動・終了,""" ]
  Fields = [
    """^([^\,]*\,){2}({src_host}[^\,]+)\,""",
    """^([^\,]*\,){3}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\,""",
    """^([^\,]*\,){5}({user}[\w\.\-\!\#\^\~]{1,40}\$?)\,""",
    """^([^\,]*\,){7}({time}\d+\/\d+\/\d+ \d+:\d+:\d+)""",
    """^([^\,]*\,){81}({domain}[^\,]+)\,""",
    """^([^\,]*\,){17}({operation}[^\,]+)\,""",
    """^([^\,]*\,){8}({additional_info}[^\,]+)\,"""
  ]
  DupFields = [ "host->dest_host" ]


}
```