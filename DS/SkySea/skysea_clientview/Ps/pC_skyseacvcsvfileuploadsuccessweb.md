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
    """({host}[^,]+),(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+)),[^,]*,({user}[\w\.\-\!\#\^\~]{1,40}\$?),[^,]*,[^,]*,[^,]*,[^,]*,Webアクセス""",
    """({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
    """,Webアクセス,[^,]*,[^,]*,({access}(?:[^:\\\/\s,"]+:[\\\/]+)?({domain}[^\\\/\s:,"]+)[^,]*)""",
    """Webアップロード,([^,]*,){23}(({src_file_dir}[^=]+?)\\+)?({src_file_name}[^\\]+?(\.({src_file_ext}[^\\,\.]+))?),""",
    """,Webアップロード,([^,]*,){72}({app}[^,]+),""",
  ]
  DupFields = [ "src_file_name->file_name", "src_file_ext->file_ext" ]


}
```