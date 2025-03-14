#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-login-4776-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""CEF:"""
""""eventID":"4776""""
"""attempted to validate the credentials for an account"""
]
Fields = [
""""systemTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
""""computer":"({host}[\w\-.]+)""""
""""message":"({event_name}[^"]+?)\s*""""
""""eventID":"({event_code}\d+)""""
""""eventRecordID":"({event_id}\d+)""""
""""severityValue":"({result}[^"]+?)\s*""""
""""targetUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*""""
""""targetUserName":"({email_address}[^"\s@]+@[^"\s@]+?)\s*""""
""""workstation":"({src_host}[^"\s]+?)\s*""""
""""status":"({result_code}[^"]+?)\s*""""
]
DupFields = [ "result_code->failure_code", "email_address->dest_email_address", "user->dest_user" ]
ParserVersion = "v1.0.0"


}
```