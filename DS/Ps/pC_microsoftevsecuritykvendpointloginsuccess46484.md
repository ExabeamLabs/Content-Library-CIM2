#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-success-4648-4
  Conditions = [ """LogType="WLS"""", """EventID="4648"""" ]
  ParserVersion = "v1.0.0"
  Fields = ${WindowsParsersTemplates.windows-events-wls.Fields}[
    """Computer="+({host}[\w\-.]+)""""
  ]
  DupFields = [ "host->dest_host", "user->src_user", "domain->src_domain" ]
 

}
```