#### Parser Content
```Java
{
Name = microsoft-evapp-json-endpoint-activity-success-catchall
  ParserVersion = v1.0.0
  Product = Event Viewer - Application
  Conditions = [ """"EventID":""", """"Channel":"Application"""", """"ProviderName":"""" ]
  Fields = ${WindowsParsersTemplates.microsoft-json-events.Fields}[
    """exa_json_path=$.StringInserts,exa_regex=(\[\]|.+?"({additional_info}[^"]+))"""
  ]


}
```