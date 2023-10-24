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
    """Subject:[^"]+?Account Name:\s*(LOCAL|({user}[\w\.\-]{1,40}\$?))"""
    """Subject:[^"]+?Account Domain:\s*(\\r|\\t|\\n)*({domain}[^"]+?)\s*(\\r|\\t|\\n)*Logon ID:"""
    """Logon ID(:|=)\s*(\\r|\\t|\\n)*({login_id}[^\\]+)[\s;]*(\\r|\\t|\\n)*"""
    """Object:[^"]+?Handle ID:\s*(\\r|\\t|\\n)*({handle_id}[^\\\s]+)[\s;]*(\\r|\\t|\\n)*"""
    """Process Information:\s*Process ID:\s*({process_id}[^\s]+)"""
    """Process Name:\s*(?:|({process_path}({process_dir}(\w:)?(?:[^:;]+)?[\\\/])?({process_name}[^\\\/";]+?)))\s*Change Information:"""
    """New Value Type:((\\)[rnt])*\s*(-|({registry_details_type}[^"]+?))((\\)[rnt])*\s*New Value:"""
    """New Value:\s*<({registry_details}.+?)\s*("|>|$)"""
    """Operation Type:((\\)[rnt])*\s*({operation}[^:]+?)((\\)[rnt])*\s*Process Information:"""
    """Logon ID:\s*({login_id}[^\s]+)\s"""
    """Process ID(:|=)((\\)[rnt])*\s*({process_id}[^=:]+?)((\\)[rnt])*\s*Process Name(:|=)"""
    """Object Name:((\\)[rnt])*\s*({registry_path}[^"]+?({registry_key}[^"]+?))((\\)[rnt])*\s*Object Value Name"""
    """Object Value Name:((\\)[rnt])*\s*({registry_value}[^"]+?)((\\)[rnt])*\s*Handle ID:"""
    """\(EventID\s({event_code}\d+)\)"""
  ]
  ParserVersion = "v1.0.0"


}
```