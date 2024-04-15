#### Parser Content
```Java
{
Name = "salesforce-sf-cef-app-login-success-loginsuccess"
  ParserVersion = "v1.0.0"
  Vendor = "Salesforce"
  Product = "Salesforce"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """|login-success|""", """destinationServiceName =Sales Cloud""" ]
  Fields = [
    """LoginTime\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """CreatedDate\\=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """suser=(({domain}[^\\\s@;=]+)\\+)?(system|({user}[^\\\=\s;@]+))\s+(\w+=|$)""",
    """suser=({email_address}[^\\\=\s;@]+@({email_domain}[^\\\=\s;@]+))""",
    """suser=({email_address}[^\\\=\s;@]+@[^\\\=\s;@]+)""",
    """SourceIp\\*=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Status\\*=({result}[^;]+)""",
    """Platform\\*=(Unknown|({os}[^;]+))""",
    """deviceNtDomain=({os}[^=]+?)\s+\w+=""",
    """TlsProtocol\\*=({protocol}[^;]+)""",
    """Browser\\*=(Unknown|({browser}.+?))(;|\s\w+=)""",
    """dvchost=({src_host}.+?)\s*(\w+=|$)""",
    """({app}Sales Cloud)""",
    """cs1=({auth_method}[^\s]+)""",
    """UserId\\*=({user_id}[^;]+)""",
    """LoginGeo\.City\\*=(null|({location_city}[^;]+))""",
    """LoginGeo\.Country\\*=({location_country}[^;]+)""",
    """LoginType\\*=({login_type_text}[^;]+)""",
    """LoginUrl\\*=({url_host}[^;]+)""",
  ]


}
```