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
    """"computer":"({src_host}({host}[\w\-.]+))""",
    """"message":"({event_name}[^"]+?)\s*"""",
    """"eventID":"({event_code}\d+)""",
    """"eventRecordID":"({event_id}\d+)""",
    """"severityValue":"({action}[^"]+?)\s*"""",
    """"targetUserSid":"({user_sid}[^"\s]+?)\s*"""",
    """"targetUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*"""",
    """"targetDomainName":"({domain}[^"\s]+?)\s*"""",
    """"targetLogonId":"({login_id}[^"\s]+?)\s*"""",
    """"logonType":"({login_type}\d+)\s*""""
  ]
  DupFields = [ "login_id->dest_login_id" , "user_sid->dest_user_sid" , "domain->dest_domain", "user->dest_user" ]


}
```