#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-create-success-601
  Conditions = [ """LogType="WLS"""", """EventID="601"""" ]
  ParserVersion = "v1.0.0"
  Fields = ${WindowsParsersTemplates.windows-events-wls.Fields}[
    """Computer="+({host}[\w\-.]+)""""
  ]
  DupFields = [ "host->dest_host", "user->src_user", "domain->src_domain" ]


}
```