#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-app-login-createapi"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
  """"eventType":"""
  """"AuthActivityAuditEvent""""
  """"OperationName":"""
  """"CreateAPIClient""""
]
Fields = [
  """"eventCreationTime":\s*({time}\d{10})"""
  """"timestamp":"({time}\d{10})""""
  """"UTCTimestamp":({time}\d{10})"""
  """"UserId":\s*"({email_address}[^"@]+@({email_domain}[^"@]+))""""
  """"eventCreationTime":({time}\d+)"""
  """"eventCreationTime":\s*({time}\d+)"""
  """"UserId":\s*"({email_address}[^"@]+@[^"@]+)""""
  """"UserId":\s*"({user}[\w\.\-]{1,40}\$?)""""
  """"UserIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"ServiceName":\s*"({app}[^"]+)"""
  """"Success":\s*({result}[^",}]+)"""
  """"OperationName":"({event_name}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```