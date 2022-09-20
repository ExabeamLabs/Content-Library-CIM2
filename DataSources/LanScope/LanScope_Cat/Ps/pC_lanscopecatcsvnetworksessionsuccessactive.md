#### Parser Content
```Java
{
Name = lanscope-cat-csv-network-session-success-active
  Product = LanScope Cat
  ParserVersion = v1.0.0
  Conditions = [ """"リアルタイムイベントログ"""", """"ACTIVE"""" ]
  Fields = ${LanScopeParserTemplates.s-lanscope-app-activity.Fields}[
    ""","*リアルタイムイベントログ"*,"*ACTIVE"*,("*[^"]*"*,){5}"*({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({dest_port}\d+)\s+\-\s+({account}[^\s@]+)@({dest_host}[^:]+):({process_command_line}[^"]+)"*,"""
  ]
  DupFields = [ "application->process_name" ]

s-lanscope-app-activity = {
  Vendor = LanScope
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    ""","*(|({host}[^"]+))"*,"*(|({user}[^"]+))"*,"*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"*,"*[^"]*"*,"*(|({operation}[^"]+))"*,("*[^"]*"*,){2}"*(|({app}[^"]+))"*,("*[^"]*"*,){2}"*(|({file_path}({file_dir}[^"]+?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?)))"*,"*[^"]*"*,"*(|({bytes}\d+)({bytes_unit}\w+))"*,"""
  
}
```