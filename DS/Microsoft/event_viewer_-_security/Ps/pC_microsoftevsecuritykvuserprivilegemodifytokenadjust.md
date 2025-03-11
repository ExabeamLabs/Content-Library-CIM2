#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-privilege-modify-tokenadjust
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""A token right was adjusted.""", """Enabled Privileges:""", """Disabled Privileges:"""]
  Fields = [
    """ComputerName =({host}[\w\-\.]+)""",
    """({event_code}4703)""",
    """({event_name}A token right was adjusted)""",
    """Subject:[^:]+Security ID:\s*({user_sid}[^:<]+?)\s*(<14>)?\s*Account Name:""",
    """Subject:[^:]+Security ID:[^:]+Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(<14>)?\s*Account Domain:\s*({domain}[^:<]+?)\s*(<14>)?\s*Logon ID:\s+({login_id}[^\s]+)""",
    """Target Account:[^:]+?Security ID:\s*(NULL SID|({dest_user_sid}[^:<]+?))\s*(<14>)?\s*Account Name:""",
    """Target Account:[^:]+Security ID:[^:]+?Account Name:\s*(SYSTEM|({dest_user}[^:<]+?))\s*(<14>)?\s*Account Domain:\s*({dest_domain}[^\s]+?)\s*(<14>)?\s*Logon ID:""",
    """Enabled Privileges:\s+(-|({privileges}[^:]+?))\s*(<14>)?Disabled Privileges:""",
    """Process ID:\s+({process_id}[^<:]+?)\s*(<14>)?\s*Process Name:""",
    """Process Name:\s*(-|({process_path}({process_dir}(?:[^<=]+)?[\\\/])?({process_name}[^\\\/<:]+?)))[\s\<\>\d]+Enabled Privileges:"""
  ]


}
```