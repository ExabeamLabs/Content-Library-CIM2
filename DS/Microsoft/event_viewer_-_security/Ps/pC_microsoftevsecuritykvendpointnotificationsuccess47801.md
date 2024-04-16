#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-notification-success-4780-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [ 
	"""EventCode=4780"""
	"""Message=The ACL was set on accounts which are members of administrators groups"""
	"""Microsoft Windows security auditing"""
	]
Fields = [
	  """({time}\d+\/\d+\/\d+ \d+:\d+:\d+ (am|AM|pm|PM))""",
    """EventCode=({event_code}\d+)""",
    """ComputerName\=({host}[\w\-.]+?)\s""",
    """Target\sAccount\:(\\t|\\r|\\n|\s)*Security\s+ID\:(\\t|\\r|\\n|\s)*({dest_domain}\w+)\\({dest_user}[\w\.\-]{1,40}\$?)(\\t|\\r|\\n|\s)*""",
    """TaskCategory=({operation_type}.+?)(\\t|\\r|\\n|\s)*OpCode(:|=)"""
    """RecordNumber=({event_id}\d+)"""
    """Keywords=({result}.+?);?(\\t|\\r|\\n|\s)*Message="""
    """Subject:(\\t|\\r|\\n|\s)*Security ID:(\\t|\\r|\\n|\s)*({user_sid}[^:]+?)(\\t|\\r|\\n|\s)*Account Name:"""
    """Subject:[^"]+?Account Name:(\\t|\\r|\\n|\s)*({user}[\w\.\-]{1,40}\$?)(\\t|\\r|\\n|\s)*Account Domain:"""
    """Subject:[^"]+?Account Domain:(\\t|\\r|\\n|\s)*({domain}[^:]+?)(\\t|\\r|\\n|\s)*Logon ID:"""
    """Additional Information:(\\t|\\r|\\n|\s)*Privileges:(\\t|\\r|\\n|\s|\-)*({additional_info}.+?)\.(\w+=|$|")"""
      ]
      DupFields = [ "host->dest_host" ]
ParserVersion = "v1.0.0"


}
```