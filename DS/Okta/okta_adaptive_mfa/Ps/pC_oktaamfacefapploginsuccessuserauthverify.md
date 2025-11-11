#### Parser Content
```Java
{
Name = "okta-amfa-cef-app-login-success-userauthverify"
  ParserVersion = "v1.0.0"
  Vendor = "Okta"
  Product = "Okta Adaptive MFA"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"actor":""", """"securityContext":""", """"target":""", """"client":""", """user.authentication.verify""" ]
  Fields=[
    """"published"\s*:\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"displayMessage"\s*:\s*"({event_name}[^"]+)""",
    """"eventType"\s*:\s*"({operation}[^"]+)""",
    """"legacyEventType"\s*:"\s*({operation_details}[^",]+)""",
    """actor":\s*\{[^\}]+?alternateId":\s*"((({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s"]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({=user}[\w\.\-\!\#\^\~]{1,40}\$?))",[^\}]+?"type":\s*"User"""",
    """actor":\s*\{[^\}]+?displayName":\s*"({full_name}[^"]+)"[^\}]+?type":\s*"User"""",
    """request"+:[^\]]*?User[^\]]*?"+displayName"+:\s*(null|"+(Okta System|(?:({first_name}[^,"]+),\s*({last_name}[^"]+)|((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))))")""",
    """"actor"+[^\]]*?"+type"+:\s*"+User[^\]]*?displayName"+:\s*(null|"+(Okta System|Okta Admin|(?:({last_name}[^,"]+),\s*({first_name}[^"]+)|((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|AD Agent|({full_name}[^"]+)))))""",
    """"os":\s*"({os}[^"]+)"""",
    """"client":[^\]]*?"os"\s*:\s*"((?i)unknown|({os}[^"]+))""",
    """"client":[^\]]*?"rawUserAgent"\s*:\s*"((?i)unknown|({user_agent}[^"]+))""",
    """logInfo.request.ipChain.ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"client":[^\]]*?"ipAddress"\s*:\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"request":\s*\{[^\}]+?"ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"risk":"\{reasons=({failure_reason}[^=]+?),\s\w+=""",
    """"outcome":[^\]]*?"result"\s*:\s*"(FAILURE|DENY)","reason":\s*"({failure_reason}[^"]+)""",
    """"outcome":[^\]]*?"result"\s*:\s*"({result}[^"]+)"""",
    """outcome":[^\]]*?"result":"?(null|({result}[^\"]+))"?,"reason":"?(null|({result_reason}[^"]+))""",
    """({app}(?i)Okta)""",
    """"destinationServiceName":"({app}[^",]+)""""
    """"type":\s*"AppInstance"[^\}\]]*"displayName":\s*"({app}[^"]+?)\s*"""",
    """request"+:[^\]]*?"+type"+:\s*"+User"+,"+alternateId"+:\s*(null|"+(system@okta\.com|unknown|(?:(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s",]+?\.corp))|({email_address}[^"@]+@({email_domain}[^"]+))|({=user}[\w\.\-\!\#\^\~]{1,40}\$?))))""",
    """"actor"+:[^\]]*?"+type"+:\s*"+User"+,"+alternateId"+\s*:\s*"+(system@okta\.com|(?:(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s",]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({=user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
    """(s|d)?user\\*=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """(s|d)?user\\*=(anonymous|system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s|\||,)""",
    """\Wsuid=(anonymous|email|system|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)""",
    """"browser":"((?i)UNKNOWN|({browser}[^"]+))""""
    """"deviceFingerprint":"({fingerprint}[^"]+)""""
    """"methodTypeUsed":\s*"({auth_method}[^"]+)""""
    """"debugData":.*?"risk":\s*"[^"]*?level=({severity}[^"\}]+)("|\})"""
    """"request".+?"geographicalContext".+?"country":"({mfa_country}[^"]+)""""
    """"target":\s*\[.*?\{.*?"alternateId":\s*"({app_id}[^"]+)"[^\{\}]*?"type":\s*"AppInstance""""
    """"target":\s*\[.*?\{.*?"displayName":\s*"({app}[^"]+)"[^\{\}]*?"type":\s*"AppInstance""""
    """"city":"({location_city}[^"]+)""",
    """"state":"({location_state}[^"]+)""",
    """"country":"({location_country}[^"]+)""",
    """"behaviors":"\{({more_info}[^\}"]+)\}"""", 
    """"type":\s\"User\"\,\s+\"alternateId\"\:\s\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """exa_json_path=$..published,exa_field_name=time""",
    """exa_json_path=$..displayMessage,exa_field_name=event_name""",
    """exa_json_path=$..eventType,exa_field_name=operation""",
    """exa_json_path=$..legacyEventType,exa_field_name=operation_details,exa_match_expr=!Contains($.legacyEventType,"null")""",
    """exa_regex=actor":\s*\{[^\}]+?alternateId":\s*"((({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s"]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({=user}[\w\.\-\!\#\^\~]{1,40}\$?))",[^\}]+?"type":\s*"User"""",
    """exa_regex=actor":\s*\{[^\}]+?displayName":\s*"({full_name}[^"]+)"[^\}]+?type":\s*"User"""",
    """exa_regex=request"+:[^\]]*?User[^\]]*?"+displayName"+:\s*(null|"+(Okta System|(?:({first_name}[^,"]+),\s*({last_name}[^"]+)|((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))))")""",
    """exa_regex="actor"+[^\]]*?"+type"+:\s*"+User[^\]]*?displayName"+:\s*(null|"+(Okta System|Okta Admin|(?:({last_name}[^,"]+),\s*({first_name}[^"]+)|((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|AD Agent|({full_name}[^"]+)))))""",
    """exa_json_path=$..client.userAgent.os,exa_field_name=os,exa_match_expr=!Contains($.client.userAgent.os,"Unknown","unknown")""",
    """exa_json_path=$..client.userAgent.rawUserAgent,exa_field_name=user_agent""",
    """exa_json_path=$..client.userAgent.browser,exa_field_name=browser,!Contains($.client.userAgent.browser,"UNKNOWN")""",
    """exa_json_path=$..client.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$..request.ipChain[:1].ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.debugContext.debugData.risk,exa_regex=^\{reasons=({failure_reason}[^=]+?),\s\w+=""",
    """exa_regex="outcome":[^\]]*?"result"\s*:\s*"(FAILURE|DENY)","reason":\s*"({failure_reason}[^"]+)""",
    """exa_regex="outcome":[^\]]*?"result"\s*:\s*"({result}[^"]+)"""",
    """exa_regex="outcome":[^\]]*?"result":"?(null|({result}[^\"]+))"?,"reason":"?(null|({result_reason}[^"]+))""",
    """exa_json_path=$.destinationServiceName,exa_field_name=app""",
    """exa_regex="request"+:[^\]]*?"+type"+:\s*"+User"+,"+alternateId"+:\s*(null|"+(system@okta\.com|unknown|(?:(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s",]+?\.corp))|({email_address}[^"@]+@({email_domain}[^"]+))|({=user}[\w\.\-\!\#\^\~]{1,40}\$?))))""",
    """exa_regex="actor"+:[^\]]*?"+type"+:\s*"+User"+,"+alternateId"+\s*:\s*"+(system@okta\.com|(?:(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s",]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({=user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
    """exa_json_path=$.debugContext.debugData.deviceFingerprint,exa_field_name=fingerprint""",
    """exa_json_path=$.target[1:].detailEntry.methodTypeUsed,exa_field_name=auth_method""",
    """exa_json_path=$.debugContext.debugData.risk,exa_regex=^[^"]*?level=({severity}[^"\}]+)("|\})""",
    """exa_json_path=$.request.ipChain[:1].geographicalContext.country,exa_field_name=mfa_country"""
    """exa_regex=({app}(?i)Okta)""",
    """exa_regex="os":\s*"({os}[^"]+)"""",
    """exa_regex="browser":"((?i)UNKNOWN|({browser}[^"]+))""""
    """exa_regex="methodTypeUsed":\s*"({auth_method}[^"]+)""""
    """exa_regex="target":\s*\[.*?\{.*?"alternateId":\s*"({app_id}[^"]+)"[^\{\}]*?"type":\s*"AppInstance""""
    """exa_regex="target":\s*\[.*?\{.*?"displayName":\s*"({app}[^"]+)"[^\{\}]*?"type":\s*"AppInstance""""
    """exa_json_path=$..client.geographicalContext.city,exa_field_name=location_city""",
    """exa_json_path=$..client.geographicalContext.state,exa_field_name=location_state""",
    """exa_json_path=$..client.geographicalContext.country,exa_field_name=location_country""",
    """exa_json_path=$.debugContext.debugData.behaviors,exa_field_name=more_info"""
    """exa_regex="type":\s\"User\"\,\s+\"alternateId\"\:\s\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  ]


}
```