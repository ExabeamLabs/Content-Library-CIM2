#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-logout-4634
  ExtractionType = json
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss", "epoch_sec", "MM/dd/yyyy hh:mm:ss a", "MMM dd HH:mm:ss yyyy"]
  Conditions = [ """4634""", """An account was logged off""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d ((?i)am|pm))""",
    """Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(::ffff:)?((?i)am|pm|\d{4}|({host}[\w.\-]+))\s""",
    """\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?((?i)am|pm|\d{4}|({host}[\w\-.]+))\s"""
    """TimeGenerated=({time}\d+)""",
    """({time}\w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+""",
    """({event_code}4634)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({time}\w+\s\d+\s\d+:\d+:\d+\s\d+)"""
    """EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
    """({event_name}An account was logged off)""",
    """Security ID:\s*(SYSTEM|({user_sid}\S+))\s+Account Name:""",
    """Account Name:\s*(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:""",
    """Account Domain:\s*({domain}\S+)\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+Logon Type:""",
    """Logon Type:\s*({login_type}\d+)""",
    """({event_code}4634)""",
    """\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|((?i)am|pm|\d{4}|({dest_host}[\w\-.]+)))\s""",
    """Computer(Name)?\s*\\*"?(=|:|>)\s*"*(::ffff:)?((?i)am|pm|({host}[\w\.-]+))(\s|,|"|</Computer>|$)""",

    """exa_json_path=$.TimeCreated,exa_regex=[\\\/]*Date\(({time}\d{13})"""
    """exa_json_path=$.times[0].EventTime,exa_field_name=time"""
    """exa_regex=({event_name}An account was logged off)"""
    """exa_json_path=$..TargetUserSid,exa_regex=(SYSTEM|({user_sid}\S+))"""
    """exa_json_path=$..TargetUserName,exa_regex=(SYSTEM|ANONYMOUS LOGON|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$..TargetDomainName,exa_regex=(-|NT AUTHORITY|({domain}[^\s\\"]+))"""
    """exa_json_path=$..TargetLogonId,exa_field_name=login_id"""
    """exa_json_path=$..LogonType,exa_field_name=login_type"""
    """exa_json_path=$.EventID,exa_field_name=event_code"""
    """exa_json_path=$.Computer,exa_field_name=host"""
  ]
  DupFields = ["login_id->dest_login_id" , "user_sid->dest_user_sid" , "domain->dest_domain", "user->dest_user"]


}
```