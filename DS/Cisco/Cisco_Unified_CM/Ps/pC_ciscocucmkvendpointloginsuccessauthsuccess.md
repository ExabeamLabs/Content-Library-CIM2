#### Parser Content
```Java
{
Name = cisco-cucm-kv-endpoint-login-success-authsuccess
  Product = Cisco Unified CM
  ParserVersion = v1.0.0
  Conditions = [ """EventType =UserLogging""", """=Login Authentication Successful]""" ]

cisco-events = {
  Vendor = Cisco
  Product = Cisco
  TimeFormat = "MMM dd yyyy HH:mm:ss a"
  Fields = [
    """\s({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+\s+(AM|PM|am|pm))""",
    """UserID\s*=({user}[^\s\]]+)""",
    """ClientAddress\s*=({src_ip}[A-Fa-f:\d.]+)""",
    """EventType\s*=({operation}[^\]]+)""",
    """ResourceAccessed\s*=({object}[^\]]+)""",
    """EventStatus\s*=({result}[^\]]+)""",
    """ComponentID\s*=({target}[^\]]+)""",
    """AuditDetails\s*=({additional_info}[^\]]+)""",
    """App ID\s*=({app}[^\]]+)""",
    """userPrincipalName"+:\s*"+({email_address}[^@]+@({email_domain}[^"]+))""",
  
}
```