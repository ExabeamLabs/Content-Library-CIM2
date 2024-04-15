#### Parser Content
```Java
{
Name = "salesforce-sf-cef-app-login-fail-loginfailed"
  ParserVersion = "v1.0.0"
  Vendor = "Salesforce"
  Product = "Salesforce"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """|login-failed|""", """destinationServiceName =Sales Cloud""" ]
  Fields = [
    """LoginTime\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """suser=(({domain}[^\\\s@;=]+)\\+)?(system|({user}[^\\\=\s;@]+))\s+(\w+=|$)""",
    """suser=({email_address}[^\\\=\s;@]+@[^\\\=\s;@]+)""",
    """SourceIp\\=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Status\\=({result}[^;]+)""",
    """Status\\=({failure_reason}[^;]+)""",
    """Platform\\=({os}[^;]+)""",
    """TlsProtocol\\=({protocol}[^;]+)""",
    """Browser\\*=({browser}.+?)\s*(\w+=|$|\s*(\d*\s)")""",
    """dvchost=({src_host}.+?)\s*(\w+=|$)""",
    """({app}Sales Cloud)""",
  ]


}
```