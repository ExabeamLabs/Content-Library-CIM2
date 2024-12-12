#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-privilege-use-success-576
  ParserVersion = "v1.0.0"
  Conditions = [ """LogType="WLS"""", """EventID="576"""" ]
  Fields = ${WindowsParsersTemplates.windows-events-wls.Fields}[
    """Computer="+({host}[\w\-.]+)""""
  ]
  DupFields = [ "host->src_host" ]


}
```