#### Parser Content
```Java
{
Name = "google-workspace-cef-app-login-success-loginsuccess"
ParserVersion = v1.0.0
Vendor = "Google"
Product = "Google Workspace"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""applicationName":"""
""""login""""
""""uniqueQualifier":"""
""""login_success""""
]
Fields = [
"""\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s\d+\s"""
"""\"time\"\s*:\s*\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""\"ipAddress\"\s*:\s*\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\"profileId\"\s*:\s*\"({user_id}\d+)"""
"""suser=(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+[\w=]+""",
""""actor"\s*:\s*\{[^=]*?"email"\s*:\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
"""\"events\"\s*:[^\]]*?\"name\"\s*:\s*\"login_type\"\s*,\s*\"value\"\s*:\s*\"({login_type_text}[^\"]+?)\""""
"""\"applicationName\":\"({app}[^\"]+)\""""
]


}
```