#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-login-fail-appdisplayname
  Vendor = Microsoft
  Product = Microsoft 365
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
""""appDisplayName":"""
"""failed to login"""
""""userPrincipalName":""""
]
Fields = [
    """"userDisplayName":"({full_name}[^"]+)""",
    """"userPrincipalName":"({email_address}[^@]+@({email_domain}[^"]+\.[^"]+))""",
    """"userId":"({user_sid}[^"]+)""",
    """"appDisplayName":"({app}[^"]+)""",
    """"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"city":"({location_city}[^"]+)""",
    """"state":"({location_state}[^"]+)""",
    """"failureReason":"({failure_reason}[^"]+)""",
    """"(created|signin)DateTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"countryOrRegion":"({country_code}[^"]+)""",
    """"additionalDetails":"({additional_info}[^"]+)""",
    """"deviceInformation":"(|({src_host}[\w\-.]+?));(|({os}[^;]+?));(|({browser}[^"]+?));?"""",
    """"operatingSystem":"({os}[^"]+)""",
    """"browser":"({browser}[^"]+)""",
    """login-({result}failed)""",
    """"signinErrorCode":({failure_code}\d+)"""
  ]


}
```