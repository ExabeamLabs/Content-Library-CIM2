#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-peripheral-storage-insert-success-6422"
Conditions = [ """Microsoft-Windows-Security-Auditing""" ,"""<EventID>6422</EventID>"""]
ParserVersion = "v1.0.0"

microsoft-json-events.Fields}[
    """Subject:\s+Security ID:\s+({user_sid}[^\s]+)""",
    """Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """Account Domain:\s+({domain}[^\s]+)""",
    """Logon ID:\s+({login_id}[^\s]+)""",  
    """Share Information:\s+Object Type:\s+({file_type}[^:]+?)\s+Share Name:""",
    """Share Name:\s+(?:[\\\*]+)?({share_name}[^\s]+)\s+Share Path:""",
    """Share Path:\s*[\\\?]*({share_path}(({d_parent}[^@]+?)\\)?(|({d_name}[^\\]+?)))\s*Old Remark:"""
  
}
```