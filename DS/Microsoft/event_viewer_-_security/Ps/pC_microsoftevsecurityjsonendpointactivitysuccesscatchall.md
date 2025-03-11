#### Parser Content
```Java
{
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


}
```