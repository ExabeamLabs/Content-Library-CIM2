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
    """\WipAddress"\s*:\s*"({src_ip}[\da-fA-F\.:]+)""",
    """\Wmessage"\s*:\s*"({failure_reason}[^",]+)""",
    """"targets"\s*:\s*\[\{.*?\WdisplayName"\s*:\s*"({full_name}[^",]+)""",
    """"targets"\s*:\s*\[\{.*?\Wlogin"\s*:\s*"({email_address}[^",]+)""",
    """({app}Okta)""",
    """"actors":\[\{[^\]\}]*?"id":"({user_agent}.+?),displayName":""",
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "host->dest_host" ]


}
```