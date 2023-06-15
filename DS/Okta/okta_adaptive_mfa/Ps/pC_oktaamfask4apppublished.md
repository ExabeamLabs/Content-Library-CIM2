#### Parser Content
```Java
{
Name = okta-amfa-sk4-app-published
  ParserVersion = v1.0.0
  Conditions = [ """"objectType":"app.""", """"published":""" ]

okta-app-activity = {
    Vendor = Okta
    Product = Okta Adaptive MFA
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """\d+:\d+ ({host}[^\s]+) \{""",
    """"published":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """"ipAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"action":\s*\{.*?"objectType":\s*"({operation}[^"]+)".+?\}""",
    """"action":\s*\{.*?"objectType":\s*"[^"]*?({result}error)".+?\}""",
    """"categories":\s*\["({operation}[^"]+)"""",
    """"actors":\[.*?\{.*?"displayName":"((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))"[^\{\}]+?"objectType":"User".*?\}""",
    """"actors":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"displayName":\s*"((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))"""",
    """"displayName":"((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+?))\s*"[^\}\]]*"objectType":"User"""",
    """"actors":\[.*?\{.*?"login":"({user}[^"\s@]+)"[^\{\}]+?"objectType":"User".*?\}""",
    """"actors":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"login":\s*"({user}[^"\s@]+)"""",
    """"actors":\[.*?\{.*?"login":"({email_address}[^"\s@]+@[^"\s@]+)"[^\{\}]+?"objectType":"User".*?\}""",
    """"actors":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"login":\s*"({email_address}[^"\s@]+@[^"\s@]+)"""",
    """"actors":\[.*?\{.*?"login":"[^@]+@({email_domain}[^"]+)"[^\{\}]+?"objectType":"User".*?\}""",
    """"actors":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"login":\s*"[^@]+@({email_domain}[^"]+)"""",
    """"targets":\[.*?\{.*?"login":"({dest_user}[^"]+)"[^\{\}]+?"objectType":"User".*?\}""",
    """"targets":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"login":\s*"({dest_user}[^"]+)"""",
    """"targets":\[.*?\{.*?"login":"({account_name}[^@\s"]+)@({dest_domain}[^"]+)"[^\{\}]+?"objectType":"User".*?\}""",
    """"targets":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"login":\s*({account_name}[^@\s"]+)@({dest_domain}[^"]+)"""",
    """"actors":\[.*?\{.*?"id":"({user_agent}[^"]+)"[^\{\}]+?"objectType":"Client".*?\}""",
    """"actors":\s*\[\{[^\]]*?"objectType":\s*"Client"[^\]]*?"id":\s*"({user_agent}[^"]+)"""",
    """"message":\s*"({additional_info}[^"]+?)\s*"""",
    """({app}Okta)""",
    """destinationServiceName(=)?({app}.+?)\s*\w+=""",
    """"targets":\[.*?\{.*?"displayName":"({app}[^"]+)"[^\{\}]+?"objectType":"AppInstance".*?\}""",
    """"targets":\s*\[\{[^\]]*?"objectType":\s*"AppInstance"[^\]]*?"displayName":\s*"({app}[^"]+)"""",
    """"type":"AppInstance"[^\}\]]*"displayName":"({app}[^"]+?)\s*"""",
    """requestUri":\s*"({request_uri}[^"]+?)\s*"""",
    """"id":"({object}[^"]+)"[^\}\]]*"objectType":"AppInstance"""",
    """"objectType":"AppInstance"[^\}\]]*"id":"({object}[^"]+)"""",
    ]
    DupFields = ["dest_user->account_name", "dest_domain->account_domain", "additional_info->event_name"
}
```