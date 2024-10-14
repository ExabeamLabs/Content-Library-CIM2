#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-group-member-list-success-4799
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """A security-enabled local group membership was enumerated""", """Security ID:""" ]
  Fields = [
    """({event_name}A security-enabled local group membership was enumerated)""",
    """Security ID:\s+({user_sid}[^\s]+?)\s+Account Name:"""
    """Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:"""
    """Account Domain:\s+({domain}[^:]+?)\s+Logon ID:"""
    """Logon ID:\s+({login_id}[^\s:]+?)\s+Group:"""
    """Group Name:\s+({group_name}[^:]+?)\s+Group Domain:\s+({group_domain}[^:]+?)\s+Process Information:"""
    """Process ID:\s+({process_id}[^\s:]+?)\s+Process Name:"""
    """Process Name:\s+(-|({process_path}({process_dir}(\w:)?(?:[^:"]+)?[\\\/])?({process_name}[^"]+?)))\s*("|$)"""
  ]
  ParserVersion = "v1.0.0"


}
```