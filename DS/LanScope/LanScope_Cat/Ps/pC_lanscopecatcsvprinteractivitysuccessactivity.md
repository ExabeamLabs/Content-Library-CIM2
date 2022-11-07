#### Parser Content
```Java
{
Name = lanscope-cat-csv-printer-activity-success-activity
  Vendor = LanScope
  Product = LanScope Cat
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ ""","プリントログ",""", ""","ドキュメントの印刷",""" ]
  Fields = [
    ""","(|({host}[^"]+))","(|({user}[^"]+))","({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)","プリントログ"""",
    """ドキュメントの印刷",("[^"]*",){7}"(|({printer_name}[^"]+))","[^"]*","(|({num_pages}\d+))","[^"]*","(|({dest_ip}[^"]+))",""",
  ]
  ParserVersion = "v1.0.0"


}
```