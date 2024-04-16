#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-endpoint-login-fail-4771-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """CEF:""", """"eventID":"4771"""", """Kerberos pre-authentication failed""" ]
  Fields = [
    """"systemTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """"computer":"({host}[\w\-.]+)""",
    """"message":"({event_name}[^"]+?)\s*"""",
    """"eventID":"({event_code}\d+)""",
    """"eventRecordID":"({event_id}\d+)""",
    """"severityValue":"({result}[^"]+?)\s*"""",
    """"targetSid":"({user_sid}[^"\s]+?)\s*"""",
    """"targetUserName":"({user}[\w\.\-]{1,40}\$?)\s*"""",
    """"serviceName":"({src_host}[\w\-.]+)\/({domain}[^\\\/\s"]+?)\s*"""",
    """"status":"({result_code}[^"]+?)\s*""""
  ]
  DupFields = [
    "result_code->failure_code"
  ]


}
```