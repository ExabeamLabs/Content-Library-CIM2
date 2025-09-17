#### Parser Content
```Java
{
Name = google-cloudplatform-json-http-session-httploadbalancer
  Vendor = Google
  Product = Google Cloud Platform
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [""""type":"http_load_balancer"""",  """"requestMethod":"""","""google.cloud.loadbalancing""", """"target_proxy_name":"""]
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"remoteIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
	  """"requestMethod":"({method}[^"]+)"""",
	  """"requestSize":"({bytes_in}\d+)"""",
	  """"requestUrl":"({url}[^"]+)"""",
	  """"responseSize":"({bytes_out}\d+)"""",
	  """"serverIp":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
	  """"status":({http_response_code}\d+)""",
	  """"outcome":"({result}[^"]+)"""",
	  """"statusDetails":"({additional_info}[^"]+)""""
    """"requestSize":({bytes_in}\d+)"""
  ]
  ParserVersion = v1.0.0


}
```