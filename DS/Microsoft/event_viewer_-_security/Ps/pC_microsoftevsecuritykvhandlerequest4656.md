#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-handle-request-4656
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """4656""", """A handle to an object was requested""" ]
  Fields = [
    """(?i)\w+\s*\d+\s*\d\d:\d\d:\d\d (::ffff:)?(am|pm|({host}[\w\-.]+))""",
    """Computer(Name)?\s*\\*"?(=|:|>)\s*"*(::ffff:)?({host}[\w\.-]+)(\s|,|"|</Computer>|$)""",
    """({event_code}4656)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d)\s(AM|PM|am|pm)""",
    """({time}\w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+4656\s"""
    """({event_name}A handle to an object was requested)""",
    """Security ID:\s*({user_sid}\S+)\s+Account Name:""",
    """Account Name:\s*({user}\S+)\s+Account Domain:""",
    """Account Domain:\s*(NA|({domain}\S+))\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+Object:""",
    """Object Server:\s*({object_server}\S.*?)\s+Object Type:""",
    """Object Type:\s*({object_class}\S+)\s*Object Name:""",
    """Object Name:\s*({object}\S.*?)\s*Handle ID:""",
    """Process ID:\s*({process_id}[^\s]*)""",
    """Process Name:\s*({process_path}({process_dir}.+)[\\\/]({process_name}.+?))\s*Access Request Information:""",
    """Transaction ID:\s*({transaction_id}[^\s]+)\s*Accesses:""",
    """Accesses:\s*({access}\S.*?)\s*Access Reasons:""",
    """Access Reasons:\s*(-|({access}\S.*?))\s*Access Mask:""",
    """Privileges Used for Access Check:\s*(-|({privileges}.*?))\s*Restricted SID Count:""",
    """({operation_type}requested)""",
    """Handle ID:\s*({object_id}.+?)\s""",
    """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|({dest_host}[\w\-.]+)))"""
  ]
  DupFields = [ "host->dest_host" ]


}
```