#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-login-success-loggedin
  Vendor = Microsoft
  Product = Office 365
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [
  """"appDisplayName":"""
  """successfully logged in"""
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
    """"createdDateTime":"({time}[^"]+)""",
    """"countryOrRegion":"({country_code}[^"]+)""",
    """"additionalDetails":"({additional_info}[^"]+)""",
    """"operatingSystem":"({os}[^"]+)""",
    """"browser":"({browser}[^"]+)""",
    """login-({result}success)""",
  ]


}
```