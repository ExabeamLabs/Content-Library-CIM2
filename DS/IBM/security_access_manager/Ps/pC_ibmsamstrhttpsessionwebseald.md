#### Parser Content
```Java
{
Name = "ibm-sam-str-http-session-webseald"
Vendor = "IBM"
Product = "Security Access Manager"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """-webseald """
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)-\d\d:\d\d\s({host}[^\s]+)\s"""
  """webseald\s\d+\s(.*?\s){4}(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """"({request}({method}[^\s]+)\sHTTPS*:\/\/({url}[^\s]+))\s({protocol}[^\/]+).*?\"\s({http_response_code}\d+)\s(-|\d+)\s.*?\s(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
]
ParserVersion = "v1.0.0"


}
```