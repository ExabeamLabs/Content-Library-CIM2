#### Parser Content
```Java
{
Name = skysea-cv-csv-file-upload-success-web
  ParserVersion = v1.0.0
  Vendor = SkySea
  Product = SkySea ClientView
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [""",Webアクセス,""", """,Webアップロード,"""]
  Fields = [
    """({host}[^,]+),(({src_ip}[A-Fa-f:\d.]+)|({src_host}[\w\-.]+)),[^,]*,({user}[^,]*),[^,]*,[^,]*,[^,]*,[^,]*,Webアクセス""",
    """({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
    """,Webアクセス,[^,]*,[^,]*,({access}(?:[^:\\\/\s,"]+:[\\\/]+)?({domain}[^\\\/\s:,"]+)[^,]*)""",
    """Webアップロード,([^,]*,){23}(({src_file_dir}[^=]+?)\\+)?({src_file_name}[^\\]+?),""",
    """,Webアップロード,([^,]*,){72}({app}[^,]+),""",
  ]
  DupFields = [ "src_file_name->file_name" ]


}
```