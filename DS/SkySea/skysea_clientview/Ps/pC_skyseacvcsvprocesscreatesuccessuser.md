#### Parser Content
```Java
{
Name = skysea-cv-csv-process-create-success-user
    Vendor = SkySea
    Product = SkySea ClientView
    TimeFormat = "yyyy/MM/dd HH:mm:ss"
    Conditions = [ """,クライアント操作,""" ]
    Fields = [
      """^([^\,]*\,){4}({session_id}\d)\,""",
      """^([^\,]*\,){11}({process_name}[^\,]+)\,""",
      """^([^\,]*\,){12}\s*({file_name}[^\,]+?)\s*\,""",
      """^([^\,]*\,){8}({operation_type}[^\,]+)\,"""
      """({host}[\w\-.]+),\d+,""",
      """^([^\,]*\,){3}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\,""",
      """^([^\,]*\,){5}({user}[\w\.\-\!\#\^\~]{1,40}\$?)\,""",
      """^([^\,]*\,){7}({time}\d+\/\d+\/\d+ \d+:\d+:\d+)""",
    ]
    ParserVersion = "v1.0.0"
  

}
```