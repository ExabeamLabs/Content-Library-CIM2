#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-handle-request-4656-2
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MM/dd/yyyy hh:mm:ss a", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
  Conditions = [ """4656""", """A handle to an object was requested""", """Computer""" ]
  Fields = [
    """Computer(Name)?\s*\\*"?(=|:|>)\s*"*({host}[\w\.-]+)(\s|,|"|<[\\\/]+Computer>|$)""",
    """({event_code}4656)""",
    """({time}\w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+4656\s""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d\s(AM|PM|am|pm))""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
    """({event_name}A handle to an object was requested)""",
    """Security ID:(\s|\\[rnt])*({user_sid}\S+?)(\s|\\[rnt])*Account Name:""",
    """Account Name:(\s|\\[rnt])*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s|\\[rnt])*Account Domain:""",
    """Account Domain:(\s|\\[rnt])*({domain}\S+?)(\s|\\[rnt])*Logon ID:""",
    """Logon ID:(\s|\\[rnt])*({login_id}\S+?)(\s|\\[rnt])*Object:""",
    """Object Server:(\s|\\[rnt])*({object_server}\S.*?)(\s|\\[rnt])*Object Type:""",
    """Object Type:(\s|\\[rnt])*({object_class}\S+?)(\s|\\[rnt])*Object Name:""",
    """Object Name:(\s|\\[rnt])*({object}\S.*?)(\s|\\[rnt])*Handle ID:""",
    """Process ID:(\s|\\[rnt])*({process_id}\S+?)(\s|\\[rnt])*Process Name:""",
    """Process Name:(\s|\\[rnt])*({process_path}(({process_dir}.+?)[\\\/]+)?({process_name}[^\\\/]+?))(\s|\\[rnt])*Access Request Information:""",
    """Transaction ID:(\s|\\[rnt])*(\{)*({transaction_id}[^\{\s]+?)(\})*(\s|\\[rnt])*Accesses:""",
    """Accesses:(\s|\\[rnt])*({access}\S.*?)(\s|\\[rnt])*Access Reasons:""",
    """Access Reasons:(\s|\\[rnt])*(-|({access}\S.*?))(\s|\\[rnt])*Access Mask:""",
    """Privileges Used for Access Check:(\s|\\[rnt])*(-|({privileges}.*?))(\s|\\[rnt])*Restricted SID Count:""",
    """({operation_type}requested)""",
    """Handle ID:(\s|\\[rnt])*({object_id}\S+?)(\s|\\[rnt])*Resource Attributes:""",
  ]
  DupFields = [ "host->dest_host" ]


}
```