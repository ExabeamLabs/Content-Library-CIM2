#### Parser Content
```Java
{
Name = assetview-av-str-file-write-success-10001
  ParserVersion = v1.0.0
  Vendor = AssetView
  Product = AssetView
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ファイル作成""", """10001""" ]
  Fields = [
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",)"({time}\d{4}-\d\d-\d\d \d\d:\d\d:\d\d.\d\d\d)",""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){2}("[^"]*",){21}"({user}[\w\.\-]{1,40}\$?)"""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){2}("[^"]*",){52}"({file_name}[^"]+)"""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){2}("[^"]*",){6}"({file_path}[^"]+)""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){2}("[^"]*",){13}"({bytes}\d+)""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){2}("[^"]*",){10}"({process_name}[^"]+)""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){2}("[^"]*",){3}"({asset_id}[^"]+)"""",
  ]


}
```