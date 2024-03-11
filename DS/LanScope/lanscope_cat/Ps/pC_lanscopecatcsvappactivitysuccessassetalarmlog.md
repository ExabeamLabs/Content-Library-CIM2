#### Parser Content
```Java
{
Name = lanscope-cat-csv-app-activity-success-assetalarmlog
  ParserVersion = v1.0.0
  Vendor = LanScope
  Product = LanScope Cat
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ ""","資産アラームログ",""" ]
  Fields = [
    ""","(|({host}[^"]+))","(|({user}[^"]+))","({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)",("[^"]*",){7}"(|({operation}[^"\-]+?)\s*\-\s*({object}[^"]+))","""
  ]


}
```