#### Parser Content
```Java
{
Name = "amazon-s3-str-http-session-success-accesslog"
ParserVersion = v1.0.0
Vendor = "Amazon"
Product = "Amazon S3"
TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
Conditions = ["""aws""", """.OBJECT""", """HTTP/""", """ AuthHeader """ ]
Fields = [
"""\w+\s({bucket_name}[^\s]+)\s\[({time}\d{2}\/\w+\/\d{4}:\d{2}:\d{2}:\d{2}\s\+\d+)\]\s(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s(.*?user\/({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+\s({operation}[^\s]+)\s({object}[^\s]+)\s"({url}[^"]+)"\s({http_response_code}\d+)\s(-|({error_code}[^\s]+))\s(-|({bytes_out}\d+))\s({bytes}\d+)\s\d+\s\d+\s"(-|({referrer}[^"]+))"\s"(-|({user_agent}[^"]+))"\s\S+\s\S+\s\S+\s(-|({cipher}[^\s]+))\s(-|({auth_type}[^\s]+))\s(-|({host}[\w\-\.]+))\s(-|({protocol}[^\s]+))\s"""
"""\w+\s({bucket_name}[^\s]+)\s\[({time}\d{2}\/\w+\/\d{4}:\d{2}:\d{2}:\d{2}\s\+\d+)\]\s(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s\S+\s\S+\s({operation}[^\s]+)\s({object}[^\s]+)\s"({url}[^"]+)"\s({http_response_code}\d+)\s(-|({error_code}[^\s]+))\s(-|({bytes_out}\d+))\s({bytes}\d+)\s\d+\s\d+\s"(-|({referrer}[^"]+))"\s"(-|({user_agent}[^"]+))"\s\S+\s\S+\s\S+\s(-|({cipher}[^\s]+))\s(-|({auth_type}[^\s]+))\s(-|({host}[\w\-\.]+))\s(-|({protocol}[^\s]+))\s"""
]


}
```