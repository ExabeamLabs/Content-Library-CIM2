#### Parser Content
```Java
{
Name = "airlock-sah-kv-vpn-logout-success-auditlog"
Conditions = [
""" Audit Log ["""
""" event_type=""""
"""" time_taken=""""
"""" system_name=""""
""""Disconnect""""
]
ParserVersion = "v1.0.0"

netwrix-app-activity-2.Fields}[
    """CEF:0\|Netwrix\|(AD FS|Logon Activity|Self-audit)\|[^\|]+\|[^\|]+\|({operation}[^\|]+)\|""",
  
}
```