#### Parser Content
```Java
{
Name = skysea-cv-csv-process-create-success-processcreated
    Vendor = SkySea
    Product = SkySea ClientView
    TimeFormat = "yyyy/MM/dd HH:mm:ss"
    Conditions = [ ",アプリケーション," ]
    Fields = [
      """^([^\,]*\,){4}({session_id}\d)\,""",
      """^([^\,]*\,){69}({hash_md5}[^\,]+)\,""",
      """^([^\,]*\,){68}({process_path}({process_dir}(?:(\w+:)*([\\\/]+[^\\\/"]+)+)?[\\\/]+)({process_name}.+?))\,""",
      """^([^\,]*\,){8}({operation_type}[^\,]+)\,"""
      """({host}[\w\-.]+),\d+,""",
      """^([^\,]*\,){3}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\,""",
      """^([^\,]*\,){5}({user}[\w\.\-]{1,40}\$?)\,""",
      """^([^\,]*\,){7}({time}\d+\/\d+\/\d+ \d+:\d+:\d+)""",
    ]
	ParserVersion = "v1.0.0"
  

}
```