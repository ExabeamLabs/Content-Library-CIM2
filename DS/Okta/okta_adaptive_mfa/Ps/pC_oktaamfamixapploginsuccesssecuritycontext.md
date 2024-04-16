#### Parser Content
```Java
{
Name = "okta-amfa-mix-app-login-success-securitycontext"
  ParserVersion = "v1.0.0"
  Vendor = "Okta"
  Product = "Okta Adaptive MFA"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"actor":""", """"securityContext":""", """"target":""", """"client":""" ]
  Fields=[
    """"published"\s*:\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"displayMessage"\s*:\s*"({event_name}(Kerberos[^",]+user)|([^"]+))""",
    """"eventType"\s*:\s*"({operation_details}[^"]+)""",
    """"legacyEventType":\s*"({operation}[^"]+)"""",
    """suser\\*=suser\\*=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""
    """duser\\*=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(?<!corp)(?<!local)(?<!loc)(?<!localdomain)\s\w+=""",
   """actor":\s*\{[^\}]+?alternateId":\s*"(unknown|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))(?<!corp)(?<!local)(?<!loc)(?<!localdomain)|(({user}[\w\.\-]{1,40})(@({domain}[^\s"]+?))?))",[^\}]+?"type":\s*"User"""",
   """\Wsuid=(anonymous|email|system|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))(\s+\w+=|\s*$)""",
   """"actor"+:[^\]\}]*?"+type"+:\s*"+User"+,"+alternateId"+\s*:\s*"+(system@okta\.com|unknown|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))(?<!corp)(?<!local)(?<!loc)(?<!localdomain)|(({user}[\w\.\-]{1,40})(@({domain}[^\s"]+?))?))"""",
    """actor":\s*\{[^\}]+?"+displayName"+:\s*(null|"+(Okta System|(?:({first_name}[^,"]+),\s*({last_name}[^"]+)|((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|_oktaadagent|({full_name}[^"]+))))")[^\}]+?"type":"User"""",
    """actor":\s*\{[^\}]+?"type":"User"[^\}]+?"+displayName"+:\s*(null|"+(Okta System|(?:({first_name}[^,"]+),\s*({last_name}[^"]+)|((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|_oktaadagent|({full_name}[^"]+))))")"""
    """actor":\s*\{[^\}]+?displayName":\s*"({full_name}[^"]+)"[^\}]+?type":\s*"User"""",
    """actor":\s*\{[^\}]+?"+type"+:\s*"+User.+?displayName"+:\s*(null|"+(Okta System|Okta Admin|(?:({last_name}[^,"]+),\s*({first_name}[^"]+)|((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|AD Agent|_oktaadagent|({full_name}[^"]+)))))""",
    """"client":[^\]]*?"rawUserAgent"\s*:\s*"((?i)unknown|({user_agent}[^"]+))""",
    """logInfo.request.ipChain.ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"client":[^\]]*?"ipAddress"\s*:\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"request":\s*\{[^\}]+?"ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"outcome":[^\]]*?"result"\s*:\s*"(FAILURE|DENY)","reason":\s*"({failure_reason}[^"]+)""",
    """"outcome":[^\]]*?"result"\s*:\s*"({result}[^"]+)"""",
    """outcome":[^\]]*?"result":\s*"?(null|({outcome_result_at}[^\"]+))"?,"reason":\s*"?(null|({outcome_reason_at}[^"]+))""",
    """destinationServiceName =({app}[^=]+?)\s*\w+=""",
    """({app}(?i)Okta|Microsoft Office 365)""",
    """"type":\s*"AppInstance"[^\}\]]*"displayName":\s*"({app}[^"]+?)\s*"""",
    """"actor":.+?"displayName":\s*"({app}[^"]+).+?"type":\s*"PublicClientApp"""",
    """"geographicalContext":\s*\{[^\}]*?"city":\s*"({location_city}[^"]+)"""",
    """"geographicalContext":\s*\{[^\}]*?"state":\s*"({location_state}[^"]+)"""",
    """"geographicalContext":\s*\{[^\}]*?"country":\s*"({location_country}[^"]+)"""",
    """"privilegeGranted"+\s*:\s*"+({additional_info}[^"]+)""",
    """fname=({group_name}[^=]+)\s+\w+=""",
    """"severity":\s*"({alert_severity}[^"]+)""",
    """"eventType":\s*"({alert_type}[^"]+)""",
    """requestUri":\s*"({request_uri}[^"]+?)\s*"""",
      """"target":[^\]\}]*?"type":\s*"User"[^\}]+?"alternateId"\s*:\s*"(unknown|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))(?<!corp)(?<!local)(?<!loc)(?<!localdomain)|(({dest_user}[\w\.\-]{1,40})(@({dest_domain}[^\s"]+?))?))""""
      """"target":[^\]\}]*?"alternateId"\s*:\s*"(unknown|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))(?<!corp)(?<!local)(?<!loc)(?<!localdomain)|(({dest_user}[\w\.\-]{1,40})(@({dest_domain}[^\s"]+?))?))"[^\}]+?"type":\s*"User"""",
      """"target":[^}\]]+?"type"\s*:\s*"(?!User)({object_type}[^"]+)"[^\}]+?"alternateId"\s*:\s*"({object}[^"]+)"""",
    """"target":[^}\]]+?"alternateId"\s*:\s*"({object}[^"]+)"[^\}]+?"type"\s*:\s*"(?!User)({object_type}[^"]+)"""",
    """"domain"+:"+(null|\.|({domain}[^"\/]+))"""
    """"os":\s*"((?i)unknown|({os}[^"]+))""""
    """"browser":"((?i)UNKNOWN|({browser}[^"]+))""""
    """"deviceFingerprint":\s*"({fingerprint}[^"]+)""""
    """"methodTypeUsed":\s*"({auth_method}[^"]+)""""
    """"debugData":.*?"risk":\s*"[^"]*?level=\s*({severity}[^"\}]+)("|\})"""
    """exa_json_path=$.published,exa_field_name=time""",
    """exa_json_path=$.displayMessage,exa_regex=({event_name}(Kerberos[^",]+user)|([^"]+))""",
    """exa_json_path=$.eventType,exa_field_name=operation_details""",
    """exa_json_path=$.legacyEventType,exa_field_name=operation,exa_match_expr=!Contains($.legacyEventType,"null")""",
    """exa_regex=actor":\s*\{[^\}]+?alternateId":\s*"(unknown|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))(?<!corp)(?<!local)(?<!loc)(?<!localdomain)|(({user}[\w\.\-]{1,40})(@({domain}[^\s"]+?))?))",[^\}]+?"type":\s*"User"""",
    """exa_regex="actor"+:[^\]\}]*?"+type"+:\s*"+User"+,"+alternateId"+\s*:\s*"+(system@okta\.com|unknown|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))(?<!corp)(?<!local)(?<!loc)(?<!localdomain)|(({user}[\w\.\-]{1,40})(@({domain}[^\s"]+?))?))"""",
    """exa_regex=actor":\s*\{[^\}]+?"+displayName"+:\s*(null|"+(Okta System|(?:({first_name}[^,"]+),\s*({last_name}[^"]+)|((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))))")[^\}]+?"type":"User"""",
    """exa_regex=actor":\s*\{[^\}]+?"type":"User"[^\}]+?"+displayName"+:\s*(null|"+(Okta System|(?:({first_name}[^,"]+),\s*({last_name}[^"]+)|((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))))")"""
    """exa_regex=actor":\s*\{[^\}]+?displayName":\s*"({full_name}[^"]+)"[^\}]+?type":\s*"User"""",
    """exa_regex=actor":\s*\{[^\}]+?"+type"+:\s*"+User.+?displayName"+:\s*(null|"+(Okta System|Okta Admin|(?:({last_name}[^,"]+),\s*({first_name}[^"]+)|((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|AD Agent|({full_name}[^"]+)))))""",
    """exa_json_path=$.client.userAgent.rawUserAgent,exa_field_name=user_agent""",
    """exa_json_path=$.client.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.request.ipChain[:1].ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_regex="outcome":[^\]]*?"result"\s*:\s*"(FAILURE|DENY)","reason":\s*"({failure_reason}[^"]+)""",
    """exa_regex="outcome":[^\]]*?"result"\s*:\s*"({result}[^"]+)"""",
    """exa_regex="outcome":[^\]]*?"result":\s*"?(null|({outcome_result_at}[^\"]+))"?,"reason":\s*"?(null|({outcome_reason_at}[^"]+))""",
    """exa_json_path=$.actor.displayName,exa_field_name=full_name,exa_match_expr=Contains($.actor.type,"User")""",
    """exa_json_path=$.actor.displayName,exa_field_name=app,exa_match_expr=Contains($.actor.type,"PublicClientApp")""",
    """exa_json_path=$.actor.alternateId,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.client.geographicalContext.city,exa_field_name=location_city""",
    """exa_json_path=$.client.geographicalContext.state,exa_field_name=location_state""",
    """exa_json_path=$.client.geographicalContext.country,exa_field_name=location_country""",
    """exa_json_path=$.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.eventType,exa_field_name=alert_type""",
    """exa_json_path=$.debugContext.debugData.requestUri,exa_field_name=request_uri""",
    """exa_regex="target":[^\]\}]*?"type":\s*"User"[^\}]+?"alternateId"\s*:\s*"(unknown|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))(?<!corp)(?<!local)(?<!loc)(?<!localdomain)|(({dest_user}[\w\.\-]{1,40})(@({dest_domain}[^\s"]+?))?))""""
    """exa_regex="target":[^\]\}]*?"alternateId"\s*:\s*"(unknown|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))(?<!corp)(?<!local)(?<!loc)(?<!localdomain)|(({dest_user}[\w\.\-]{1,40})(@({dest_domain}[^\s"]+?))?))"[^\}]+?"type":\s*"User"""",
    """exa_regex="target":[^}\]]+?"type"\s*:\s*"(?!User)({object_type}[^"]+)"[^\}]+?"alternateId"\s*:\s*"({object}[^"]+)"""",
    """exa_regex="target":[^}\]]+?"alternateId"\s*:\s*"({object}[^"]+)"[^\}]+?"type"\s*:\s*"(?!User)({object_type}[^"]+)"""",
    """exa_json_path=$.client.userAgent.browser,exa_regex=((?i)UNKNOWN|({browser}[^"]+))""",
    """exa_json_path=$.client.userAgent.os,exa_field_name=os,exa_match_expr=!Contains($.client.userAgent.os,"unknown")""",
    """exa_json_path=$.debugContext.debugData.deviceFingerprint,exa_field_name=fingerprint""",
    """exa_json_path=$.target[1:].detailEntry.methodTypeUsed,exa_field_name=auth_method""",
    """exa_json_path=$.debugContext.debugData.risk,exa_regex=^[^"]*?level=({severity}[^"\}]+)("|\})""",
    """exa_regex="domain"+:"+(null|\.|({domain}[^"\/]+))""",
    """exa_regex=({app}(?i)Okta|Microsoft Office 365)""",
  ]
  DupFields = ["outcome_reason_at->additional_info","operation->alert_name"]


}
```