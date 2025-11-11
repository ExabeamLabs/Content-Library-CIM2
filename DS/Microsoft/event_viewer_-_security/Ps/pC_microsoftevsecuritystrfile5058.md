#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-file-5058
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  Conditions = [ """5058""", """Key file operation""" ]
  Fields = ${DLWindowsParsersTemplates.raw-object-access.Fields} [
    """Account Name:\s*(LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:""",
    """Account Domain:\s*(NT AUTHORITY|({domain}\S+))\s+Logon ID:""",
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d[+-]\d\d:\d\d)\s+({host}[\w.-]+)\s""",
    """(?i)\w+\s+\d+\s+\d+:\d+:\d+\s+(am|pm|\d{4}|({host}[\w\-.]+))\s""",
    """Computer(Name)?\s*\\*"?(=|:|>)\s*"*({host}[\w\.-]+)(\s|,|"|</Computer>|$)""",
    """({event_name}Key file operation)""",
    """({event_code}5058)"""
    """EventID="+({event_code}[^"]+)""",
    """EventType="+({result}[^"]+)""",
    """File Path:\s*({file_path}(({file_dir}[^=]+[^\\])\\+)?({file_name}[^\s]+?(\.({file_ext}[^\s\.]+))?))\s*Operation:"""
  ]

raw-object-access = {
  Vendor = Microsoft
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ssZ", "epoch", "MM/dd/yyyy HH:mm:ss a", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSS"]
  Fields = [
    """EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+({event_code}\d+)""",
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d\d\d\d\d\d)?[+-]\d\d:\d\d)\s+""",
    """\WexternalId=({event_code}\d+)""",
    """Security ID:\s*({user_sid}\S+)\s+Account Name:""",
    """Logon ID:\s*({login_id}\S+)\s+Cryptographic Parameters:""",
    """Provider Name:\s*({provider_name}.+?)\s+Algorithm Name:""",
# algorithm_name is removed
    """Key Name:\s*({key_name}.+?)\s+Key Type:""",
    """Key Type:\s*({key_type}.+?)\.?\s+(Key File Operation Information|Additional Information|Cryptographic Operation)""",
    """File Path:\s*({file_path}.+?)\s+Operation:""",
    """Operation:\s*({operation}[^:]+?)\s+Return Code:""",
    """Return Code:\s*({return_code}.+?)\s*(User:|<\/Message>)""",
    """EventID="*({event_code}\d+)""",
    """EventType="*({result}[^"\s]+)"""
    """<TimeCreated SystemTime(\\)?=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
  
}
```