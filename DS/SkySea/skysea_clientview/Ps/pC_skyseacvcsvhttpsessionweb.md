#### Parser Content
```Java
{
Name = "skysea-cv-csv-http-session-web"
  Vendor = SkySea
  Product = SkySea ClientView
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """,Webアクセス,""" ]
  Fields = [
    """({host}[\w\-.]+),\d+,({src_host}[\w\-.]+),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,[^,]*,({user}[\w\.\-\!\#\^\~]{1,40}\$?),({full_name}[^,\(\（]+(\（[^\）,]+\）)?)({department}[^,]+)[^,]*,({time}\d+\/\d+\/\d+ \d+:\d+:\d+),Webアクセス,([^,]*,){2}(-|({url}(({protocol}[^:\\\/\s,"]+):[\\\/]+)?({web_domain}[^\\\/\s:,"]+)(:\d+)?({uri_path}\/[^\s\?",]*)?({uri_query}\?[^"\s,]*)?)),([^,]*,){5}({action}[^,]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```