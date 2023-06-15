#### Parser Content
```Java
{
Name = skysea-cv-csv-file-download-success-web
  ParserVersion = v1.0.0
  Vendor = SkySea
  Product = SkySea ClientView
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [""",Webアクセス,""", """,Webダウンロード,"""]
  Fields = [
    """({host}[^,]+),(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))|({src_host}[\w\-.]+)),[^,]*,({user}[^,]*),[^,]*,[^,]*,[^,]*,[^,]*,Webアクセス""",
    """({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
    """,Webアクセス,[^,]*,[^,]*,({download_source}(?:[^:\\\/\s,"]+:[\\\/]+)?({domain}[^\\\/\s:,"]+)[^,]*)""",
    """Webアクセス,([^,]*,){32}(({file_path}[^=]+?)\\+)?({src_file_name}[^\\]+?),""",
  ]
  DupFields = [ "src_file_name->file_name" ]


}
```