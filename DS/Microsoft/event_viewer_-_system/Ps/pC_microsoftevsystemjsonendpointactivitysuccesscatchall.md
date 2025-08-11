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
  Fields = ${WindowsParsersTemplates.microsoft-json-events.Fields}[
    """Subject:\s*Security ID:\s*({user_sid}[^:]+?)(\s+\w+){1,2}:\s"""
    """Subject:[^"]+?Account Name:\s*(({domain}[^:\\]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+){1,2}:\s"""
    """Subject:[^"]+?Account Domain:\s*({domain}[^:]+?)(\s+\w+){1,2}:\s"""
    """Subject:[^"]+?Logon ID:\s*({login_id}[^:]+?)(\s+\w+){1,2}:\s"""
  ]  
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