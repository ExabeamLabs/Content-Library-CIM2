#### Parser Content
```Java
{
Name = lanscope-cat-csv-file-success-realtime
  Product = LanScope Cat
  ParserVersion = "v1.0.0"
  Conditions = [ """"リアルタイムイベントログ"""" ]

s-lanscope-app-activity = {
  Vendor = LanScope
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    ""","*(|({host}[^"]+))"*,"*(|({user}[^"]+))"*,"*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"*,"*[^"]*"*,"*(|({operation}[^"]+))"*,("*[^"]*"*,){2}"*(|({app}[^"]+))"*,("*[^"]*"*,){2}"*(|({file_path}({file_dir}[^"]+?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?)))"*,"*[^"]*"*,"*(|({bytes}\d+)({bytes_unit}\w+))"*,"""
  
}
```