#### Parser Content
```Java
{
Name = skysea-cv-csv-file-success-fileactivity
  ParserVersion = v1.0.0
  Vendor = SkySea
  Product = SkySea ClientView
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ ",ファイルアクセス," ]
  Fields = [
    """^([^\,]*\,){7}({time}\d+\/\d+\/\d+ \d+:\d+:\d+)""",
    """^([^\,]*\,){16}({user}[\w\.\-]{1,40}\$?)\,""",
    """^([^\,]*\,){3}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\,""",
    """^([^\,]*\,){19}({src_file_path}({file_dir}.*?)({src_file_name}[^\\.]+(\.({src_file_ext}[^\\.]+?))?))\,""",
    """^([^\,]*\,){59}({bytes}\d+)\,""",
    """^([^\,]*\,){17}({access}[^\,]+)\,"""
  ]


}
```