#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-login-fail-appdisplayname
  Vendor = Microsoft
  Product = Office 365
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [
""""appDisplayName":"""
"""failed to login"""
""""userPrincipalName":""""
]
Fields = [
    """"userDisplayName":"({full_name}[^"]+)""",
    """"userPrincipalName":"({email_address}[^@]+@[^"]+)""",
    """"userId":"({user_sid}[^"]+)""",
    """"appDisplayName":"({app}[^"]+)""",
    """"ipAddress":"({src_ip}[^"]+)""",
    """"city":"({location_city}[^"]+)""",
    """"state":"({location_state}[^"]+)""",
    """"failureReason":"({failure_reason}[^"]+)""",
    """"createdDateTime":"({time}[^"]+)""",
    """"countryOrRegion":"({country_code}[^"]+)""",
    """"additionalDetails":"({additional_info}[^"]+)""",
    """"operatingSystem":"({os}[^"]+)""",
    """"browser":"({browser}[^"]+)""",
    """login-({result}failed)"""
  ]


}
```