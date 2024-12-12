#### Parser Content
```Java
{
Name = imperva-securesphere-cef-database-alert-success-security
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF""", """|cat=Security""" , """|EventId=""" , """|Policy=""", """|EventType="""]
  Fields = ${ImpervaParsersTemplates.securesphere-db-activity.Fields}[
    """EventType=({alert_name}({alert_type}[^\|]+))"""
  ]


}
```