#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-file-5058
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  Conditions = [ """5058""", """Key file operation""" ]
  Fields = ${DLWindowsParsersTemplates.raw-object-access.Fields} [
    """({event_name}Key file operation)""",
    """EventID="+({event_code}[^"]+)""",
    """EventType="+({result}[^"]+)""",
    """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d+)\S+\s({host}[^\s]+)"""
    """File Path:\s*({file_path}(({file_dir}[^=]+[^\\])\\+)?({file_name}[^\s]+))\s*Operation:"""
  ]

raw-object-access = {
  Vendor = Microsoft
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss"]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d[+-]\d\d:\d\d)\s+({host}[\w.-]+)\s""",
    """EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+({event_code}\d+)""",
    """\WexternalId=({event_code}\d+)""",
    """(?i)\w+\s+\d+\s+\d+:\d+:\d+\s+(am|pm|({host}[\w\-.]+))""",
    """Computer(Name)?\s*\\*"?(=|:|>)\s*"*({host}[\w\.-]+)(\s|,|"|</Computer>|$)""",
    """Security ID:\s*({user_sid}\S+)\s+Account Name:""",
    """Account Name:\s*(LOCAL SERVICE|({user}[\w\.\-]{1,40}\$?))\s+Account Domain:""",
    """Account Domain:\s*(NT AUTHORITY|({domain}\S+))\s+Logon ID:""",
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
  
}
```