#### Parser Content
```Java
{
Name = dell-rsaauthmngr-kv-endpoint-authentication-userlogin
  Vendor = Dell
  Product = RSA Authentication Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ SINGLEPOINT """, """ USER_LOGIN """, """ AUTHN_TYPE="""" ]
  Fields = [
    """({host}[\w\-.]+) \d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) \S+ SINGLEPOINT""",
    """USERNAME="({user}[^\s"]+)""",
    """REMOTE_IP="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """RESULT="({result}[^"]+)""",
    """SESSION_ID="({session_id}[^"]+)""",
    """AUTHN_TYPE="({auth_method}[^"]+)""",
    """NOT_AUTHNED_REASON="({failure_reason}[^"]+)""",
    """USER_AGENT="({user_agent}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```