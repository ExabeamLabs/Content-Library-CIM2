#### Parser Content
```Java
{
Name = rubrik-cdm-kv-app-login-success-loggedin-1
    ParserVersion = v1.0.0
    Conditions = [ """ Rubrik """, """status="Success"""", """eventName ="Audit.SamlSsoLoginAudit"""", """ logged in """ ]
    Fields = ${RubrikCDMParserTemplates.rubrik-events.Fields}[
      """\] ({user}\S+?) [^\)]+?\) ({event_name}logged in) with ({auth_method}[^"]+?) from ({src_host}[\w.-]+?)\s*("|$)"""
    ]
  

}
```