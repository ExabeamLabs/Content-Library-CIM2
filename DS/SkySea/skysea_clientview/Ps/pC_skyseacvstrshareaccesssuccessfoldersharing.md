#### Parser Content
```Java
{
Name = skysea-cv-str-share-access-success-foldersharing
  Vendor = SkySea
  Product = SkySea ClientView
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ ",フォルダ共有," ]
  Fields = [
    """^([^\,]*\,){7}({time}\d+\/\d+\/\d+ \d+:\d+:\d+)""",
    """^([^\,]*\,){5}({user}[\w\.\-]{1,40}\$?)\,""",
    """^([^\,]*\,){3}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\,""",
    """^([^\,]*\,){8}({access_type}[^\,]+)\,""",
    """^([^\,]*\,){11}({file_path}({file_dir}([^\,]+\\)?)({file_name}[^\,]+))\,"""
  ]


}
```