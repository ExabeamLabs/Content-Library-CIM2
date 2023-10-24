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
    """UserId":\s*"({user}[\w\.\-]{1,40}\$?)""",
    """SourceIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Platform":\s*"(Unknown|({os}[^"]+))""",
    """Application":\s*"({protocol}[^"]+)""",
  ]


}
```