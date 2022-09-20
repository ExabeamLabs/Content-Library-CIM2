#### Parser Content
```Java
{
Name = dell-ram-kv-app-login-success-userprotectedappauth
  ParserVersion = v1.0.0
  Product = RSA Authentication Manager
  Conditions = [ """ SINGLEPOINT """, """ USER_PROTECTED_APP_AUTHN """ ]

rsa-app-login = {
  Vendor = Dell
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """({host}[\w\-.]+) \d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) \S+ SINGLEPOINT""",
    """USERNAME="(unknown|({user}[^\s"]+))""",
    """RESULT="({result}[^"]+)""",
    """APPLICATION="({app}[^"]+)""",
    """TYPE="({auth_method}[^"]+)""",
    """SESSION_ID="({session_id}[^"]+)""",
    """NOT_AUTHNED_REASON="({failure_reason}[^"]+)""",
  
}
```