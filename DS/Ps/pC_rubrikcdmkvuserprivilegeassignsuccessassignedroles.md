#### Parser Content
```Java
{
Name = rubrik-cdm-kv-user-privilege-assign-success-assignedroles
  ParserVersion = v1.0.0
  Conditions = [ """ Rubrik """, """status="Success"""", """eventName ="Audit.AssignRolesAudit"""" ]
    Fields = ${RubrikCDMParserTemplates.rubrik-events.Fields}[
    """\] ({user}[\w\.\-\!\#\^\~]{1,40}\$?) [^\)]+?\) assigned roles '""",
    """\] ({operation}[^\)]+?\) assigned roles '({privileges}[^']+)'[^"]+?)\s+("|$)"""
    """(assigned roles '({privileges}[^']+)'[^"]+?)"""
  ]


}
```