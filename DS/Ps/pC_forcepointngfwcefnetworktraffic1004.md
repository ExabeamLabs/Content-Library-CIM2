#### Parser Content
```Java
{
Name = forcepoint-ngfw-cef-network-traffic-1004
Conditions = [
  """CEF:"""
  """|FORCEPOINT|Firewall|"""
  """|1004|FW_Related-Connection|"""
]
ParserVersion = "v1.0.0"

netwrix-app-activity-2.Fields}[
    """CEF:0\|Netwrix\|(AD FS|Logon Activity|Self-audit)\|[^\|]+\|[^\|]+\|({operation}[^\|]+)\|""",
  
}
```