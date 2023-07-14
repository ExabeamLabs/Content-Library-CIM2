#### Parser Content
```Java
{
Name = microsoft-iis-str-http-session-optionsmapi
  Conditions = [ """ OPTIONS /mapi""" ]
  ParserVersion = "v1.0.0"

iis-web-activity = {
  Vendor = "Microsoft"
  Product = "Microsoft IIS"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """({time}\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2})\s({dest_ip}[\da-fA-F.:]+)\s({method}[^\s]+)\s""",
    """\s\d{2}:\d{2}:\d{2}\s([^\s]+\s){2}({uri_path}[^\s]+)\s(-|({uri_query}[^\s]+))\s({dest_port}\d+)\s(({domain}[^\\"]+)\\)?(-|(S(-\d+){6}-\d+)|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({user}[\w\.\-]{1,40}\$?)(@({=domain}[^\s]+))?))\s[^\s]+\s"?(-|({user_agent}[^\s"]+))"?\s\S+\s({http_response_code}\d+)\s([^\s]+\s){3}(?:[\d\.]+,)?(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))"""
  
}
```