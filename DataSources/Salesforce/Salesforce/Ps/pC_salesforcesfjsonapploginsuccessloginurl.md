#### Parser Content
```Java
{
Name = salesforce-sf-json-app-login-success-loginurl
  ParserVersion = v1.0.0
  Vendor = Salesforce
  Product = Salesforce
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"LoginUrl"""",""""login.salesforce.com"""" ]
  Fields = [
    """({app}salesforce)""",
    """LoginTime":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """Status":\s*"({result}[^"]+)""",
    """LoginType":\s*"({login_type_text}[^"]+)""",
    """Browser":\s*"(Unknown|({browser}[^"]+))""",
    """UserId":\s*"({user}[^"]+)""",
    """SourceIp":\s*"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """Platform":\s*"(Unknown|({os}[^"]+))""",
    """Application":\s*"({protocol}[^"]+)""",
  ]


}
```