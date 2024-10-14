#### Parser Content
```Java
{
Name = "secureauth-login-kv-endpoint-login-20990-1"
Vendor = "SecureAuth"
Product = "SecureAuth Login"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
Conditions = [ """ EventID="20990"""", """Realm=""", """AuthRegMethod=""", """ApplianceMachineName =""" ]
Fields = [
"""\sTimeStamp="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}Z)"""",
"""\sHostName ="({host}[\w\-.]+)"""",
"""\sUserHostAddress="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
"""\sUserID="+(({email_address}[^@"]+@[^\."]+\.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
"""\sUserAgent="({user_agent}[^"]+)"""",
"""\sApplianceMachineName ="({dest_host}[\w\-.]+)"""",
"""\sAuthRegMethod="(NONE|({auth_method}[^"]+))"""",
"""\sRealm="({realm}[^"]+)"""",
"""({event_code}20990)""",
"""\sTrxResult="({result_reason}[^"]+)"""",
"""\sSucceed="({result}(True|False))""""
]
ParserVersion = "v1.0.0"


}
```