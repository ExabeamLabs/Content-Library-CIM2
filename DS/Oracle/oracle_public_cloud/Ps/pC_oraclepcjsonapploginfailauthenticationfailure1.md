#### Parser Content
```Java
{
Name = oracle-pc-json-app-login-fail-authenticationfailure-1
  ParserVersion = "v1.0.0"
  Conditions = [ """"ssoIdentityProvider":"""",""""eventId":"sso.authentication.failure"""",""""serviceName\":\"SSO\"""" ]

oracle-public-cloud-events-1 = {
    Vendor = Oracle
    Product = Oracle Public Cloud
    ExtractionType = json
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ssZ"]
    Fields = [
          """exa_json_path=$..eventId,exa_field_name=event_name""",
          """exa_json_path=$..ssoApplicationName,exa_field_name=app""",
          """exa_json_path=$..message,exa_regex="\s*({additional_info}[^"]+?)\s*"""",
          """exa_json_path=$..actorId,exa_field_name=user_id""",
          """exa_json_path=$..clientIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",    
          """exa_regex=created\\":\\"({time}[^\\"]+)""",
          """exa_regex=timestamp\\":\\"({time}[^\\"]+)""",
          """exa_regex=actorName\":\"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
          """exa_regex=ssoPlatform\":\"({os}[^"\\]+)""",
          """exa_regex=idcsLastModifiedBy\":.+?display\":\"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}[^,"\\]+,[^"\\]+))""",
          """exa_regex=serviceName\":\"({service_name}[^\\"]+)""",
          """exa_regex=actorType\":\"({user_type}[^\\"]+)""",
          """exa_regex=ssoUserAgent\":\"({user_agent}[^\\"]+)""",
          """exa_regex=clientName\":\"({src_host}[^\\"]+)"""
    
}
```