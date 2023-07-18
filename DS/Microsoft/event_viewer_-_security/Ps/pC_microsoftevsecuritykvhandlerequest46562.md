#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-handle-request-4656-2
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """4656""", """A handle to an object was requested""", """Computer""" ]
  Fields = [
    """Computer(Name)?\s*\\*"?(=|:|>)\s*"*({host}[\w\.-]+)(\s|,|"|</Computer>|$)""",
    """({event_code}4656)""",
    """({time}\w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+4656\s""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d)\s(AM|PM|am|pm)""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """({event_name}A handle to an object was requested)""",
    """Security ID:\s*({user_sid}\S+)\s+Account Name:""",
    """Account Name:\s*({user}\S+)\s+Account Domain:""",
    """Account Domain:\s*({domain}\S+)\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+Object:""",
    """Object Server:\s*({object_server}\S.*?)\s+Object Type:""",
    """Object Type:\s*({object_class}\S+)\s*Object Name:""",
    """Object Name:\s*({object}\S.*?)\s*Handle ID:""",
    """Process ID:\s*({process_id}[^\s]*)""",
    """Process Name:\s*({process_path}({process_dir}.+)[\\\/]({process_name}.+?))\s*Access Request Information:""",
    """Transaction ID:\s*(\{)*({transaction_id}[^\{\s]+)(\})*\s*Accesses:""",
    """Accesses:\s*({access}\S.*?)\s*Access Reasons:""",
    """Access Reasons:\s*(-|({access}\S.*?))\s*Access Mask:""",
    """Privileges Used for Access Check:\s*(-|({privileges}.*?))\s*Restricted SID Count:""",
    """({operation_type}requested)""",
    """Handle ID:\s*({object_id}.+?)\s""",
  ]
  DupFields = [ "host->dest_host" ]


}
```