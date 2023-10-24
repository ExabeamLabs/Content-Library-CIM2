#### Parser Content
```Java
{
Name = "google-cloudplatform-json-http-session-jsonpayload"
Vendor = "Google"
Product = "Google Cloud Platform"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""""jsonPayload":"""
""""gce_instance""""
"""googleapis.com"""
"""resource_name"""
]
Fields = [
""""timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""""
""""bytes":"({bytes}\d+)""""
""""client":"(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""""
""""method":"(-|({method}[^"]+))""""
""""cache":"({proxy_action}[^"]+)""""
""""status":"({http_response_code}\d+)""""
""""url":"({url}[^"]+)""""
""""user":"({user}[\w\.\-]{1,40}\$?)""""
""""project_id":"({project_id}[^"]+)""""
""""logName":".+squid_({action}[^"]+)""""
""""hierarchy_target":"(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""""
""""zone":"(-|({zone}[^"]+))""""
""""instance_id":"(-|({host}[^"]+))""""
]
ParserVersion = "v1.0.0"


}
```