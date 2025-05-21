#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-app-activity-success-authactivityauditevent
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = ["epoch_sec", "yyyy-MM-dd'T'HH:mm:ss"]
  Conditions = [ """"eventType":""", """"OperationName":""", """AuthActivityAuditEvent""" ]
  Fields = [
    """"received_time":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)"""
    """"eventCreationTime":\s*({time}\d{10})""",
    """"timestamp":"({time}\d{10})"""",
    """"UTCTimestamp":({time}\d{10})""",
    """"UserId":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """"UserIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"ServiceName":\s*"({app}[^"]+)""",
    """"Success":\s*({result}[^",}]+)"""
    """"OperationName":"({event_name}[^"]+)""""
    """"user_agent":"({user_agent}[^"]+)""""
    """"request_path":"({uri_path}[^"]+)""""
    """"status_code":"({http_response_code}\d+)""""
    """"request_query":"({uri_query}[^"]+)""""
    """"request_method":"({method}[^"]+)""""
    """"cid":"({cid}[^"]+)""""
    """"customerIDString":"({cid}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```