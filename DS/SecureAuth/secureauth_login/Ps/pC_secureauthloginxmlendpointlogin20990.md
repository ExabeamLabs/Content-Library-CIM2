#### Parser Content
```Java
{
Name = "secureauth-login-xml-endpoint-login-20990"
  Vendor = "SecureAuth"
  Product = "SecureAuth Login"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """<EventID>20990<""", """<Realm>""", """<AuthRegMethod>""", """<ApplianceMachineName>""" ]
  Fields = [
    """<TimeStamp>({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}Z)<""",
    """<HostName>({host}[\w\-.]+)<""",
    """<UserHostAddress>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<""",
    """<UserID>(({email_address}([A-Za-z0-9]+[!#$%&'+\-\/=?^_`~])*[A-Za-z0-9]+?@[^\]\s<\\,\|]+\.[^\]\s<\\,\|]+?)|({user}[\w.\-!#^~]{1,40}?$))<""",
    """<UserAgent>({user_agent}[^<]+)<""",
    """<ApplianceMachineName>({dest_host}[\w.-]+)<""",
    """<AuthRegMethod>(NONE|({auth_method}[^<]+))<""",
    """<Realm>(NONE|({realm}[^<]+))<""",
    """({event_code}20990)""",
    """<TrxResult>({result_reason}[^<]+)<""",
    """<Succeed>({result}(True|False))<""",
    """<Comment>({additional_info}[^<]+)<"""
  ]
  ParserVersion = "v1.0.0"


}
```