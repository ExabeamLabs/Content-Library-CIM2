#### Parser Content
```Java
{
Name = dell-rsaauthmngr-kv-endpoint-authentication-userstepup
  Vendor = RSA
  Product = RSA Authentication Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ SINGLEPOINT """, """ USER_STEPUP_AUTHN """, """REQUEST_CONTEXT_ID="""" ]
  Fields = [
    """(({host}[\w\-.]+) \d+ )?({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) \S+ SINGLEPOINT""",
    """USERNAME="(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))""",
    """APP_NAME="({app}[^"]+)""",
    """SENSITIVITY_LEVEL="({sensitivity_level}[^"]+)""",
    """TENANT="({tenant}[^"]+)""",
    """REQUEST_CONTEXT_ID="({context_id}[^"]+)""",
    """RESULT="({result}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```