#### Parser Content
```Java
{
Name = apache-a-str-http-session-apacheaccess
  Vendor = Apache
  Product = Apache
  ParserVersion = "v1.0.0"
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Conditions = [ """-access""", """ HTTP"""  ]
  Fields = [
  """\s({host}[\w\-.]+)\s+apache-access"""
  """-access:\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s"""
  """\[({time}\d\d\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d\s[+-]\d{4})\]\s+\\?"({method}\w+)\s\\?({url}[^\s]+)\s({protocol}\w+)[^"\s]+"\s({http_response_code}\d+)\s({bytes}\d+)"""
  """(GET|POST|PUT|TUNNEL|OPTIONS|CONNECT|HEAD|DELETE)(?:\s[^\s]+){4}\s\\?"(-|({referrer}[^"]+))\\?"\s\\?"(-|({user_agent}[^"]+))"""
  ]


}
```