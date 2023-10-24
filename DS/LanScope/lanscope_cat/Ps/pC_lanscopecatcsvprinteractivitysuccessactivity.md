#### Parser Content
```Java
{
Name = lanscope-cat-csv-printer-activity-success-activity
  Vendor = LanScope
  Product = LanScope Cat
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ ""","プリントログ",""", ""","ドキュメントの印刷",""" ]
  Fields = [
    ""","(|({host}[^"]+))","(|({user}[\w\.\-]{1,40}\$?))","({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)","プリントログ"""",
    """ドキュメントの印刷",("[^"]*",){7}"(|({printer_name}[^"]+))","[^"]*","(|({num_pages}\d+))","[^"]*","(|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)",""",
  ]
  ParserVersion = "v1.0.0"


}
```