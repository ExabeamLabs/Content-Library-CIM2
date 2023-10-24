#### Parser Content
```Java
{
Name = okta-amfa-json-app-login-fail-signinfailed-1
    Vendor = Okta
    Product = Okta Adaptive MFA
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """"Sign-in Failed""", """,published"""", """,action"""" ]
    Fields=[
    """\Wpublished"\s*:\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """\WipAddress"\s*:\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wmessage"\s*:\s*"({failure_reason}[^",]+)""",
    """"targets"\s*:\s*\[\{.*?\WdisplayName"\s*:\s*"({full_name}[^",]+)""",
    """"targets"\s*:\s*\[\{.*?\Wlogin"\s*:\s*"({email_address}[^",]+)""",
    """({app}Okta)""",
    """"actors":\[\{[^\]\}]*?"id":"({user_agent}.+?),displayName":""",
  ]
  ParserVersion = "v1.0.0"


}
```