#### Parser Content
```Java
{
Name = "microsoft-evsecurity-str-registry-create-success-4657"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
  Conditions = [ """4657""", """A registry value was modified""", """Subject:""", """Object:""" ]
  Fields = [
    """({time}\w+\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)\s+({event_code}4657)"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(AM|PM))""",
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)""",
    """({event_code}\d+)\|\s+devTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """EventCode=({event_code}\d+)""",
    """<Computer>({src_host}({host}[\w\-.]+?))<\/Computer>"""
    """ComputerName =({src_host}({host}[^\s]+))""",
    """Keywords=({result}[^=]+?)\s+\w+=""",
    """\w+\s{1,2}\d{1,2}\s\d\d:\d\d:\d\d\s(\d{4}|({src_host}({host}[\w\-.]+)))\s\w+"""
    """({event_name}A registry value was modified)"""
    """Subject:[^"]+?Security ID:\s*({user_sid}[^:]+?)\s+Account Name:"""
    """Subject:[^"]+?Account Name:\s*(LOCAL|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """Subject:[^"]+?Account Domain:\s*(\\r|\\t|\\n)*({domain}[^"]+?)\s*(\\r|\\t|\\n)*Logon ID:"""
    """Logon ID(:|=)\s*(\\r|\\t|\\n)*({login_id}[^\\]+)[\s;]*(\\r|\\t|\\n)*"""
    """Object:[^"]+?Handle ID:\s*(\\r|\\t|\\n)*({handle_id}[^\\\s]+)[\s;]*(\\r|\\t|\\n)*"""
    """Process Information:\s*Process ID:\s*({process_id}[^\s]+)"""
    """Process Name:\s*(?:|({process_path}({process_dir}(\w:)?(?:[^:;]+)?[\\\/])?({process_name}[^\\\/";]+?)))\s*Change Information:"""
    """New Value Type:((?-i)\\+[rnt])*\s*(-|({registry_details_type}[^"]+?))((?-i)\\+[rnt])*\s*New Value:"""
    """New Value:(\\+[rnt]|\s)*(-|({registry_details}.+?))(\\+[rnt]|\s)*("|<|$)"""
    """Old Value Type:((?-i)\\+[rnt])*\s*(-|({old_registry_details_type}[^"]+?))((?-i)\\+[rnt])*\s*Old Value:"""
    """Old Value:(\\+[rnt]|\s)*(-|({old_registry_details}.+?))(\\+[rnt]|\s)*\s*New Value Type:"""
    """Operation Type:((?-i)\\+[rnt])*\s*({operation}[^:]+?)((?-i)\\+[rnt])*\s*Process Information:"""
    """Logon ID:\s*({login_id}[^\s]+)\s"""
    """Process ID(:|=)((?-i)\\+[rnt])*\s*({process_id}[^=:]+?)((?-i)\\+[rnt])*\s*Process Name(:|=)"""
    """Object Name:((?-i)\\+[rnt])*\s*({registry_path}[^"]+?({registry_key}[^"\\]+?))((?-i)\\+[rnt])*\s*Object Value Name"""
    """Object Value Name:((?-i)\\+[rnt])*\s*({registry_value}[^"]+?)((?-i)\\+[rnt])*\s*Handle ID:"""
    """\(EventID\s({event_code}\d+)\)"""
  ]
  ParserVersion = "v1.0.0"


}
```