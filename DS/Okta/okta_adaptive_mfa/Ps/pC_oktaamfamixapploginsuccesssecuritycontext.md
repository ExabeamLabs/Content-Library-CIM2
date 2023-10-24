#### Parser Content
```Java
{
Name = "okta-amfa-mix-app-login-success-securitycontext"
  ParserVersion = "v1.0.0"
  Vendor = "Okta"
  Product = "Okta Adaptive MFA"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """"actor":""", """"securityContext":""", """"target":""", """"client":""" ]
  Fields=[
    """"published"\s*:\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """"displayMessage"\s*:\s*"({event_name}(Kerberos[^",]+user)|([^"]+))""",
    """"eventType"\s*:\s*"({operation}[^"]+)""",
    """"legacyEventType":\s*"({operation}[^"]+)"""",
    """actor":\s*\{[^\}]+?alternateId":\s*"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))",[^\}]+?"type":\s*"User"""",
    """actor":\s*\{[^\}]+?"+displayName"+:\s*(null|"+(Okta System|(?:({first_name}[^,"]+),\s*({last_name}[^"]+)|((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))))")[^\}]+?"type":"User"""",
    """actor":\s*\{[^\}]+?"type":"User"[^\}]+?"+displayName"+:\s*(null|"+(Okta System|(?:({first_name}[^,"]+),\s*({last_name}[^"]+)|((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))))")"""
    """actor":\s*\{[^\}]+?displayName":\s*"({full_name}[^"]+)"[^\}]+?type":\s*"User"""",
    """"actor"+.+?"+type"+:\s*"+User.+?displayName"+:\s*(null|"+(Okta System|Okta Admin|(?:({last_name}[^,"]+),\s*({first_name}[^"]+)|((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|AD Agent|({full_name}[^"]+)))))""",
    """"client":[^\]]*?"rawUserAgent"\s*:\s*"((?i)unknown|({user_agent}[^"]+))""",
    """logInfo.request.ipChain.ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"client":[^\]]*?"ipAddress"\s*:\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"request":\s*\{[^\}]+?"ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"outcome":[^\]]*?"result"\s*:\s*"(FAILURE|DENY)","reason":\s*"({failure_reason}[^"]+)""",
    """"outcome":[^\]]*?"result"\s*:\s*"({result}[^"]+)"""",
    """outcome":[^\]]*?"result":\s*"?(null|({outcome_result_at}[^\"]+))"?,"reason":\s*"?(null|({outcome_reason_at}[^"]+))""",
    """({app}(?i)Okta)""",
    """destinationServiceName =({app}[^=]+?)\s*\w+=""",
    """"type":\s*"AppInstance"[^\}\]]*"displayName":\s*"({app}[^"]+?)\s*"""",
    """"geographicalContext":\s*\{[^\}]*?"city":\s*"({location_city}[^"]+)"""",
    """"geographicalContext":\s*\{[^\}]*?"state":\s*"({location_state}[^"]+)"""",
    """"geographicalContext":\s*\{[^\}]*?"country":\s*"({location_country}[^"]+)"""",
    """request"+:.+?"+type"+:\s*"+User"+,"+alternateId"+:\s*(null|"+(system@okta\.com|unknown|(?:({email_address}[^"@]+@({email_domain}[^"]+))|({user}[\w\.\-]{1,40}\$?))))""",
    """\Wsuid=(anonymous|email|system|({email_address}[^@=]+@[^@=]+?)|({user}[\w\.\-]{1,40}\$?))(\s+\w+=|\s*$)""",
    """"actor"+:[^\]]*?"+type"+:\s*"+User"+,"+alternateId"+\s*:\s*"+(system@okta\.com|(?:({email_address}[^"@]+@({email_domain}[^"]+))|({user}[\w\.\-]{1,40}\$?)))"""",
    """suser\\*=({email_address}[^\s@,]+@({email_domain}[^\s@,]+))""",
    """duser\\*=({dest_email_address}[^\s@,]+@({dest_email_domain}[^\s@,]+))""",
    """"privilegeGranted"+\s*:\s*"+({additional_info}[^"]+)""",
    """fname=({group_name}[^=]+)\s+\w+=""",
    """"severity":\s*"({alert_severity}[^"]+)""",
    """"eventType":\s*"({alert_type}[^"]+)""",
    """requestUri":\s*"({request_uri}[^"]+?)\s*"""",
    """target":[^\]]*?"type":\s*"User"[^\}]+?"alternateId"\s*:\s*"(unknown|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({dest_user}[\w\.\-]{1,40}\$?))"""",
    """"target":[^\]]*?"alternateId"\s*:\s*"(unknown|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({dest_user}[\w\.\-]{1,40}\$?))"[^\}]+?"type":\s*"User"""",
    """"target":[^}\]]+?"type"\s*:\s*"(?!User)({object_type}[^"]+)"[^\}]+?"alternateId"\s*:\s*"({object}[^"]+)"""",
    """"target":[^}\]]+?"alternateId"\s*:\s*"({object}[^"]+)"[^\}]+?"type"\s*:\s*"(?!User)({object_type}[^"]+)"""",
    """"domain"+:"+(null|\.|({domain}[^"]+))""""
    """"os":\s*"((?i)unknown|({os}[^"]+))""""
    """"browser":"((?i)UNKNOWN|({browser}[^"]+))""""
    """"deviceFingerprint":\s*"({fingerprint}[^"]+)""""
    """"methodTypeUsed":\s*"({auth_method}[^"]+)""""
  ]
  DupFields = ["outcome_reason_at->additional_info","operation->alert_name"]


}
```