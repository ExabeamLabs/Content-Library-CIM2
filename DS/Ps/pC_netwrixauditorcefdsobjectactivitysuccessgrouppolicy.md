#### Parser Content
```Java
{
Name = "netwrix-auditor-cef-ds-object-activity-success-grouppolicy"
Conditions = [
  """CEF:0|Netwrix|Group Policy|"""
]
ParserVersion = "v1.0.0"

netwrix-app-activity-2.Fields}[
    """CEF:0\|Netwrix\|(AD FS|Logon Activity|Self-audit)\|[^\|]+\|[^\|]+\|({operation}[^\|]+)\|""",
  
}
```