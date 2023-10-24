#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-share-delete-success-5144
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-dd-MM'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """CEF:""", """EventSourceName":"Microsoft-Windows-Security-Auditing""", """cat=audit""", """EventID":5144""", """A network share object was deleted""" ]
  Fields = [
  """"TimeGenerated":"({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{1,7}Z)""""
  """"EventID":({event_code}\d+)"""
  """({event_name}A network share object was deleted)"""
  """"SubjectLogonId":"({login_id}[^"]+)""""
  """"Computer":"({host}[\w\-.]+)"""
  """"ShareName":"({share_name}[^"]+)""""
  """"SubjectAccount":"(-|({domain}[\w\-.]+)([\\]+)?({user}[\w\.\-]{1,40}\$?))""""
  """"SubjectUserSid":"({user_sid}[^"]+)""""
  """"ShareLocalPath":"({share_path}[^"]+)""""
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```