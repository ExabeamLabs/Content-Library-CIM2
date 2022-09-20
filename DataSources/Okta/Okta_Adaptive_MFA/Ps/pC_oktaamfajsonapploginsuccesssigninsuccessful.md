#### Parser Content
```Java
{
Name = okta-amfa-json-app-login-success-signinsuccessful
    Vendor = Okta
    Product = Okta Adaptive MFA
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """"Sign-in successful,""", """,published"""", """,action"""" ]
    Fields=[
    """\Wpublished"\s*:\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """\WipAddress"\s*:\s*"({src_ip}[\da-fA-F\.:]+)""",
    """\Wmessage"\s*:\s*"({result}[^",]+)""",
    """"targets"\s*:\s*\[\{[^\]]*?\WdisplayName"\s*:\s*"({full_name}[^",]+)""",
    """"targets"\s*:\s*\[\{[^\}]*?\Wlogin"\s*:\s*"({email_address}[^",]+)""",
    """({app}Okta)""",
    """"actors":\[[^\]]*?"id":"({user_agent}[^"]+?),displayName[^\}]*?objectType":"Client"""",
    """"actors":\[[^\]]*?objectType":"Client"[^\}]*?"id":"({user_agent}[^"]+?),displayName""",
    #""""actors":\[.*?\{("?[^"]+"\s*:\s*"([^"\\]|(\\\\)*\\"|\\)+"?,?)*"?objectType"\s*:\s*"Client",?("?[^"]+"\s*:\s*([^"\\]|(\\\\)*\\"|\\)+",?)*"?id"\s*:\s*"({user_agent}[^"]+)"?,("?[^"]+"\s*:\s*"([^"\\]|(\\\\)*\\"|\\)+"?,?)*\}\]""",
    #""""actors":\[.*?\{("?[^"]+"\s*:\s*"([^"\\]|(\\\\)*\\"|\\)+"?,?)*"?id"\s*:\s*"({user_agent}[^"]+)"?,("?[^"]+"\s*:\s*"([^"\\]|(\\\\)*\\"|\\)+"?,?)*"?objectType"\s*:\s*"Client",?("?[^"]+"\s*:\s*"([^"\\]|(\\\\)*\\"|\\)+",?)*\}\]""",
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "host->dest_host" ]


}
```