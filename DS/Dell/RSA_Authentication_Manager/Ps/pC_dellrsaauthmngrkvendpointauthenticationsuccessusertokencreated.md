#### Parser Content
```Java
{
Name = dell-rsaauthmngr-kv-endpoint-authentication-success-usertokencreated
Conditions = [
  """client_ip_address="""
  """result_action=User Token Created"""
]
ParserVersion = "v1.0.0"

syslog-rsa-auth {
  Vendor = Dell
  Product = RSA Authentication Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """({host}[\w\-.]+) \d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) \S+ SINGLEPOINT""",
    """USERNAME="(unknown|({user}[^\s"]+))""",
    """RESULT="({result}[^"]+)""",
    """authenticationType="?({auth_method}[^",]+)""",
    """UserAgent=({user_agent}[^"=,]+)""",
    """ipAddress=({src_ip}[A-Fa-f:\d.]+)""",
    """displayName =({last_name}[^=,]+?),\s*({first_name}[^=,]+?),""",
    """NameID=({name_id}[^,]+)""",
    """sAMAccountName =({sam_accountname}[^,]+)""",
    """POLICY="*({policy_name}[^"]+?)\s*"""",
  
}
```