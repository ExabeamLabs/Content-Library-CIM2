#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-4776-3"
Conditions = [
"""LogType="WLS""""
"""EventID="4776""""
]
ParserVersion = "v1.0.0"

windows-events-wls.Fields}[
    """Computer="+({host}[\w\-.]+)""""
  ]
  DupFields = [ "host->dest_host", "user->src_user", "domain->src_domain" ]
 },

${WindowsParsersTemplates.windows-events-wls} {
  Name = microsoft-evsecurity-kv-endpoint-login-success-552
  Product = "Event Viewer - Security"
  Conditions = [ """LogType="WLS"""", """EventID="552"""" ]
  ParserVersion = "v1.0.0"
  Fields = ${WindowsParsersTemplates.windows-events-wls.Fields}[
    """Computer="+({host}[\w\-.]+)""""
  ]
  DupFields = [ "host->dest_host", "user->src_user", "domain->src_domain" 
}
```