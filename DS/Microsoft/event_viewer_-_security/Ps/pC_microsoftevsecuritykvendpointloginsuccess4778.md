#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-4778"
Conditions = [
"""LogType="WLS""""
"""EventID="4778""""
]
ParserVersion = "v1.0.0"

windows-events-wls.Fields}[
    """Computer="+({host}[\w\-.]+)""""
  ]
  DupFields = [ "host->dest_host" ]
 },

${WindowsParsersTemplates.windows-events-wls} {
  Name = microsoft-evsecurity-kv-endpoint-login-success-552
  Product = "Event Viewer - Security"
  Conditions = [ """LogType="WLS"""", """EventID="552"""" ]
  ParserVersion = "v1.0.0"
  Fields = ${WindowsParsersTemplates.windows-events-wls.Fields}[
    """Computer="+({host}[\w\-.]+)""""
  ]
  DupFields = [ "host->dest_host" 
}
```