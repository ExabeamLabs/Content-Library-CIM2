#### Parser Content
```Java
{
Name = oracle-pc-json-app-activity-success-appaccess
  ParserVersion = "v1.0.0"
  Conditions = [ """"ssoIdentityProvider":"""",""""eventId":"sso.app.access.success"""",""""serviceName":"SSO"""" ]

oracle-public-cloud-events = {
    Vendor = Oracle
    Product = Oracle Public Cloud
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
          """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
          """"actorName":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""",
          """"ssoPlatform":"({os}[^"]+)"""",
          """"idcsLastModifiedBy".+?"display":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}[^,"]+,[^"]+))"""",
          """"eventId":"({event_name}[^"]+)"""",
          """"ssoApplicationName":"({app}[^"]+)"""",
          """"message":"({additional_info}[^"]+)"""",
          """"serviceName":"({service_name}[^"]+)"""",
          """"clientIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
          """"actorType":"({user_type}[^"]+)""""
          """"ssoUserAgent":"({user_agent}[^"]+)""""
          """"resourceType":"({resource_type}[^"]+)""""
          """"appmgmtAppDisplayName":"({app}[^"]+)""""
          """"actorId":"({user_id}[^"]+)""""
          """"clientName":"({src_host}[\w\-\.]+)""""
          """"appID":"({app_id}[^"]+)""""
    
}
```