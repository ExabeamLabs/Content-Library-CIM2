#### Parser Content
```Java
{
Name = cisco-ucm-str-app-logout-success-loggedout
  ParserVersion = v1.0.0
  Product = Cisco Unified CM
  Conditions = [ """EventType =UserLogging""", """Successfully Logged out""" ]

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