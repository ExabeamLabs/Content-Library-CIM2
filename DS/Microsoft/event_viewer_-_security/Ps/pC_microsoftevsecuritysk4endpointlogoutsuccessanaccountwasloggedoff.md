#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-endpoint-logout-success-anaccountwasloggedoff
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """CEF:""", """"eventID":"4634"""", """An account was logged off""" ]
  Fields = [
    """"systemTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """"computer":"({host}[\w\-.]+)""",
    """"message":"({event_name}[^"]+?)\s*"""",
    """"eventID":"({event_code}\d+)""",
    """"eventRecordID":"({event_id}\d+)""",
    """"severityValue":"({action}[^"]+?)\s*"""",
    """"targetUserSid":"({user_sid}[^"\s]+?)\s*"""",
    """"targetUserName":"({user}[^"\s]+?)\s*"""",
    """"targetDomainName":"({domain}[^"\s]+?)\s*"""",
    """"targetLogonId":"({login_id}[^"\s]+?)\s*"""",
    """"logonType":"({login_type}\d+)\s*""""
  ]
   DupFields = ["host->dest_host"]


}
```