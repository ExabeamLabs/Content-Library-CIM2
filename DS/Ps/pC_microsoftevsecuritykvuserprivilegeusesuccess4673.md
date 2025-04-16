#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-privilege-use-success-4673
  ParserVersion = "v1.0.0"
  Conditions = [ """LogType="WLS"""", """EventID="4673"""" ]
  Fields = ${WindowsParsersTemplates.windows-events-wls.Fields}[
    """Computer="+({host}[\w\-.]+)""""
  ]
  DupFields = [ "host->dest_host", "user->src_user", "domain->src_domain" ]


}
```