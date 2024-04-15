#### Parser Content
```Java
{
Name = "okta-amfa-cef-app-login-success-userauthverify"
  ParserVersion = "v1.0.0"
  Vendor = "Okta"
  Product = "Okta Adaptive MFA"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """"actor":""", """"securityContext":""", """"target":""", """"client":""", """user.authentication.verify""" ]
  Fields=[
    """"published"\s*:\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """"displayMessage"\s*:\s*"({event_name}[^"]+)""",
    """"eventType"\s*:\s*"({operation}[^"]+)""",
    """actor":\s*\{[^\}]+?alternateId":\s*"({user}[^"]+)",[^\}]+?"type":\s*"User"""",
    """actor":\s*\{[^\}]+?displayName":\s*"({full_name}[^"]+)"[^\}]+?type":\s*"User"""",
    """request"+:[^\]]*?User[^\]]*?"+displayName"+:\s*(null|"+(Okta System|(?:({first_name}[^,"]+),\s*({last_name}[^"]+)|((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))))")""",
    """"actor"+[^\]]*?"+type"+:\s*"+User[^\]]*?displayName"+:\s*(null|"+(Okta System|Okta Admin|(?:({last_name}[^,"]+),\s*({first_name}[^"]+)|((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|AD Agent|({full_name}[^"]+)))))""",
    """"client":[^\]]*?"os"\s*:\s*"((?i)unknown|({os}[^"]+))""",
    """"client":[^\]]*?"rawUserAgent"\s*:\s*"((?i)unknown|({user_agent}[^"]+))""",
    """logInfo.request.ipChain.ip="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"client":[^\]]*?"ipAddress"\s*:\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"request":\s*\{[^\}]+?"ip":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"outcome":[^\]]*?"result"\s*:\s*"(FAILURE|DENY)","reason":\s*"({failure_reason}[^"]+)""",
    """"outcome":[^\]]*?"result"\s*:\s*"({result}[^"]+)"""",
    """({app}(?i)Okta)""",
    """destinationServiceName({app}[^=]+?)\s*\w+=""",
    """"type":\s*"AppInstance"[^\}\]]*"displayName":\s*"({app}[^"]+?)\s*"""",
    """request"+:[^\]]*?"+type"+:\s*"+User"+,"+alternateId"+:\s*(null|"+(system@okta\.com|unknown|(?:({email_address}[^"@]+@({domain}[^"]+))|({user}[^"]+))))""",
    """"actor"+:[^\]]*?"+type"+:\s*"+User"+,"+alternateId"+\s*:\s*"+(system@okta\.com|(?:({email_address}[^"@]+@({domain}[^"]+))|({user}[^"]+)))"""",
    """(s|d)?user\\*=({email_address}[^\s@,]+@({email_domain}[^\s@,]+))""",
    """(s|d)?user\\*=(anonymous|system|({user}[^\s@,]+))(\s|\||,)""",
    """\Wsuid=(anonymous|email|system|({email_address}[^@=]+@[^@=]+?)|({user}[^\s=]+?))(\s+\w+=|\s*$)""",
  ]


}
```