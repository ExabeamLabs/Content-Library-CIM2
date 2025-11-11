#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-delete-fail-4743"
  Vendor = Microsoft
  Product = Event Viewer - Security	 
  ParserVersion = "v1.0.0"
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """EventCode=4743""", """Message=A computer account was deleted.""", """SourceName =Microsoft Windows security auditing""", """Target Computer:""", """TaskCategory=Computer Account Management""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(AM|PM))""",
    """EventCode=({event_code}\d+)""",
    """ComputerName =({host}[\w\-.]+)""",
    """Keywords=({result}[^=]+?)\s+\w+=""",
    """Message=({event_name}[^:]+?)\s+\w+:""",
    """Subject:\s+Security ID:\s+({user_sid}[^:]+?)\s+Account Name:""",
    """Subject:.+?Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:""",
    """Subject:.+?Account Domain:\s+({domain}[^:]+?)\s+Logon ID:""",
    """Subject:.+?Logon ID:\s+({login_id}[^\s]+)""",
    """Target Computer:\s+Security ID:\s+({dest_user_sid}[^:]+?)\s+Account Name:""",
    """Target Computer:.+?Account Name:\s+({account_name}({dest_user}[^:]+?))\s+Account Domain:""",
    """Target Computer:.+?Account Domain:\s+({dest_domain}[^:]+?)\s+Additional Information:""",
    """Privileges:\s+(-|({privileges}.+?))\s*(\w+=|$)"""
  ]


}
```