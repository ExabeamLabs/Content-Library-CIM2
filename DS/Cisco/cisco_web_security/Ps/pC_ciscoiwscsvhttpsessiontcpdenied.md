#### Parser Content
```Java
{
Name = cisco-iws-csv-http-session-tcpdenied
    Vendor = Cisco
    Product = "Cisco Web Security"
    TimeFormat = "epoch_sec"
    Conditions = ["""TCP_DENIED""" ,"""AccessLogPush:"""]
    Fields = [
    """AccessLogPush:.+?({time}\d{10}).+?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s({proxy_action}[^\/]+)\/({http_response_code}\d+)\s\d+\s({method}\S+)\s(-|(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(:({dest_port}\d+))?)|({url}(({protocol}[^:\\\/\s,\"]+):[\\\/]+)?({web_domain}[^\\\/\s:,\"]+)(:\d+)?({uri_path}\/[^\s\?\",]*)?({uri_query}\?[^\"\s]*)?))\s(-|\"*(\w+\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)[^\s\"]*\"*))\s(\w+\/)?(-|({=web_domain}\S+))\s(-|({mime}[^\s]+))\s.+?<(-|({category}[^,>]+))"""
    """(\S{3}\s\d\d \d\d:\d\d:\d\d)\s+(\S+\s){9}(?:-|({url}(({protocol}[^:\\\/\s,\"]+):[\\\/]+)?({web_domain}[^\\\/\s:,\"]+)(:({dest_port}\d+))?({uri_path}\/[^\s\?\"]*)?({uri_query}\?[^\"\s]*)?))\s(-|\"*\(Unauthenticated[^\"]+\"*|\"*(\w+\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)[^\s\"]*\"*))\s(\w+\/)?(-|({=web_domain}\S+))\s(-|({mime}[^\s]+))\s.+?<(-|\"*(-|({category}[^,\">]+)))"""
    ]
    ParserVersion = "v1.0.0"
  

}
```