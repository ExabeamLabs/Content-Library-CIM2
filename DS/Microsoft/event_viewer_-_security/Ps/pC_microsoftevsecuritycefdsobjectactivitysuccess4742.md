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
    """"targetSid":"({object_name}[^"\s]+?)\s*"""",
    """"targetUserName":"({dest_user}[^"\s]+?)\s*"""",
    """"targetDomainName":"({ds_object_dn}[^"\s]+?)\s*"""",
    """"subjectUserSid":"({user_sid}[^"\s]+?)\s*"""",
    """"subjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*"""",
    """"subjectDomainName":"({domain}[^"\s]+?)\s*"""",
    """"subjectLogonId":"({login_id}[^"\s]+?)\s*""""
    """UserAccountControl":"(-|({uac_status}[^"]+))","UserParameters""""
    """OldUacValue":"(-|({old_value}[^"]+))","NewUacValue""""
    """"NewUacValue":"(-|({new_value}[^"]+))","UserAccountControl""""
  ]
  DupFields = ["host->dest_host", "user->src_user", "domain->src_domain"]
  ParserVersion = "v1.0.0"


}
```