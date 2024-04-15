#### Parser Content
```Java
{
Name = "rs2-t-xml-physical_location-access-fail-accessdenied"
Conditions = [
  """<DESCNAME><![CDATA[Access denied]]></DESCNAME>"""
  """<RDRNAME><"""
]
ParserVersion = "v1.0.0"

netwrix-app-activity-2.Fields}[
    """CEF:0\|Netwrix\|(AD FS|Logon Activity|Self-audit)\|[^\|]+\|[^\|]+\|({operation}[^\|]+)\|""",
  
}
```