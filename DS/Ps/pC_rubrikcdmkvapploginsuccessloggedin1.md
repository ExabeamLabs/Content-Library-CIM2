#### Parser Content
```Java
{
Name = rubrik-cdm-kv-app-login-success-loggedin-1
    ParserVersion = v1.0.0
    Conditions = [ """ Rubrik """, """status="Success"""", """eventName ="Audit.SamlSsoLoginAudit"""", """ logged in """ ]
    Fields = ${RubrikCDMParserTemplates.rubrik-events.Fields}[
      """\] (({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)) [^\)]+?\) ({event_name}logged in) with ({auth_method}[^"]+?) from ({src_host}[\w.-]+?)\s*("|$)"""
    ]
  

}
```