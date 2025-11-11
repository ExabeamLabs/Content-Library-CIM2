#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-handle-request-4656-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch_sec"
  Conditions = [ "EventIDCode=4656" ]
  Fields = [
    """Computer=\s*({dest_host}({host}[^\s]*))""",
    """EventID=({event_code}\d+)""",
    """TimeGenerated=({time}\d{10})""",
    """Message=({event_name}.*?)\s*Subject\s*:""",
    """Security ID:\s*({user_sid}\S+)\s+Account Name:""",
    """Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:""",
    """Account Domain:\s*({domain}\S+)\s+Logon ID:""",
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
    """({operation_type}requested)"""
  ]


}
```