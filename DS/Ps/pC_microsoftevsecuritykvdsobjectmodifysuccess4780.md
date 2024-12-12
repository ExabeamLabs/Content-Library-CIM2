#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-ds-object-modify-success-4780
  Conditions = [ """LogType="WLS"""", """EventID="4780"""" ]
  ParserVersion = "v1.0.0"
  Fields = ${WindowsParsersTemplates.windows-events-wls.Fields}[
    """Computer="+({host}[\w\-.]+)""""
  ]
  DupFields = [ "host->dest_host" ]


}
```