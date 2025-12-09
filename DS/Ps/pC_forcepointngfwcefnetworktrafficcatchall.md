#### Parser Content
```Java
{
Name = forcepoint-ngfw-cef-network-traffic-catchall
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|Forcepoint|Firewall|""", """dvchost=""", """rt=""" ]
  Fields = ${DLForcepointParsersTemplates.forcepoint-template.Fields} [
    """CEF:\s*\d+\|([^\|]+\|){4}({event_name}[^\|]+)""",  
  ]


}
```