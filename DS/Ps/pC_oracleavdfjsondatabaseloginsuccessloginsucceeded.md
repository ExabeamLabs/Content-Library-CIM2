#### Parser Content
```Java
{
Name = oracle-avdf-json-database-login-success-loginsucceeded
Conditions = [
  """TARGET_TYPE="USER""""
  """ EVENT_NAME="LOGIN SUCCEEDED""""
  """ COMMAND_CLASS="LOGIN""""
  """ SECURED_TARGET_NAME="""
]
ParserVersion = "v1.0.0"

SSSZ"
    Fields = [
          """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
          """"actorName":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[^"]+))"""",
          """"ssoPlatform":"({os}[^"]+)"""",
          """"idcsLastModifiedBy".+?"display":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}[^,"]+,[^"]+))"""",
          """"eventId":"({event_name}[^"]+)"""",
          """"ssoApplicationName":"({app}[^"]+)"""",
          """"message":"({additional_info}[^"]+)"""",
          """"serviceName":"({service_name}[^"]+)"""",
          """"clientIp":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
          """"actorType":"({user_type}[^"]+)""""
    
}
```