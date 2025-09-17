#### Parser Content
```Java
{
Name = microsoft-evsystem-json-endpoint-activity-success-catchall
  ParserVersion = v1.0.0
  Product = Event Viewer - System
  Conditions = [ """"EventID":""", """"Channel":"System"""", """"ProviderName":"""" ]  

microsoft-json-events}{
  Name = microsoft-evsecurity-json-endpoint-activity-success-catchall
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = [ """"EventID":""", """"Channel":"Security"""", """"ProviderName":"""" ]  
},

${WindowsParsersTemplates.microsoft-json-events}{
  Name = microsoft-evapp-json-endpoint-activity-success-catchall
  ParserVersion = v1.0.0
  Product = Event Viewer - Application
  Conditions = [ """"EventID":""", """"Channel":"Application"""", """"ProviderName":"""" ]
  Fields = ${WindowsParsersTemplates.microsoft-json-events.Fields}[
    """exa_json_path=$.StringInserts,exa_regex=(\[\]|.+?"({additional_info}[^"]+))"""
  
}
```