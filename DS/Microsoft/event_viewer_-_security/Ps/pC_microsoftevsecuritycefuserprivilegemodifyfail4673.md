#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-user-privilege-modify-fail-4673
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """CEF:""", """"eventID":"4673"""", """A privileged service was called""" ]
  Fields = [
    """"systemTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """"computer":"({host}[\w\-.]+)""",
    """"message":"({event_name}[^"]+?)\s*"""",
    """"eventID":"({event_code}\d+)""",
    """"eventRecordID":"({event_id}\d+)""",
    """"severityValue":"({result}[^"]+?)\s*"""",
    """"subjectUserSid":"({user_sid}[^"\s]+?)\s*"""",
    """"subjectUserName":"({user}[\w\.\-]{1,40}\$?)\s*"""",
    """"subjectDomainName":"({domain}[^"\s]+?)\s*"""",
    """"subjectLogonId":"({login_id}[^"\s]+?)\s*"""",
    """"objectServer":"({object_server}[^"]+?)\s*"""",
    """"privilegeList":"({privileges}[^"]+?)\s*"""",
  ]
  DupFields = [ "host->dest_host" ]


}
```