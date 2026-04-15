#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-disable-success-4725-1"
Conditions = [
"""A user account was disabled"""
"""event_id\":4725"""
"""computer_name"""
]
ParserVersion = "v1.0.0"

0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssz"
    Fields = [
      """devTime=({time}[^=]+)\s+\w+="""
      """cat=({result}[^=]+?)\s+\w+="""
      """sev=({severity}\d+)"""
      """application=({app}[^=]+?)\s+\w+="""
      """Logon ID:\s+({login_id}\w+)"""
      """Group Name:\s+({group_name}[^:]+?)\s+Group Domain:\s+({group_domain}[^:]+?)\s+"""
      """Changed Attributes:\s+({attribute}[^:=]+?)\s+Account"""
      """message=({event_name}[^=]+?)\s+Subject:"""
      """\|Microsoft\|Windows\|\w+\|({event_code}\d+)"""
    
}
```