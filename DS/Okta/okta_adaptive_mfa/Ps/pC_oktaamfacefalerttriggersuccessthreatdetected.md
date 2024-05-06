#### Parser Content
```Java
{
Name = okta-amfa-cef-alert-trigger-success-threatdetected
  ParserVersion = v1.0.0
  Conditions = [ """Type":"security.threat.detected""""]
  Fields = ${OktaParserTemplates.json-okta-auth.Fields}[
    """suser=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(anonymous|({user}[\w\.\-]{1,40}\$?)))""",
    """"severity"+:"+({alert_severity}[^",]+)""",
    """({alert_type}application-action)"""
  ]
  DupFields = [ "event_name->alert_name" ]

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
    """outcome":[^\]]*?"result":"?(null|({result}[^\"]+))"?,"reason":"?(null|({result_reason}[^"]+))""",
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
    """exa_regex="outcome":[^\]]*?"result":"?(null|({result}[^\"]+))"?,"reason":"?(null|({result_reason}[^"]+))""",
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