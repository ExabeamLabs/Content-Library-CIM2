#### Parser Content
```Java
{
Name = "microsoft-evsecurity-str-registry-create-success-4657"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """4657""", """A registry value was modified""", """Subject:""", """Object:""" ]
  Fields = [
    """({time}\w+\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)\s+({event_code}4657)"""
    """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(AM|PM))""",
    """EventCode=({event_code}\d+)""",
    """ComputerName =({host}[^\s]+)""",
    """Keywords=({result}[^=]+?)\s+\w+=""",
    """\w+\s{1,2}\d{1,2}\s\d\d:\d\d:\d\d\s({host}[\w\-.]+)\s\w+"""
    """({event_name}A registry value was modified)"""
    """Subject:[^"]+?Security ID:\s*({user_sid}[^:]+?)\s+Account Name:"""
    """Subject:[^"]+?Account Name:\s*(LOCAL|({user}[^\s]+))"""
    """Subject:[^"]+?Account Domain:\s*({domain}[^"]+?)\s*Logon ID:"""
    """Subject:[^"]+?Logon ID:\s*({login_id}[^\s]+)"""
    """Object:[^"]+?Handle ID:\s*({handle_id}[^\s]+)"""
    """Process Information:\s*Process ID:\s*({process_id}[^\s]+)"""
    """Process Name:\s*(?:|({process_path}({process_dir}(\w:)?(?:[^:;]+)?[\\\/])?({process_name}[^\\\/";]+?)))\s*Change Information:"""
    """New Value Type:\s*(-|({registry_details_type}[^"]+?))\s*New Value:"""
    """New Value:\s*(-|({registry_details}[^"]+?))\s*-\d{10}"""
    """Operation Type:\s*({operation}[^:]+?)\s*Process Information:"""
    """Logon ID:\s*({login_id}[^\s]+)\s"""
    """Process ID:\s*({process_id}[^\s]+)\s*Process"""
    """Object Name:\s*\\REGISTRY\\({registry_key}[^"]+?)\s*Object Value Name:"""
    """Object Value Name:\s*({registry_value}[^"]+?)\s*Handle ID:"""
    """\(EventID\s({event_code}\d+)\)"""
  ]
  ParserVersion = "v1.0.0"


}
```