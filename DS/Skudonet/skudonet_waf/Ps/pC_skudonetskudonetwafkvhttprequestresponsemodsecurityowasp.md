#### Parser Content
```Java
{
Name = "skudonet-skudonetwaf-kv-http-request-response-modsecurityowasp"
ParserVersion = "v1.0.0"
Vendor = "Skudonet"
Product = "Skudonet WAF"
TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
event_timeFormat = ["MMM dd HH:mm:ss"]
Conditions = [
"""SKUDONET"""
"""ModSecurity"""
"""severity"""
"""OWASP_CRS"""
]
  Fields = [
    """"time_stamp":"({time}\w+ \w+ \d+ \d\d:\d\d:\d\d \d\d\d\d)"""
    """"client_ip":"(null|-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""""
    """"host_ip":"(null|-|({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))?)""""
    """"client_port":({src_port}\d+)"""
    """"host_port":({dest_port}\d+)"""
    """"method":"({method}[^"]+)","""
    """"uri":"({uri_path}[^"]+)""""
    """"file":"({file_url}[^"]+)""""
    """"severity":"({alert_severity}[^"]+)""""
    """"message":"({additional_info}[^"]+)""""
    """"http_code":({http_response_code}\d+)"""
    """unique_id":({alert_id}[^"]+)"""
    """"Content-Type":"({mime}[^";]+)"""
    """"ver":"({user_agent}[^"]+)"""
    """({event_time}\w+\s\d+\s\d+:\d+:\d+)\s({server}[^"\s]+)\s"""
    """pound:\s*({policy_id}[^",]+),\s*"""
  ]


}
```