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
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",)"({time}\d{1,4}-\d\d-\d\d \d\d:\d\d:\d\d.\d\d\d)",""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){1,2}("[^"]*",){1,21}"({user}[^"]+)"""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){1,2}("[^"]*",){1,52}"({file_name}[^"]+)"""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){1,2}("[^"]*",){1,6}"({file_path}[^"]+)""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){1,2}("[^"]*",){1,13}"({bytes}\d+)""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){1,2}("[^"]*",)+"({process_name}[^"]+)""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){1,2}("[^"]*",){1,3}"({asset_id}[^"]+)"""",
  ]


}
```