#### Parser Content
```Java
{
Name = dell-rsaauthmngr-kv-endpoint-authentication-userauthn
  Vendor = Dell
  Product = RSA Authentication Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ SINGLEPOINT """, """ USER_AUTHN_CONDITION """, """,authenticationType=""" ]
  Fields = [
    """({host}[\w\-.]+) \d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) \S+ SINGLEPOINT""",
    """USERNAME="({user}[^\s"]+)""",
    """POLICY="({auth_policy}[^"]+)""",
    """AUTH_CONDITION="({auth_condition}[^"]+)""",
    """ipAddress=({src_ip}[A-Fa-f:\d.]+)""",
    """DECIDING_RULE_SET="({deciding_rule_set}[^"]+)""",
    """RESOURCE="({resource}[^"]+)""",
    """authenticationType=({auth_method}[^",]+)""",
    """ACTION="({action}[^"]+)""",
    """UserAgent=({user_agent}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```