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
    """actor":\s*\{[^\}]+?alternateId":\s*"({user}[^"]+)",[^\}]+?"type":\s*"User"""",
    """request"+:.+?User.+?"+displayName"+:\s*(null|"+(Okta System|(?:({first_name}[^,"]+),\s*({last_name}[^"]+)|((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))))")""",
    """actor":\s*\{[^\}]+?displayName":\s*"({full_name}[^"]+)"[^\}]+?type":\s*"User"""",
    """"actor"+.+?"+type"+:\s*"+User.+?displayName"+:\s*(null|"+(Okta System|Okta Admin|(?:({last_name}[^,"]+),\s*({first_name}[^"]+)|((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|AD Agent|({full_name}[^"]+)))))""",
    """"client":[^\]]*?"rawUserAgent"\s*:\s*"((?i)unknown|({user_agent}[^"]+))""",
    """logInfo.request.ipChain.ip="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"client":[^\]]*?"ipAddress"\s*:\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"request":\s*\{[^\}]+?"ip":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"outcome":[^\]]*?"result"\s*:\s*"(FAILURE|DENY)","reason":\s*"({failure_reason}[^"]+)""",
    """"outcome":[^\]]*?"result"\s*:\s*"({result}[^"]+)"""",
    """outcome":[^\]]*?"result":\s*"?(null|({outcome_result_at}[^\"]+))"?,"reason":\s*"?(null|({outcome_reason_at}[^"]+))""",
    """"target(s)?"+:[^\}\]]+?"+displayName"+\s*:\s*"+((?i)unknown|({object}[^"]+[^\s]))"""",
    """"target":[^}\]]+?"type"\s*:\s*"({object_type}[^"]+)"""",
    """({app}(?i)Okta)""",
    """destinationServiceName =({app}[^=]+?)\s*\w+=""",
    """"type":\s*"AppInstance"[^\}\]]*"displayName":\s*"({app}[^"]+?)\s*"""",
    """"geographicalContext":\s*\{[^\}]*?"city":\s*"({location_city}[^"]+)"""",
    """"geographicalContext":\s*\{[^\}]*?"state":\s*"({location_state}[^"]+)"""",
    """"geographicalContext":\s*\{[^\}]*?"country":\s*"({location_country}[^"]+)"""",
    """request"+:.+?"+type"+:\s*"+User"+,"+alternateId"+:\s*(null|"+(system@okta\.com|unknown|(?:({email_address}[^"@]+@({domain}[^"]+))|({user}[^"]+))))""",
    """\Wsuid=(anonymous|email|system|({email_address}[^@=]+@[^@=]+?)|({user}[^\s=]+?))(\s+\w+=|\s*$)""",
    """"actor"+:[^\]]*?"+type"+:\s*"+User"+,"+alternateId"+\s*:\s*"+(system@okta\.com|(?:({email_address}[^"@]+@({domain}[^"]+))|({user}[^"]+)))"""",
    """suser\\*=({email_address}[^\s@,]+@({email_domain}[^\s@,]+))""",
    """duser\\*=({dest_email_address}[^\s@,]+@({dest_domain}[^\s@,]+))""",
    """"privilegeGranted"+\s*:\s*"+({additional_info}[^"]+)""",
    """fname=({group_name}[^=]+)\s+\w+=""",
    """"severity":\s*"({alert_severity}[^"]+)""",
    """"eventType":\s*"({alert_type}[^"]+)""",
    """requestUri":\s*"({request_uri}[^"]+?)\s*"""",
    """target":[^\]]*?"type":\s*"User","alternateId"\s*:\s*"(unknown|({dest_email_address}[^"@]+@[^"]+)|({dest_user}[^"]+))""""
    """target":[^\]]*?"type":\s*"AppInstance","alternateId"\s*:\s*"({object}[^"]+)"""
    """"domain"+:"+(null|({domain}[^"]+))"""
  ]
  DupFields = ["domain->email_domain", "outcome_reason_at->additional_info","operation->alert_name"]


}
```