#### Parser Content
```Java
{
Name = skysea-cv-csv-file-success-fileactivity-1
  ParserVersion = v1.0.0
  Vendor = SkySea
  Product = SkySea ClientView
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ ",ファイル操作," ]
  Fields = [
    """^([^\,]*\,){7}({time}\d+\/\d+\/\d+ \d+:\d+:\d+)""",
    """^([^\,]*\,){5}(SYSTEM|NETWORK SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\,""",
    """({host}[\w\-.]+),\d+,""",
    """^([^\,]*\,){3}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\,""",
    """^([^\,]*\,){19}({src_file_path}({file_dir}[^,]*?)({src_file_name}[^\\.,]+(\.({src_file_ext}[^\\.,]+?))?))\,""",
    """^([^\,]*\,){17}({access}[^\,]+)\,""",
    """^([^\,]*\,){69}({hash_md5}[^\,]+)\,""",
    """^([^\,]*\,){82}({bytes}\d+)\,"""
  ]


}
```