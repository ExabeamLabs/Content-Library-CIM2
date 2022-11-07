#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-ds-object-activity-success-4742
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """CEF:""", """"eventID":"4742"""",  """A computer account was changed""" ]
  Fields = [
    """"systemTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """"computer":"({host}[\w\-.]+)""",
    """"message":"({event_name}[^"]+?)\s*"""",
    """"eventID":"({event_code}\d+)""",
    """"eventRecordID":"({event_id}\d+)""",
    """"severityValue":"({result}[^"]+?)\s*"""",
    """"targetSid":"({object}[^"\s]+?)\s*"""",
    """"targetUserName":"({dest_user}[^"\s]+?)\s*"""",
    """"targetDomainName":"({object_dn}[^"\s]+?)\s*"""",
    """"subjectUserSid":"({user_sid}[^"\s]+?)\s*"""",
    """"subjectUserName":"({user}[^"\s]+?)\s*"""",
    """"subjectDomainName":"({domain}[^"\s]+?)\s*"""",
    """"subjectLogonId":"({login_id}[^"\s]+?)\s*""""
  ]
  DupFields = ["host->dest_host"]
  ParserVersion = "v1.0.0"


}
```