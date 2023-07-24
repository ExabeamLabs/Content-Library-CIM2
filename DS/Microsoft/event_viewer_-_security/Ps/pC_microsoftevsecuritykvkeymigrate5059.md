#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-key-migrate-5059
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Product = Event Viewer - Security
  Conditions = [ """5059""", """Key migration operation""" ]
  Fields = ${DLWindowsParsersTemplates.raw-object-access.Fields} [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9})-\d\d:\d\d\s[^\s]+""",
    """"EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """({host}[^\s]+)\sMicrosoft-Windows-Security-Auditing""",
    """EventID="*({event_code}\d+)""",
    """({event_name}Key migration operation)""",
    """"(?i)HostName":\s*"({host}[^"]+)""""
  ]

raw-object-access = {
  Vendor = Microsoft
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d[+-]\d\d:\d\d)\s+({host}[\w.-]+)\s""",
    """EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+({event_code}\d+)""",
    """\WexternalId=({event_code}\d+)""",
    """(?i)\w+\s+\d+\s+\d+:\d+:\d+\s+(am|pm|({host}[\w\-.]+))""",
    """Computer(Name)?\s*\\*"?(=|:|>)\s*"*({host}[\w\.-]+)(\s|,|"|</Computer>|$)""",
    """Security ID:\s*({user_sid}\S+)\s+Account Name:""",
    """Account Name:\s*(LOCAL SERVICE|({user}\S+))\s+Account Domain:""",
    """Account Domain:\s*(NT AUTHORITY|({domain}\S+))\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+Cryptographic Parameters:""",
    """Provider Name:\s*({provider_name}.+?)\s+Algorithm Name:""",
# algorithm_name is removed
    """Key Name:\s*({key_name}.+?)\s+Key Type:""",
    """Key Type:\s*({key_type}.+?)\s+(Key File Operation Information|Additional Information|Cryptographic Operation)""",
    """File Path:\s*({file_path}.+?)\s+Operation:""",
    """Operation:\s*({operation}[^:]+?)\s+Return Code:""",
    """Return Code:\s*({return_code}.+?)\s*(User:|<\/Message>)""",
    """EventID="*({event_code}\d+)""",
    """EventType="*({result}[^"\s]+)"""
  
}
```