#### Parser Content
```Java
{
Name = "zscaler-pa-json-network-traffic-url"
  ParserVersion = "v1.0.0"
  Vendor = "Zscaler"
  Product = "Zscaler Private Access"
  TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
  Conditions = [ """"Protocol":"HTTP""", """"URL":""", """"Method":""", """"StatusCode":""", """"Customer":"""]
  Fields = [
     """"LogTimestamp":"({time}[^"]+)"""",  
     """({protocol}HTTP(S)?)""",
     """"Method":"({method}[^"]+)"""",
     """"URL":"({url}[^"]+)"""",
     """"UserAgent":"({user_agent}[^"]+)"""",
     """"RequestSize":\s*({bytes_out}\d+)""",
     """"ResponseSize":\s*({bytes_in}\d+)""",
     """"NameID":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""",
     """"StatusCode":({http_response_code}\d+)""",
     """"ClientPublicIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """"ClientPublicPort":({src_port}\d+)""",
     """"ClientPrivateIp":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
     """"ApplicationPort":({dest_port}\d+)""",
     """"ConnectionStatus":"({result}[^"]+)"""",
     """"ConnectionReason":"({failure_reason}[^"]+)""""
  ]


}
```