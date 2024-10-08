#### Parser Content
```Java
{
Name = google-cloudplatform-sk4-http-session-http
Vendor = "Google"
Product = "Google Cloud Platform"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [ """"httpRequest":{"""", """"insertId":"""" ]
Fields = [
""""timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
""""remoteIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
""""requestMethod":"({method}[^"]+)""""
""""cache":"({proxy_action}[^"]+)""""
""""status":"*({http_response_code}\d+)"""
""""requestUrl":"({url}[^"]+)""""
""""user":"({user}[\w\.\-]{1,40}\$?)""""
""""protocol":"({protocol}[^"]+)""""
""""project_id":"({project_id}[^"]+)""""
""""requestSize":"({bytes_in}\d+)"""",
""""serverIp":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
""""responseSize":"({bytes_out}\d+)"""",
""""userAgent":"({user_agent}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```