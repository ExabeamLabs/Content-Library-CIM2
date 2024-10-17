#### Parser Content
```Java
{
Name = cisco-cucm-kv-app-activity-success-useraccess
Conditions = [
  """EventType =UserAccess"""
  """ResourceAccessed="""
  """EventStatus ="""
]
ParserVersion = "v1.0.0"

cisco-events = {
  Vendor = Cisco
  Product = Cisco
  TimeFormat = "MMM dd yyyy hh:mm:ss a"
  Fields = [
    """\s({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+\s+(AM|PM|am|pm))""",
    """UserID\s*=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """ClientAddress\s*=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """EventType\s*=({operation}[^\]]+)""",
    """ResourceAccessed\s*=({object}[^\]]+)""",
    """EventStatus\s*=({result}[^\]]+)""",
    """ComponentID\s*=({target}[^\]]+)""",
    """AuditDetails\s*=({additional_info}[^\]]+)""",
    """App ID\s*=({app}[^\]]+)""",
    """userPrincipalName"+:\s*"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
  
}
```