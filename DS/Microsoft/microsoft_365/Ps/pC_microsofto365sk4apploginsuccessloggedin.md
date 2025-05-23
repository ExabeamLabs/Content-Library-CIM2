#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-login-success-loggedin
  Vendor = Microsoft
  Product = Microsoft 365
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss"]
  Conditions = [
  """"appDisplayName":"""
  """successfully logged in"""
  """"userPrincipalName":""""
]
Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """"userDisplayName":"({full_name}[^"]+)""",
    """"userPrincipalName":"({email_address}[^@"]+@({email_domain}[^\."]+\.[^"]+))(?<!local)?""",
    """"userId":"({user_sid}[^"]+)""",
    """"appDisplayName":"\s*({app}[^"]+?)\s*"""",
    """"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"city":"({location_city}[^"]+)""",
    """"state":"({location_state}[^"]+)""",
    """"createdDateTime":"({time}[^"]+)""",
    """"countryOrRegion":"({country_code}[^"]+)""",
    """"additionalDetails":"({additional_info}[^"]+)""",
    """"deviceInformation":"(|({src_host}[\w\-.]+?));(|({os}[^;]+?));(|({browser}[^"]+?));?"""",
    """"operatingSystem":"({os}[^"]+)""",
    """"browser":"({browser}[^"]+)""",
    """login-({result}success)""",
  ]


}
```