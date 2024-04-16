#### Parser Content
```Java
{
Name = amazon-awscloudwatch-sk4-http-session-awscloudfront
  Vendor = "Amazon"
  Product = "AWS CloudWatch"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """CEF:"""
    """ https """
    """AWS_CLOUDFRONT"""
  ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\s\S+\s({bytes_in}\d+)\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s({method}\S+)\s({src_host}[\w\-\.]+)\s({uri_path}[^\s]+)\s({http_response_code}\d+)\s({referrer}[^\s]+)\s({user_agent}[^\s]+)\s(-|({uri_query}[^\s]+))\s\S*\s({result}[^\s]+)\s(\S*\s){2}({protocol}[^\s]+)\s({bytes_out}\d+)\s(\S*\s){11}(-|({mime}[^\s]+))"""
  ]
  ParserVersion = "v1.0.0"


}
```