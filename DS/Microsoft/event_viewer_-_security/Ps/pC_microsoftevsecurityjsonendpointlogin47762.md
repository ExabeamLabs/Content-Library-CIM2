#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-login-4776-2
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """"event_id":"4776"""", """attempted to validate the credentials for an account""" ]
  Fields = [
    """({event_name}The computer attempted to validate the credentials for an account)""",
    """"time":"({time}\d+\/\d+\/\d\d\d\d \d+:\d\d:\d\d (am|AM|pm|PM))""",
    """"computer":"({host}[^"]+)""",
    """"computer":"({dest_host}[^"]+)""",
    """"computer":"(?!(?:[A-Fa-f:\d.]+))[^."]+\.({domain}[^"]+)""",
    """"source_workstation":"({src_host}[^"]+)""",
    """"error_code":"({result_code}[^"]+)""",
    """"logon_account":"({user}[\w\.\-]{1,40}\$?)""",
    """"event_id":"({event_code}\d+)""",
    """"The ({login_type_text}computer|domain)(\s\w+)? attempted to validate the credentials""",
  ]
  ParserVersion = "v1.0.0"


}
```