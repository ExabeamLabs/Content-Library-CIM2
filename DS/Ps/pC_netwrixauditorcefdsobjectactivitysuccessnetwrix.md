#### Parser Content
```Java
{
Name = "netwrix-auditor-cef-ds-object-activity-success-netwrix"
Conditions = [
  """CEF:0|Netwrix|Active Directory|"""
]
ParserVersion = "v1.0.0"

netwrix-app-activity-2.Fields}[
    """CEF:0\|Netwrix\|(AD FS|Logon Activity|Self-audit)\|[^\|]+\|[^\|]+\|({operation}[^\|]+)\|""",
  
}
```