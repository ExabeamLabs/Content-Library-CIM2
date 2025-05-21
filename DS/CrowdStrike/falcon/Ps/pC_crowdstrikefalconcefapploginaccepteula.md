#### Parser Content
```Java
{
Name = "crowdstrike-falcon-cef-app-login-accepteula"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
  """"eventType":"""
  """"AuthActivityAuditEvent""""
  """"OperationName":"""
  """"selfAcceptEula""""
]
Fields = [
  """"eventCreationTime":\s*({time}\d{10})"""
  """"timestamp":"({time}\d{10})""""
  """"UTCTimestamp":({time}\d{10})"""
  """"UserId":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  """"UserIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"ServiceName":\s*"({app}[^"]+)"""
  """"Success":\s*({result}[^",}]+)"""
  """"cid":"({cid}[^"]+)""""
  """"customerIDString":"({cid}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```