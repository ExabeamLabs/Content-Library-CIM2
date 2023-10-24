#### Parser Content
```Java
{
Name = okta-amfa-json-app-login-success-singlesignon-1
  ParserVersion = "v1.0.0"
  Conditions = [ """"displayMessage": "User single sign on to app"""", """"result": "SUCCESS"""" ]

s-okta-app-login = {
  Vendor = "Okta"
  Product = "Okta Adaptive MFA"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"published":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """"userAgent":\s*\{[^\{\}]*?"rawUserAgent":\s*"((?i)unknown|({user_agent}[^"]+))""",
    """"ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"request":\s*\{[^\}]+?"ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"type":\s*"({app}[^"]+)""",
    """({app}Okta)""",
    """destinationServiceName =({app}[^=]+?)\s*\w+=""",
    """"target":\s*\[.*?\{.*?"displayName":\s*"({app}[^"]+)"[^\{\}]*?"type":\s*"AppInstance"""",
    """"type":\s*"AppInstance"[^\}\]]*"displayName":\s*"({app}[^"]+?)\s*"""",
    """"actor":\s*\{[^\{\}]*?"displayName":\s*"((?i)okta[^"]*|unknown|({full_name}[^",]+))"[^\{\}]*?"type":\s*"User"""",
    """"actor":\s*\{[^\{\}]*?"type":\s*"User"[^\{\}]*?"displayName":\s*"((?i)okta[^"]*|unknown|({full_name}[^",]+))"""",
    """"actor"":\s*\{[^\{\}]*?""type"":\s*""User""[^\{\}]*?""displayName"":\s*""((?i)okta[^"]*|unknown|({last_name}[^,]+),\s*({first_name}[^,"\}\]]+))""""
    """"actor":\s*\{[^\{\}]*?"alternateId":\s*"(?:({email_address}[^@"]+@({email_domain}[^@"]+))|({user}[\w\.\-]{1,40}\$?))"""",
    """"userName":\s*"({email_address}[^@"]+@({email_domain}[^@"]+))"""",
    """"outcome":\s*\{[^\{\}]*?"result":\s*"({result}[^"]+)""",
    """"outcome":\s*\{[^\{\}]*?"reason":\s*"({additional_info}[^"]+)""",
    """"displayMessage":\s*"({operation}[^"]+)"""",
    """"city":\s*"({location_city}[^"]+)""",
    """"state":\s*"({location_state}[^"]+)""",
    """"country":\s*"({location_country}[^"]+)"""
    """"dtHash":"({hash_md5}[^"]+)"""
    """"os":\s*"((?i)unknown|({os}[^"]+))""""
    """"browser":\s*"((?i)UNKNOWN|({browser}[^"]+))""""
    """"domain":\s*"(null|\.|({domain}[^"\\},]+))""""
   ] 
 },

  json-okta-auth = {
  Vendor = Okta
  Product = Okta Adaptive MFA
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"published"+\s*:\s*"+({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """({app}(?i)Okta)""",
    """destinationServiceName({app}[^=]+?)\s*\w+=""",
    """"city":"({location_city}[^",]+)""",
    """"state":"({location_state}[^",]+)""",
    """"country":"({location_country}[^",]+)""",
    """"ipAddress"+\s*:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"rawUserAgent"+\s*:\s*"+((?i)unknown|({user_agent}[^"]+))"""",
    """"action"+:.+?"+message"+:"+({operation}({event_name}[^",]+))"""
    """"displayMessage"\s*:\s*"({operation}({event_name}[^",]+))""",
    """"action"+:.+?"+objectType"+:"+({operation}[^",]+)""",
    """"legacyEventType"+:"+({operation}[^",]+)""",
    """"reason":"({failure_reason}[^"]+)"""
    """"target(s)?"+:[^\}\]]+?"+displayName"+\s*:\s*"+((?i)unknown|({object}[^"]+[^\s]))"""",
    """request"+:.+?User.+?"+displayName"+:(null|"+(Okta System|(?i)unknown|(?:({first_name}[^,"]+),\s*({last_name}[^"]+)|({full_name}[^"]+)))")""",
    """"actor"+.+?"+type"+:"+User.+?displayName"+:(null|"+(Okta System|Okta Admin|(?i)unknown|(?:({last_name}[^,"]+),\s*({first_name}[^"]+)|({full_name}[^"]+))))""",
    """"domain"+:"+(null|\.|({domain}[^"]+))"""",
    """"actor":\s*\{[^\}]+?alternateId":\s*"((({user}[\w\.\-]{1,40})@({domain}[^\s"]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({=user}[\w\.\-]{1,40}\$?))",[^\}]+?"type":\s*"User"""",
    """"target":[^\]]*?"alternateId"\s*:\s*"(unknown|(({dest_user}[\w\.\-]{1,40})@({domain}[^\s"]+?\.corp))|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({=dest_user}[\w\.\-]{1,40}\$?))"[^\}]+?"type":\s*"User"""",
    """"request"+:.+?"+type"+:"+User"+,"+alternateId"+:(null|"+(system@okta\.com|(?:(({user}[\w\.\-]{1,40})@({domain}[^\s"]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({=domain}[^\\\/"]+)[\/\\]+)?({=user}[\w\.\-]{1,40}\$?))))""",
    """"actor"+:[^\}]*?"+type"+:"+User"+,"+alternateId"+\s*:\s*"+(system@okta\.com|(?:(({user}[\w\.\-]{1,40})@({domain}[^\s"]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\.\-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*))|({=user}[\w\.\-]{1,40}\$?)))"""",
    """"login":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))""""
    """requestUri":\s*"({request_uri}[^"]+?)\s*"""",
    """"outcome":[^\]]*?"result"\s*:\s*"({result}[^"]+)"""",
    """outcome":[^\]]*?"result":"?(null|({outcome_result_at}[^\"]+))"?,"reason":"?(null|({outcome_reason_at}[^"]+))""",
    """"methodTypeUsed":\s*"({auth_method}[^"]+)""""
    """"dtHash":"({hash_sha256}[^"]+)""""
   ]
   DupFields = ["failure_reason->additional_info"]
 }

  okta-app-activity = {
    Vendor = Okta
    Product = Okta Adaptive MFA
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """\d+:\d+ ({host}[^\s]+) \{""",
    """"published":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """"ipAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"action":\s*\{.*?"objectType":\s*"({operation}[^"]+)".+?\}""",
    """"action":\s*\{.*?"objectType":\s*"[^"]*?({result}error)".+?\}""",
    """"categories":\s*\["({operation}[^"]+)"""",
    """"actors":\[.*?\{.*?"displayName":"((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))"[^\{\}]+?"objectType":"User".*?\}""",
    """"actors":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"displayName":\s*"((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))"""",
    """"displayName":"((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+?))\s*"[^\}\]]*"objectType":"User"""",
    """"actors":\[.*?\{.*?"login":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))"[^\{\}]+?"objectType":"User".*?\}""",
    """"actors":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"login":\s*"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))"""",
    """"targets":\[.*?\{.*?"login":"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-]{1,40}\$?))"[^\{\}]+?"objectType":"User".*?\}""",
    """"targets":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"login":\s*"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-]{1,40}\$?))"""",
    """"actors":\[.*?\{.*?"id":"({user_agent}[^"]+)"[^\{\}]+?"objectType":"Client".*?\}""",
    """"actors":\s*\[\{[^\]]*?"objectType":\s*"Client"[^\]]*?"id":\s*"({user_agent}[^"]+)"""",
    """"message":\s*"({additional_info}[^"]+?)\s*"""",
    """({app}Okta)""",
    """destinationServiceName(=)?({app}.+?)\s*\w+=""",
    """"targets":\[.*?\{.*?"displayName":"({app}[^"]+)"[^\{\}]+?"objectType":"AppInstance".*?\}""",
    """"targets":\s*\[\{[^\]]*?"objectType":\s*"AppInstance"[^\]]*?"displayName":\s*"({app}[^"]+)"""",
    """"type":"AppInstance"[^\}\]]*"displayName":"({app}[^"]+?)\s*"""",
    """requestUri":\s*"({request_uri}[^"]+?)\s*"""",
    """"id":"({object}[^"]+)"[^\}\]]*"objectType":"AppInstance"""",
    """"objectType":"AppInstance"[^\}\]]*"id":"({object}[^"]+)"""",
    ]
    DupFields = ["dest_user->account_name", "additional_info->event_name"
}
```