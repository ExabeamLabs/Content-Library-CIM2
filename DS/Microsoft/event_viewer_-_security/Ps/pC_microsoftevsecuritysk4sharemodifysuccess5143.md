#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-share-modify-success-5143
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-dd-MM'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """CEF:""", """EventSourceName":"Microsoft-Windows-Security-Auditing""", """cat=audit""", """EventID":5143""", """A network share object was modified""" ]
  Fields = [
  """"TimeGenerated":"({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{1,7}Z)""""
  """"EventID":({event_code}\d+)"""
  """({event_name}A network share object was modified)"""
  """"SubjectLogonId":"({login_id}[^"]+)""""
  """"Computer":"({host}[\w\-.]+)"""
  """"ShareName":"({share_name}[^"]+)""""
  """"SubjectAccount":"(-|({domain}[\w\-.]+)([\\]+)?({user}[^"]+))""""
  """"SubjectUserSid":"({user_sid}[^"]+)""""
  """"ShareLocalPath":"({share_path}[^"]+)""""
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```