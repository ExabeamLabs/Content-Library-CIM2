#### Parser Content
```Java
{
Name = lanscope-cat-csv-app-activity-appactivity
  Product = LanScope Cat
  Conditions = [ """"アプリケーション稼働ログ"""" ]
  ParserVersion = "v1.0.0"

s-lanscope-app-activity = {
  Vendor = LanScope
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    ""","*(|({host}[^"]+))"*,"*(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"*,"*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"*,"*[^"]*"*,"*(|({operation}[^"]+))"*,("*[^"]*"*,){2}"*(|({app}[^"]+))"*,("*[^"]*"*,){2}"*(|({file_path}({file_dir}[^"]+?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?)))"*,"*[^"]*"*,"*(|({bytes}\d+)({bytes_unit}\w+))"*,"""
  
}
```