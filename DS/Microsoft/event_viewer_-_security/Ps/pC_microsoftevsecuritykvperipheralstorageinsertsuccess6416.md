#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-peripheralstorage-insert-success-6416"
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """EventCode=6416""", """A new external device was recognized by the system.""", """ComputerName =""" ]
  Fields = [
    """({time}(\d{2}\/){2}\d{4} (\d{2}:){2}\d{2} (?:am|AM|pm|PM))""",
    """ComputerName =\s*({dest_host}[^=]+?)\s+TaskCategory=""",
    """Account Name:\s*(-\s*|({user}[^:]+?)\s+)Account Domain:""",
    """Security ID:\s*({user_sid}[^:]+?)\s+Account Name:""",
    """Device Name:\s*({device_name}[^:]+?)\s+Class ID:""",
    """Device ID:\s*({device_id}[^:]+?)\s+Device Name:""",
    """Account Domain:\s*(-\s*|({domain}[^:]+?)\s+)Logon ID:""",
    """Location Information:\s*(|-|({additional_info}[^"]*))(\s+|\s*")""",
    """Class Name:\s*({device_type}[^:]+?)\s+(Vendor IDs:|Hardware IDs:)""",
    """hostname":"({dest_host}[^"]+)""",
    """EventCode=({event_code}\d+)\s""",
    """({event_name}A new external device was recognized by the system.)"""
  ]
  DupFields = [ "event_name->operation" ]
  ParserVersion = "v1.0.0"


}
```