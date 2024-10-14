#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-lock-success-4740-3
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Account That Was Locked Out""", """EventID=4740""", """EventSource=Microsoft-Windows-Security-Auditing""" ]
  Fields = [
    """DetectTime=({time}\d{4}-\d{1,2}-\d{1,2}\s+\d{1,2}:\d{1,2}:\d{1,2})""",
    """({event_name}A user account was locked out)""",
    """({event_code}4740)""",
    """ComputerName =({host}[\w\-.]+)""",
    """Account That Was Locked Out:Account Name =({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """Account That Was Locked Out:Security ID=({user_sid}[^\s]+)""",
    """Caller Computer Name =({src_host}[\w\-.]+)""",
    """Subject:Account Name =({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """Subject:Account Domain=({src_domain}[^\s]+)""",
    """Subject:Logon ID=({login_id}[^\s\"]+)"""
  ]
  DupFields = [ "src_domain->domain" ]
  ParserVersion = "v1.0.0"


}
```