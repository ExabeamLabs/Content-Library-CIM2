#### Parser Content
```Java
{
Name = "eset-es-leef-http-session-fail-eset"
Conditions = [
  """LEEF:"""
  """|ESET|RemoteAdministrator|"""
  """cat=ESET Filtered Website Event"""
  """actionTaken=Blocked"""
]
ParserVersion = "v1.0.0"

netwrix-app-activity-2.Fields}[
    """CEF:0\|Netwrix\|(AD FS|Logon Activity|Self-audit)\|[^\|]+\|[^\|]+\|({operation}[^\|]+)\|""",
  
}
```