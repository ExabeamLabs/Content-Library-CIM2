#### Parser Content
```Java
{
Name = sailpoint-identitynow-json-app-login-success-ssoapp
  ParserVersion = v1.0.0
  Conditions = [""""type": "SSO""",""""application":""", """"id":"""]
  Fields = ${SailPointParserTemplates.s-sailpoint-activity.Fields} [
    """"application":\s*"({app}[^"]+)"""",
    """"info":\s*"((NONE)|({result}[^"]+))""""
  ]

s-sailpoint-activity = {
  Vendor = Sailpoint
  Product = IdentityNow
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """"hostname":\s*"((\d)|(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(\d+)|({src_host}[^"]+))"""",
    """"datetime":\s*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
    """"action":\s*"({operation}[^"]+)",""",
    """"ipaddr":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"target":\s*"((\d+)|(unknown|Not Available)|(({last_name}[^,"]+),\s*({first_name}[^"]+)))"""",
    """"source":\s*"((\d+)|(unknown|Not Available)|(({last_name}[^,"]+),\s*({first_name}[^"]+)))"""",
    """"target":\s*"((unknown|Not Available)|({full_name}[^\s",]+\s+[^"]+))"""",
    """"source":\s*"((unknown|Not Available)|({full_name}[^\s",]+\s+[^"]+))"""",
    """"target":\s*"((unknown|Not Available)|({user}[^\s,"]+))"""",
    """"source":\s*"((unknown|Not Available)|({user}[^\s,"]+))"""",
    """"id":\s*"({fingerprint}[^"]+)",""",
    """"type":\s*"((NONE)|({event_subtype}[^"]+))""""
  
}
```