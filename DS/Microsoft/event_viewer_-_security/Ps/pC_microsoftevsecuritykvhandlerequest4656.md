#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-handle-request-4656
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """4656""", """A handle to an object was requested""" ]
  Fields = [
    """(?i)\w+\s*\d+\s*\d\d:\d\d:\d\d (::ffff:)?(am|pm|\d{4}|({dest_host}({host}[\w\-.]+)))\s""",
    """Computer(Name)?\s*\\*"?(=|:|>)\s*"*(::ffff:)?({dest_host}({host}[\w\.-]+))(\s|,|"|</Computer>|$)""",
    """({event_code}4656)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d)\s(AM|PM|am|pm)""",
    """({time}\w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+4656\s"""
    """({event_name}A handle to an object was requested)""",
    """Security ID:\s*({user_sid}\S+)\s+Account Name:""",
    """Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:""",
    """Account Domain:\s*(NA|({domain}\S+))\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+Object:""",
    """Object Server:\s*({object_server}\S.*?)\s+Object Type:""",
    """Object Type:(\s|\\[rnt])*({object_class}\S+?)(\s|\\[rnt])*Object Name:""",
    """Object Name:\s*(\\t|\\n|\\r)*({object}\S.*?)\s*(\\t|\\n|\\r)*Handle ID:""",
    """Process ID:\s*(\\t|\\n|\\r)*({process_id}[^\\\s]+)""",
    """Process Name:\s*(\\t|\\n|\\r)*({process_path}({process_dir}[^=]*?)(\\+({process_name}[^\\]+?))?)\s*(\\t|\\n|\\r)*Access Request Information:""",
    """Transaction ID:\s*(\\t|\\n|\\r)*({transaction_id}[^\\\s]+)\s*(\\t|\\n|\\r)*Accesses:""",
    """Accesses:\s*(\\t|\\n|\\r)*({access}[^\\\s]+)\s*(\\t|\\n|\\r)*""",
    """Access Reasons:\s*(\\t|\\n|\\r)*(-|({access}\S.*?))\s*(\\t|\\n|\\r)*Access Mask:""",
    """Privileges Used for Access Check:\s*(\\t|\\n|\\r)*(-|({privileges}.*?))\s*(\\t|\\n|\\r)*Restricted SID Count:""",
    """({operation_type}requested)""",
    """Handle ID:\s*(\\t|\\n|\\r)*({object_id}[^\\\s]+)\s*(\\t|\\n|\\r)*""",
    """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|\d{4}|({dest_host}[\w\-.]+)))\s"""
  ]


}
```