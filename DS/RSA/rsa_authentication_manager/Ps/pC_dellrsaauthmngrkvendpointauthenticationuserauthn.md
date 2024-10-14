#### Parser Content
```Java
{
Name = dell-rsaauthmngr-kv-endpoint-authentication-userauthn
  Vendor = RSA
  Product = RSA Authentication Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ SINGLEPOINT """, """ USER_AUTHN_CONDITION """, """,authenticationType=""" ]
  Fields = [
    """(({host}[\w\-.]+) \d+ )?({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) \S+ SINGLEPOINT""",
    """USERNAME="(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """POLICY="({auth_policy}[^"]+)""",
    """AUTH_CONDITION="({auth_condition}[^"]+)""",
    """ipAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """DECIDING_RULE_SET="({deciding_rule_set}[^"]+)""",
    """RESOURCE="({resource}[^"]+)""",
    """authenticationType=({auth_type}[^",]+)""",
    """ACTION="({result}[^"]+)""",
    """UserAgent=({user_agent}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```