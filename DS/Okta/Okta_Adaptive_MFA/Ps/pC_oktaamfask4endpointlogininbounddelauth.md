#### Parser Content
```Java
{
Name = okta-amfa-sk4-endpoint-login-inbounddelauth
  Vendor = Okta
  Product = Okta Adaptive MFA
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"actor":""", """"securityContext":""", """"target":""", """"client":""",""""eventType":"app.inbound_del_auth.login_success"""" ]
  Fields=[
    """"published"+\s*:\s*"+({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """({app}(?i)Okta)""",
    """destinationServiceName({app}[^=]+?)\s*\w+=""",
    """"city":"((?i)null|({location_city}[^",]+))""",
    """"state":"((?i)null|({location_state}[^",]+))""",
    """"country":"((?i)null|({location_country}[^",]+))""",
    """"ipAddress"+\s*:\s*"+({src_ip}[^",]+)""",
    """"rawUserAgent"+\s*:\s*"+((?i)unknown|({user_agent}[^",]+))""",
    """"browser"+\s*:\s*"+((?i)unknown|({browser}[^",]+))""",
    """"os"+\s*:\s*"+((?i)unknown|({os}[^",]+))""",
    """"displayMessage"\s*:\s*"((?i)null|({event_name}[^",]+))""",
    """"eventType"\s*:\s*"({operation}[^"]+)""",
    """"legacyEventType"+:"+((?i)null|({operation}[^",]+))""",
    """"outcome":[^\]]*?"result"\s*:\s*"(FAILURE|DENY)","reason":"({failure_reason}[^"]+)""",
    """"reason":"({additional_info}[^"]+)"""
    """"target(s)?"+:[^\}\]]+?"+displayName"+\s*:\s*"+((?i)unknown|({object}[^"]+[^\s]))"""",
    """request"+:.+?User.+?"+displayName"+:(null|"+(Okta System|(?i)unknown|(?:({first_name}[^,"]+),\s*({last_name}[^"]+)|({full_name}[^"]+)))")""",
    """"actor"+.+?"+type"+:"+User.+?displayName"+:(null|"+(Okta System|Okta Admin|(?i)unknown|(?:({last_name}[^,"]+),\s*({first_name}[^"]+)|({full_name}[^"]+))))""",
    """request"+:.+?"+type"+:"+User"+,"+alternateId"+:(null|"+(system@okta\.com|(?:({email_address}[^"@]+@({domain}[^"]+))|(({=domain}[^\\\/]+)[\/\\]+)?({user}[^"]+))))""",
    """"actor"+:[^\]]*?"+type"+:"+User"+,"+alternateId"+\s*:\s*"+(system@okta\.com|(?:({email_address}[^"@]+@({domain}[^"]+))|({user}[^"]+)))"""",
    """requestUri":\s*"({request_uri}[^"]+?)\s*"""",
    """"outcome":[^\]]*?"result"\s*:\s*"({result}[^"]+)"""",
    """outcome":[^\]]*?"result":"?(null|({outcome_result_at}[^\"]+))"?,"reason":"?(null|({outcome_reason_at}[^"]+))""",
  ]
  DupFields = ["failure_reason->additional_info"]
  ParserVersion = "v1.0.0"


}
```