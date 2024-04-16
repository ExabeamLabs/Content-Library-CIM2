#### Parser Content
```Java
{
Name = "assetview-av-csv-printer-activity-success-15041"
  Vendor = "AssetView"
  Product = "AssetView"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ 
    """"印刷""""
    """"15041""""
  ]
  Fields = [
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",)"({time}\d{4}-\d\d-\d\d \d\d:\d\d:\d\d.\d\d\d)","""
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){2}("[^"]*",){21}"({user}[\w\.\-]{1,40}\$?)"""
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){2}("[^"]*",){52}"({file_name}[^"]+)"""
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){2}("[^"]*",){14}"({printer_name}[^"]+)"""
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){2}("[^"]*",){15}"({num_pages}\d+)"""
    """("\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d",){2}("[^"]*",){3}"({asset_id}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```