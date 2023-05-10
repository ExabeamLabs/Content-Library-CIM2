#### Parser Content
```Java
{
Name = skysea-cv-str-app-activity-success-appactivity
  Vendor = SkySea
  Product = SkySea ClientView
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """,クリップボード,""" ]
  Fields = [
    """({host}[\w\-.]+),\d+,({src_host}[\w\-.]+),({src_ip}[A-Fa-f:\d.]+),[^,]*,({user}[^\s,]+),({full_name}[^,\(\（]+(\（[^\）,]+\）)?)[^,]*,({time}\d+\/\d+\/\d+ \d+:\d+:\d+),({operation}[^,]+),([^,]*,){22}\s*($|(|({object}[^,]+?)\s*,))""",
    """,クリップボード,([^,]*,){22}(\s*$|"+\s*({object}[^"]+?)\s*"+)""",
    """({app}skysea)""",
  ]
  ParserVersion = "v1.0.0"


}
```