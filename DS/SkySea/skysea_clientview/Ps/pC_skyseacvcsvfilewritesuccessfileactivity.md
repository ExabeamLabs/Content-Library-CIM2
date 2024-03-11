#### Parser Content
```Java
{
Name = skysea-cv-csv-file-write-success-fileactivity
  ParserVersion = v1.0.0
  Vendor = SkySea
  Product = SkySea ClientView
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ ",ファイル操作,", ",ファイルコピー," ]
  Fields = [
    """(^|,)"?({host}[^,]+)"?,([^,]*,){6}({time}\d{4}\/\d\d\/\d\d \d\d:\d\d:\d\d),ファイル操作""",
    """(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^,]+)),([^,]*,){6}ファイル操作""",
    """(SYSTEM|({user}[^,]+)),([^,]*,){4}ファイル操作""",
    """,({operation}ファイルコピー),""",
    """,ファイルコピー,[^,]*,({src_file_name}[^,]+),([^,]*,){5}({file_path}({file_dir}.*?)({file_name}[^\\.,]+(\.({file_ext}[^\\.,]+?))?)),""",
    """,ファイルコピー,([^,]*,){51}({hash_md5}[^,]+),""",
    """,ファイルコピー,([^,]*,){64}({bytes}\d+),""",

  ]


}
```