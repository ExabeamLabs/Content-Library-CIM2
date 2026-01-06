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
    """({app}Okta)""",
    """destinationServiceName({app}[^=]+?)\s*\w+=""",
    """"city":"(null|({location_city}[^",]+))""",
    """"state":"(null|({location_state}[^",]+))""",
    """"country":"(null|({location_country}[^",]+))""",
    """"ipAddress"+\s*:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"rawUserAgent"+\s*:\s*"+(unknown|({user_agent}[^",]+))""",
    """"browser"+\s*:\s*"+(unknown|({browser}[^",]+))""",
    """"os"+\s*:\s*"+(unknown|({os}[^",]+))""",
    """"displayMessage"\s*:\s*"(null|({event_name}[^",]+))""",
    """"eventType"\s*:\s*"({operation}[^"]+)""",
    """"legacyEventType"+:"+(null|({operation_details}[^",]+))""",
    """"outcome":[^\]]*?"result"\s*:\s*"(FAILURE|DENY)","reason":"({failure_reason}[^"]+)""",
    """"outcome":[^\]]*?"result"\s*:\s*"(FAILURE|DENY)","reason":"({additional_info}[^"]+)""",
    """"reason":"({additional_info}[^"]+)"""
    """"target(s)?"+:[^\}\]]+?"+displayName"+\s*:\s*"+(unknown|({object}[^"]+[^\s]))"""",
    """request"+:.+?User.+?"+displayName"+:(null|"+(Okta System|unknown|(?:({first_name}[^,"]+),\s*({last_name}[^"]+)|({full_name}[^"]+)))")""",
    """"actor"+.+?"+type"+:"+User.+?displayName"+:(null|"+(Okta System|Okta Admin|unknown|(?:({last_name}[^,"]+),\s*({first_name}[^"]+)|({full_name}[^"]+))))""",
    """request"+:.+?"+type"+:"+User"+,"+alternateId"+:(null|"+(system@okta\.com|(?:(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s",]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({=domain}[^\\\/"]+)[\/\\]+)?({=user}[\w\.\-\!\#\^\~]{1,40}\$?))))""",
    """"actor"+:[^\]]*?"+type"+:"+User"+,"+alternateId"+\s*:\s*"+(system@okta\.com|(?:(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s",]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({=user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
    """requestUri":\s*"({uri_path}[^"]+?)\s*"""",
    """"outcome":[^\]]*?"result"\s*:\s*"({result}[^"]+)"""",
    """outcome":[^\]]*?"result":"?(null|({result}[^\"]+))"?,"reason":"?(null|({result_reason}[^"]+))"""
  ]
  ParserVersion = "v1.0.0"


}
```