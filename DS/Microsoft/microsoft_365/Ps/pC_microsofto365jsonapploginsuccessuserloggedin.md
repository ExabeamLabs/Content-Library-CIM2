#### Parser Content
```Java
{
Name = microsoft-o365-json-app-login-success-userloggedin
  Vendor = Microsoft
  Product = Microsoft 365
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Microsoft Office 365""", """UserLoggedIn""", """"ResultStatus":""", """,ClientIP":""" ]
  Fields = [
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",  
    """UserId":"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""",    """ClientIP":"\[?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Operation":"({event_name}[^",]+)""",
    """"ResultStatus":"({result}[^",]+)""",
    """({app}MS Office365)""",
    """"Name":"UserAgent"?,Value":"({user_agent}[^"]+?)\s*"""",
    """DeviceProperties":\[\{"Name":"OS,Value":"({os}[^"}]+)""" 
  ]


}
```