#### Parser Content
```Java
{
Name = mcafee-wg-str-http-session-mwg
  Vendor = McAfee
  Product = McAfee Web Gateway
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Conditions = [ """ mwg: [""", """Vendor:McAfee""", """] """" ]
  Fields = [
    """\s({host}[\w\-\.]+)\s+mwg:\s+\[({time}\d\d\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d\s+[+-]\d{4})\]\s+"({user}[\w\.\-]{1,40}\$?)"\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({http_response_code}\d+)\s+"({method}\w+)\s+({url}(({protocol}[^:\\\/\s,"]+):[\\\/]+)?(www\.)?(({=dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({web_domain}[^\\\/\s:,"]+))?(:({dest_port}\d+))?({uri_path}\/[^\s\?"]*)?({uri_query}\?[^"\s]*)?)\s+({=protocol}[^"]+)"\s"({categories}({category}[^,"]+)[^"]*)"\s+"[^"]*"\s+"(|({mime}[^"]+))"\s+\S+\s+"(|({user_agent}[^"]+))"(\s+("[^"]*"|\S+)){4}\s+"Vendor:McAfee"""
  ]
  ParserVersion = "v1.0.0"


}
```