#### Parser Content
```Java
{
Name = watchguard-w-kv-network-traffic-firewall-2
Conditions = [
  """msg_id="""
  """3000-0151"""
  """firewall:"""
]
ParserVersion = "v1.0.0"

netwrix-app-activity-2.Fields}[
    """CEF:0\|Netwrix\|(AD FS|Logon Activity|Self-audit)\|[^\|]+\|[^\|]+\|({operation}[^\|]+)\|""",
  
}
```