#### Parser Content
```Java
{
Name = okta-amfa-cef-alert-trigger-success-passwordspraydetected
  ParserVersion = v1.0.0
  Vendor = Okta
  Product = Okta Adaptive MFA
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """"actor":""", """"securityContext":""", """"target":""", """"client":""" , """security.password_spray.detected"""]
  Fields=[
    """"published"\s*:\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """"displayMessage"\s*:\s*"({additional_info}[^"]+)""",
    """"eventType"\s*:\s*"({alert_name}[^"]+)""",
    """"legacyEventType"\s*:\s*"({alert_name}[^"]+)""",
    """cat=({alert_type}[^\s]+)"""
    """"actor":\s*[^\]]*?"displayName"\s*:\s*"(?:({last_name}[^,"]+),\s*({first_name}[^"]+)|({full_name}[^"]+))"""",
    """"actor":[^\]]*?"alternateId"\s*:\s*"(?:({email_address}[^"@]+@({domain}[^"]+))|({user}[^"]+))"""",
    """"client":[^\]]*?"rawUserAgent"\s*:\s*"({user_agent}[^"]+)""",
    """"client":[^\]]*?"ipAddress"\s*:\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"outcome":[^\]]*?"result"\s*:\s*"FAILURE","reason":"({failure_reason}[^"]+)""",
    """"outcome":[^\]]*?"result"\s*:\s*"({result}[^"]+)"""",
    """outcome":[^\]]*?"result":"?(null|({outcome_result_at}[^\"]+))"?,"reason":"?(null|({outcome_reason_at}[^"]+))""",
    """"target":.+?"displayName"\s*:\s*"({object}[^"]+[^\s])"""",
    """"target":.+?"type"\s*:\s*"({object_type}[^"]+)"""",
    """({app}OKTA)""",
    """({app}Okta)""",
    """"city":"({location_city}[^"]+)""",
    """"state":"({location_state}[^"]+)""",
    """"country":"({location_country}[^"]+)""",
    ""","legacyEventType":"({operation}[^"]+)""""
  ]


}
```