#### Parser Content
```Java
{
Name = microsoft-windows-sk4-endpoint-login-requireduomfa
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"OperationName":"Sign-in activity"""", """"ConditionalAccessStatus":"""", """"enforcedGrantControls":["RequireDuoMfa"]""" ]
  Fields = [
    """"TimeGenerated":"({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
    """"IPAddress":"({src_ip}[A-Fa-f:\d.]+)"""",
    """"UserPrincipalName":"({email_address}[^"\s@]+@({email_domain}[^"\s@]+))"""",
    """"ConditionalAccessStatus":"({result}[^"]+)"""",
    """UserDisplayName"+:"+({full_name}[^"]+)""",
    """UserId"+:"+({user_id}[^"]+)""",
    """"+IPAddress"+:"+({src_ip}[^"]+)""",
    """"UserAgent\\*"+:\\*"+({user_agent}[^"]+)""",
    """"ResourceDisplayName":"({app}[^"]+)""",
    """"SourceSystem"+:"+({dest_host}[^"]+)""",
    """"ClientAppUsed"+:"+({category}[^"]+)""",
    """"AppDisplayName"+:"+({resource}[^"]+)""",
    """"countryOrRegion\\*"+:\\*"+({country}[^"]+)\\"+""",
    """"city\\*"+:\\*"+({city}[^"]+)\\"+""",
    """"\$table"+:"+({db_name}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```