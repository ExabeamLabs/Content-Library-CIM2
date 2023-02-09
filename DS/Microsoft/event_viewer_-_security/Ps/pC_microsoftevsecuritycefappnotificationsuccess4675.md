#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-app-notification-success-4675
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """CEF:""", """"eventID":"4675"""", """SIDs were filtered""" ]
  Fields = [
    """"systemTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """"computer":"({host}[\w\-.]+)""",
    """"message":"({event_name}[^"]+?)\s*"""",
    """"eventID":"({event_code}\d+)""",
    """"eventRecordID":"({event_id}\d+)""",
    """"severityValue":"({action}[^"]+?)\s*"""",
    """"targetUserSid":"({user_sid}[^"\s]+?)\s*"""",
# trust_attributes is removed
    """"tdoType":"({trust_type}[^"\s]+?)\s*"""",
# tdo_domain_sid is removed
  ]
  DupFields = ["host-> dest_host"]


}
```