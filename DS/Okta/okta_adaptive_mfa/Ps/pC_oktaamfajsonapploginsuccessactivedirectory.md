#### Parser Content
```Java
{
Name = okta-amfa-json-app-login-success-activedirectory
  Conditions = [ """"message"":""Active Directory authentication succeeded""", """"published"":""""" ]
  ParserVersion = "v1.0.0"

q-okta-app-login = {
  Vendor = Okta
  Product = Okta Adaptive MFA
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ExtractionType = json
  Fields = [
    """"published"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """"message"+:"+({event_name}.+?)\s*(\.|\[|")""",
    """"ipAddress"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"displayName"+:"+((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))",[^\{\}]*?"objectType"+:"+User"""",
    """"login"+:"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\{\}]*?"objectType"+:"+User"""",
    """"id"+:"+({user_agent}[^"]+)",[^\{\}]*?"objectType"+:"+Client"""",
    """({app}Okta)""",
    """"displayName"+:"+({app}[^"]+)",[^\{\}]*?"objectType"+:"+AppInstance"""",
    """"categories.*?objectType"+:"+({operation}[^"]+)"""",
    """exa_json_path=$.published,exa_field_name=time"""
    """exa_json_path=$.action.message,exa_field_name=event_name""",
    """exa_regex="ipAddress"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_regex="displayName"+:"+((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))",[^\{\}]*?"objectType"+:"+User""""
    """exa_regex="login"+:"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\{\}]*?"objectType"+:"+User""""
    """exa_json_path=$.actors[*].ipAddress,exa_field_name=src_ip""",
    """exa_json_path=$.actors[*].login,exa_regex=(?:(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s"]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""
    """exa_json_path=$.actors[1].id,exa_field_name=user_agent"""
    """exa_regex=({app}Okta)"""
    """exa_json_path=$.targets.[?(@.objectType == 'AppInstance')].displayName,exa_field_name=app"""
    """exa_json_path=$.action.objectType,exa_field_name=operation"""
  
}
```