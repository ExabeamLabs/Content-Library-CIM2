#### Parser Content
```Java
{
Name = amazon-awselb-str-http-session-elasticloadbalancing
 ParserVersion = v1.0.0
 Vendor = Amazon
 Product = AWS Elastic Load Balancer
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
 Conditions = [ """arn:aws:elasticloadbalancing:""", """HTTP/""" ]
 Fields = [
   """(cs6=)?({connection_type}[^\s\=]+)\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\dZ)\s+\S+\s+(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+)))\s+(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+)))\s+(\S+\s){4}(-|({http_response_code}\d+))\s+(-|({bytes_in}\d+))\s+(-|({bytes_out}\d+))\s+"(-|({method}\w+))\s+(-|({url}[^\s]+))\s\S+"\s"(-|({user_agent}[^"]+))"\s(-|({cipher}[^\s]+))\s(-|({protocol}[^\s]+))\s(-|({group_arn}[^\s]+))\s"(-|({tracking_id}[^"]+))"\s"(-|({web_domain}[^"]+))"\s"(-|({session_arn}[^"]+))"(\s[^\s]+){2}\s"(|-|({action}[^"]+))"\s"(-|({redirect_url}[^"]+))"\s"(-|({failure_reason}[^"]+))"\s"""
]


}
```