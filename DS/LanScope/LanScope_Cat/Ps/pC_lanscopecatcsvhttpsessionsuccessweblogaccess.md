#### Parser Content
```Java
{
Name = lanscope-cat-csv-http-session-success-weblogaccess
  ParserVersion = v1.0.0
  Vendor = LanScope
  Product = LanScope Cat
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"Webアクセスログ"""" ]
  Fields = [
     ""","*(|({host}[^"]+))"*,"*(|({user}[^"]+))"*,"*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"*,"*[^"]*"*,"*(|({operation}[^"]+))"*,("*[^"]*"*,){5}"*(|({window_title}[^"]+))"*,"*(|({url}(\w+:\/+)?({web_domain}[^"\/]*?([^"\.\/]+))({uri_path}\/[^"\?]*)?({uri_query}\?[^"]*)?))"*,""""
  ]


}
```