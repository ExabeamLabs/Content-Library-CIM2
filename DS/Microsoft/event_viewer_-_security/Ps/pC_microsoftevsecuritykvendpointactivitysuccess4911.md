#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-activity-success-4911
  Product = Event Viewer - Security
  Vendor = Microsoft
  ParserVersion = v1.0.0
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """EventCode=4911""", """Microsoft Windows security auditing""", """Resource attributes of the object were changed""" ]
  Fields =[
    """ComputerName =({host}[\w\-\.]+)"""
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (AM|PM|am|pm))\sLogName ="""
    """Keywords=({result}[^=]+?)\s\w+="""
    """TaskCategory=({task}[^=]+?)\s*\w+="""
    """({event_name}Resource attributes of the object were changed)"""
    """Subject:\s*Security ID:\s*({user_sid}[^:]+?)\s*Account Name:\s*({user}[^:]+?)\s*Account Domain:\s*({domain}[^:]+?)\s*Logon ID:\s*({login_id}[^:]+?)\s*Object:"""
    """Object Type:\s*({object_type}File)\s*Object Name:\s*(-|({file_path}({file_dir}[^<]+?)({file_name}[^<\\\/]+?(\.({file_ext}[^<\\\/\.]+?))?)))\s* Handle ID:"""
  ]
  

}
```