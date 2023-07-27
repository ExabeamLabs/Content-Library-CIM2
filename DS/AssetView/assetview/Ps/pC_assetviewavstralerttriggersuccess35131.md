#### Parser Content
```Java
{
Name = assetview-av-str-alert-trigger-success-35131
  Vendor = AssetView
  Product = AssetView
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """使用禁止USB接続""", """35131""" ]
  Fields = [
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",)"({time}\d{1,4}-\d\d-\d\d \d\d:\d\d:\d\d.\d\d\d)",""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){1,2}("[^"]*",){1,21}"({user}[\w\.\-]{1,40}\$?)"""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){1,2}("[^"]*",){1,54}"({vendor_id}[^"]+)""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){1,2}("[^"]*",){1,56}"({usb_serial_number}[^"]+)""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){1,2}("[^"]*",){1,58}"({usb_vendor}[^"]+)""",
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){1,2}("[^"]*",){1,3}"({asset_id}[^"]+)"""",
  ]
  ParserVersion = "v1.0.0"


}
```