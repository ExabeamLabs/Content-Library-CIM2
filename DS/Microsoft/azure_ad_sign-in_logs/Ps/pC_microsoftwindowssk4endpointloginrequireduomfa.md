#### Parser Content
```Java
{
Name = microsoft-windows-sk4-endpoint-login-requireduomfa
  Vendor = Microsoft
  Product = Azure AD Sign-In Logs
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"OperationName":"Sign-in activity"""", """"ConditionalAccessStatus":"""", """"enforcedGrantControls":["RequireDuoMfa"]""" ]
  Fields = [
    """"TimeGenerated":"({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
    """"IPAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"UserPrincipalName":"({email_address}[^"\s@]+@({email_domain}[^"\s@]+))"""",
    """"ConditionalAccessStatus":"({result}[^"]+)"""",
    """UserDisplayName"+:"+({full_name}[^"]+)""",
    """UserId"+:"+({user_id}[^"]+)""",
    """"+IPAddress"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"UserAgent\\*"+:\\*"+({user_agent}[^"]+)""",
    """"ResourceDisplayName":"({app}[^"]+)""",
    """"SourceSystem"+:"+({dest_host}[\w\-.]+)""",
    """"ClientAppUsed"+:"+({category}[^"]+)""",
    """"AppDisplayName"+:"+({resource}[^"]+)""",
    """"countryOrRegion\\*"+:\\*"+({country}[^"]+)\\"+""",
    """"city\\*"+:\\*"+({city}[^"]+)\\"+""",
    """"\$table"+:"+({db_name}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```