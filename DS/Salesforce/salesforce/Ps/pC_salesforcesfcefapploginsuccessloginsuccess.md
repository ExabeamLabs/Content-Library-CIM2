#### Parser Content
```Java
{
Name = "salesforce-sf-cef-app-login-success-loginsuccess"
  ParserVersion = "v1.0.0"
  Vendor = "Salesforce"
  Product = "Salesforce"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """Status\""", """=Success;""", """type\""", """\=LoginHistory;""", """LoginTime\""", """LoginType""" ]
  Fields = [
    """LoginTime\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """CreatedDate\\=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """suser=(({domain}[^\\\s@;=]+)\\+)?(system|({user}[\w\.\-]{1,40}\$?))\s+(\w+=|$)""",
    """suser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """SourceIp\\*=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Status\\*=({result}[^;]+)""",
    """Platform\\*=(Onbekend|Unknown|({os}[^;]+))""",
    """deviceNtDomain=({os}[^=]+?)\s+\w+=""",
    """TlsProtocol\\*=({protocol}[^;]+)""",
    """Browser\\*=(Unknown|({browser}[^"=]+))(;|"|\s\w+)"""
    """dvchost=({dest_host}[\w\-.]+?)\s*(\w+=|$)""",
    """({app}Sales Cloud)""",
    """cs1=({auth_method}[^\s]+)""",
    """UserId\\*=({user_id}[^;]+)""",
    """LoginGeo\.City\\*=(null|({location_city}[^;]+))""",
    """LoginGeo\.Country\\*=({location_country}[^;]+)""",
    """LoginType\\*=({login_type_text}[^;]+)""",
    """LoginUrl\\*=({url_host}[^;]+)""",
    """\ssourceDnsDomain=({src_domain}.+?)\s*\w+="""
  ]


}
```