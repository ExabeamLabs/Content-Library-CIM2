#### Parser Content
```Java
{
Name = okta-amfa-json-app-login-success-oauth2signon
  ParserVersion = "v1.0.0"
  Conditions = [ """"eventType": "app.oauth2.signon"""" ]

s-okta-app-login = {
  Vendor = "Okta"
  Product = "Okta Adaptive MFA"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ExtractionType = json
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
    """"type":\s*"AppInstance"(,\s"[^"]+":\s\{[^\}]+\},\s|[^\]\}]*)"displayName":\s*"({app}[^"]+?)\s*"""",
    """"type":\s*"AppUser"[^\}\]]"alternateId":\s*"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({dest_user}[^"]+?))\s*""""
    """"alternateId":\s*"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({dest_user}[^",]+?))",\s*?"type":\s*"AppUser""""
    """"actor":\s*\{[^\{\}]*?"displayName":\s*"((?i)okta[^"]*|unknown|({full_name}[^",]+))"[^\{\}]*?"type":\s*"User"""",
    """"actor":\s*\{[^\{\}]*?"type":\s*"User"[^\{\}]*?"displayName":\s*"((?i)okta[^"]*|unknown|({full_name}[^",]+))"""",
    """"actor"":\s*\{[^\{\}]*?""type"":\s*""User""[^\{\}]*?""displayName"":\s*""((?i)okta[^"]*|unknown|({last_name}[^,]+),\s*({first_name}[^,"\}\]]+))""""
    """"actor":\s*\{[^\{\}]*?"alternateId":\s*"(?:(({user}[\w\.\-]{1,40})@({domain}[^\s"]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({=user}[\w\.\-]{1,40}\$?))"""",
    """"userName":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """"outcome":\s*\{[^\{\}]*?"result":\s*"({result}[^"]+)""",
    """outcome":[^\]]*?"result":"?(null|({outcome_result_at}[^\"]+))"?,"reason":"?(null|({outcome_reason_at}[^"]+))""",
    """"displayMessage":\s*"({operation}[^"]+)"""",
    """"displayMessage"\s*:\s*"((?i)null|({event_name}[^",]+))""",
    """"city":\s*"({location_city}[^"]+)""",
    """"state":\s*"({location_state}[^"]+)""",
    """"country":\s*"({location_country}[^"]+)"""
    """"dtHash":"({hash_sha256}[^"]+)"""
    """"os":\s*"((?i)unknown|({os}[^"]+))""""
    """"browser":\s*"((?i)UNKNOWN|({browser}[^"]+))""""
    """"domain":\s*"(null|\.|({domain}[^"\\},]+))""""
    """exa_json_path=$.published,exa_field_name=time""",
    """exa_regex=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """exa_json_path=$.client.userAgent.rawUserAgent,exa_field_name=user_agent,exa_match_expr=!Contains($.client.userAgent.rawUserAgent,"unknown")"""
    """exa_regex=({app}Okta)"""
    """exa_json_path=$.outcome.result,exa_field_name=result""",
    """exa_json_path=$.outcome.reason,exa_field_name=additional_info""",
    """exa_json_path=$.client.geographicalContext.city,exa_field_name=location_city""",
    """exa_json_path=$.client.geographicalContext.state,exa_field_name=location_state""",
    """exa_json_path=$.client.geographicalContext.country,exa_field_name=location_country""",
    """exa_json_path=$.displayMessage,exa_field_name=operation""",
    """exa_json_path=$.client.userAgent.os,exa_field_name=os,exa_match_expr=!Contains(toLower($.client.userAgent.os),"unknown")"""
    """exa_json_path=$.client.userAgent.browser,exa_field_name=browser,exa_match_expr=!Contains(toLower($.client.userAgent.browser),"unknown")"""
    """exa_json_path=$.request.ipChain.ip,exa_field_name=src_ip""",
    """exa_json_path=$.actor.displayName,exa_field_name=full_name,exa_match_expr=InList(toLower($.actor.type),"user")"""
    """exa_json_path=$.client.ipAddress,exa_field_name=src_ip""",
    """exa_json_path=$.target[*].alternateId,exa_regex=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))\s*""""
    """exa_json_path=$.target[*].alternateId,exa_regex=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({dest_user}[^",]+?))",\s*?"type":\s*"AppUser""""
    """exa_json_path=$.actor.alternateId,exa_regex=(?:(({user}[\w\.\-]{1,40})@({domain}[^\s"]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({=user}[\w\.\-]{1,40}\$?))"""
    """exa_json_path=$.securityContext.domain,exa_field_name=domain,exa_match_expr=!InList($.securityContext.domain, 'null' , '.' )""",
    """exa_regex="target":\s*\[.*?\{.*?"displayName":\s*"({app}[^"]+)"[^\{\}]*?"type":\s*"AppInstance"""",
    """exa_regex="type":\s*"AppInstance"(,\s"[^"]+":\s\{[^\}]+\},\s|[^\]\}]*)"displayName":\s*"({app}[^"]+?)\s*"""",
    """"eventType":\s*"({operation_details}[^"]+)""""
    """"legacyEventType":\s*"({operation}[^"]+)""""
    """"debugData":.*?"risk":\s*"[^"]*?level=({severity}[^"\}]+)("|\})"""
    """exa_json_path=$.debugContext.debugData.risk,exa_regex=\s*level=({severity}[^"\}]+)("|\})"""
    """exa_json_path=$.eventType,exa_field_name=operation_details""",
    """exa_json_path=$.legacyEventType,exa_field_name=operation""",
    """exa_json_path=$.debugContext.debugData.dtHash,exa_field_name=hash_sha256""",
    """exa_json_path=$.outcome.result,exa_field_name=outcome_result_at,exa_match_expr=!Contains(toLower($.outcome.result),"null")"""
    """exa_json_path=$.outcome.reason,exa_field_name=outcome_reason_at,exa_match_expr=!Contains(toLower($.outcome.reason),"null")"""
    """exa_json_path=$.displayMessage,exa_field_name=event_name"""
   ] 
 },

  json-okta-auth = {
  Vendor = Okta
  Product = Okta Adaptive MFA
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"published"+\s*:\s*"+({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """({app}(?i)Okta)""",
    """destinationServiceName =({app}[^=]+?)\s*\w+=""",
    """"city":"({location_city}[^",]+)""",
    """"state":"({location_state}[^",]+)""",
    """"country":"({location_country}[^",]+)""",
    """"ipAddress"+\s*:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"rawUserAgent"+\s*:\s*"+((?i)unknown|({user_agent}[^"]+))"""",
    """"action"+:.+?"+message"+:"+({operation}({event_name}[^",]+))"""
    """"displayMessage"\s*:\s*"({operation}({event_name}[^",]+))""",
    """"action"+:.+?"+objectType"+:"+({operation}[^",]+)""",
    """"eventType":\s*"({operation_details}[^"]+)"""",
    """"legacyEventType"+:"+({operation}[^",]+)""",
    """"reason":"({failure_reason}[^"]+)"""
    """"target(s)?"+:[^\}\]]+?"+displayName"+\s*:\s*"+((?i)unknown|({object}[^"]+[^\s]))"""",
    """request"+:.+?User.+?"+displayName"+:(null|"+(Okta System|(?i)unknown|(?:({first_name}[^,"]+),\s*({last_name}[^"]+)|({full_name}[^"]+)))")""",
    """"actor"+.+?"+type"+:"+User.+?displayName"+:(null|"+(Okta System|Okta Admin|(?i)unknown|(?:({last_name}[^,"]+),\s*({first_name}[^"]+)|({full_name}[^"]+))))""",
    """"actor"+.+?"+[^}]+?displayName"+:(null|"+(Okta System|Okta Admin|(?i)unknown|(?:({last_name}[^,"]+),\s*({first_name}[^"]+)|({full_name}[^"]+))))[^\}]+?type":"User"""",
    """"domain"+:"+(null|\.|\.?({domain}[^"]+))"""",
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
    """"debugData":.*?"risk":\s*"[^"]*?level=({severity}[^"\}]+)("|\})"""
    """"os":\s*"({os}[^"]+)""""
    """exa_json_path=$.published,exa_field_name=time""",
    """exa_json_path=$.destinationServiceName,exa_field_name=app""",
    """exa_json_path=$.client.geographicalContext.city,exa_field_name=location_city""",
    """exa_json_path=$.client.geographicalContext.state,exa_field_name=location_state""",
    """exa_json_path=$.client.geographicalContext.country,exa_field_name=location_country""",
    """exa_json_path=$.client.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.client.userAgent.rawUserAgent,exa_field_name=user_agent""",
    """exa_json_path=$.displayMessage,exa_field_name=operation""",
    """exa_json_path=$.displayMessage,exa_field_name=event_name""",
    """exa_json_path=$.eventType,exa_field_name=operation_details""",
    """exa_json_path=$.legacyEventType,exa_field_name=operation""",
    """exa_json_path=$.outcome.reason,exa_field_name=failure_reason""",
    """exa_regex="target(s)?"+:[^\}\]]+?"+displayName"+\s*:\s*"+((?i)unknown|({object}[^"]+[^\s]))"""",
    """exa_regex=request"+:.+?User.+?"+displayName"+:(null|"+(Okta System|(?i)unknown|(?:({first_name}[^,"]+),\s*({last_name}[^"]+)|({full_name}[^"]+)))")""",
    """exa_regex="actor"+.+?"+type"+:"+User.+?displayName"+:(null|"+(Okta System|Okta Admin|(?i)unknown|(?:({last_name}[^,"]+),\s*({first_name}[^"]+)|({full_name}[^"]+))))""",
    """exa_regex="actor"+.+?"+[^}]+?displayName"+:(null|"+(Okta System|Okta Admin|(?i)unknown|(?:({last_name}[^,"]+),\s*({first_name}[^"]+)|({full_name}[^"]+))))[^\}]+?type":"User"""",
    """exa_regex="domain"+:"+(null|\.|\.?({domain}[^"]+))"""",    
    """exa_regex="actor":\s*\{[^\}]+?alternateId":\s*"((({user}[\w\.\-]{1,40})@({domain}[^\s"]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({=user}[\w\.\-]{1,40}\$?))",[^\}]+?"type":\s*"User"""",
    """exa_regex="target":[^\]]*?"alternateId"\s*:\s*"(unknown|(({dest_user}[\w\.\-]{1,40})@({domain}[^\s"]+?\.corp))|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({=dest_user}[\w\.\-]{1,40}\$?))"[^\}]+?"type":\s*"User"""",
    """exa_regex="request"+:.+?"+type"+:"+User"+,"+alternateId"+:(null|"+(system@okta\.com|(?:(({user}[\w\.\-]{1,40})@({domain}[^\s"]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({=domain}[^\\\/"]+)[\/\\]+)?({=user}[\w\.\-]{1,40}\$?))))""",
    """exa_regex="actor"+:[^\}]*?"+type"+:"+User"+,"+alternateId"+\s*:\s*"+(system@okta\.com|(?:(({user}[\w\.\-]{1,40})@({domain}[^\s"]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\.\-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*))|({=user}[\w\.\-]{1,40}\$?)))"""",
    """exa_json_path=$.debugContext.debugData.requestUri,exa_field_name=request_uri""",
    """exa_json_path=$.outcome.result,exa_field_name=result""",
    """exa_regex="outcome":[^\]]*?"result":"?(null|({outcome_result_at}[^\"]+))"?,"reason":"?(null|({outcome_reason_at}[^"]+))""",
    """exa_json_path=$.target[1:].detailEntry.methodTypeUsed,exa_field_name=auth_method""",
    """exa_json_path=$.debugContext.debugData.dtHash,exa_field_name=hash_sha256""",
    """exa_json_path=$.debugContext.debugData.risk,exa_regex=^[^"]*?level=({severity}[^"\}]+)("|\})""",
    """exa_json_path=$.client.userAgent.os,exa_field_name=os"""
   ]
   DupFields = ["failure_reason->additional_info", "location_country->mfa_country"]
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