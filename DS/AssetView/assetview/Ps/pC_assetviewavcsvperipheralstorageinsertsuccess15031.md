#### Parser Content
```Java
{
Name = assetview-av-csv-peripheral-storage-insert-success-15031
  Vendor = AssetView
  Product = AssetView
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ドライブ追加""", """15031""" ]
  Fields = [
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",)"({time}\d{4}-\d\d-\d\d \d\d:\d\d:\d\d.\d\d\d)",""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){2}("[^"]*",){21}"({user}[^"]+)"""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){2}("[^"]*",){17}"({drive_letter}[^"]+)""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){2}("[^"]*",){54}"({vendor_id}[^"]+)""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){2}("[^"]*",){56}"({usb_serial_number}[^"]+)""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){2}("[^"]*",){58}"({usb_vendor}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```