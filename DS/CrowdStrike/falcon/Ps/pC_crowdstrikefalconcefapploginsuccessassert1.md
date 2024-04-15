#### Parser Content
```Java
{
Name = "crowdstrike-falcon-cef-app-login-success-assert-1"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
  """"eventType":"""
  """"AuthActivityAuditEvent""""
  """"OperationName":"""
  """"saml2Assert""""
]
Fields = [
  """"eventCreationTime":\s*({time}\d{10})"""
  """"timestamp":"({time}\d{10})""""
  """"UTCTimestamp":({time}\d{10})"""
  """"UserId":\s*"({email_address}[^"@]+@({email_domain}[^"@]+))""""
  """"UserIp":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"ServiceName":\s*"({app}[^"]+)"""
  """"Success":\s*({result}[^",}]+)"""
]
ParserVersion = "v1.0.0"


}
```