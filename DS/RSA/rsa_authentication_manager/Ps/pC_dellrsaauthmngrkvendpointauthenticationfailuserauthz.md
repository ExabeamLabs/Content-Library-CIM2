#### Parser Content
```Java
{
Name = dell-rsaauthmngr-kv-endpoint-authentication-fail-userauthz
  Conditions = [ """ SINGLEPOINT """, """ USER_AUTHZ """, """RESULT="NOT_AUTHORIZED"""" ]
  ParserVersion = "v1.0.0"

syslog-rsa-auth {
  Vendor = RSA
  Product = RSA Authentication Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """(({host}[\w\-.]+) \d+ )?({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) \S+ SINGLEPOINT""",
    """USERNAME="(unknown|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
    """RESULT="({result}[^"]+)""",
    """authenticationType="?({auth_type}[^",]+)""",
    """UserAgent=({user_agent}[^"=,]+)""",
    """ipAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """displayName =({last_name}[^=,]+?),\s*({first_name}[^=,]+?),""",
    """NameID=({user}[\w\.\-\!\#\^\~]{1,40}\$?),""",
    """sAMAccountName =({account}[^,]+)""",
    """POLICY="*({policy_name}[^"]+?)\s*"""",
  
}
```