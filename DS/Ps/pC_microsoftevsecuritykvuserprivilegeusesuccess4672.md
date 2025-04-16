#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-privilege-use-success-4672
  ParserVersion = "v1.0.0"
  Conditions = [ """LogType="WLS"""", """EventID="4672"""" ]
  Fields = ${WindowsParsersTemplates.windows-events-wls.Fields}[
    """Computer="+({host}[\w\-.]+)""""
  ]
  DupFields = [ "host->src_host", "user->src_user", "domain->src_domain" ]


}
```