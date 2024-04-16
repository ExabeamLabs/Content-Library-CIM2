#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-peripheralstorage-insert-success-6416"
  ExtractionType = json
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """EventCode=6416""", """A new external device was recognized by the system.""", """ComputerName =""" ]
  Fields = [
    """({time}(\d{2}\/){2}\d{4} (\d{2}:){2}\d{2} (?:am|AM|pm|PM))""",
    """ComputerName =\s*({dest_host}[\w\.-]+?)\s+TaskCategory=""",
    """Account Name:\s*(-\s*|({user}[\w\.\-]{1,40}\$?)\s+)Account Domain:""",
    """Security ID:\s*({user_sid}[^:]+?)\s+Account Name:""",
    """Device Name:\s*({device_name}[^:]+?)\s+Class ID:""",
    """Device ID:\s*({device_id}[^:]+?)\s+Device Name:""",
    """Account Domain:\s*(-\s*|({domain}[^:]+?)\s+)Logon ID:""",
    """Location Information:\s*(|-|({additional_info}[^"]*))(\s+|\s*")""",
    """Class Name:\s*({device_type}[^:]+?)\s+(Vendor IDs:|Hardware IDs:)""",
    """hostname":"({dest_host}[\w\-.]+)""",
    """EventCode=({event_code}\d+)\s""",
    """({event_name}A new external device was recognized by the system.)"""

    """exa_regex=({time}(\d{2}\/){2}\d{4} (\d{2}:){2}\d{2} (?:am|AM|pm|PM))""",
    """exa_json_path=$.message,exa_regex=ComputerName =\s*({dest_host}[\w\.-]+?)\s+TaskCategory""",
    """exa_json_path=$.message,exa_regex=Account Name:\s*(-\s*|({user}[\w\.\-]{1,40}\$?)\s+)Account Domain:""",
    """exa_json_path=$.message,exa_regex=Security ID:\s*({user_sid}[^:]+?)\s+Account Name:""",
    """exa_json_path=$.message,exa_regex=Device Name:\s*({device_name}[^:]+?)\s+Class ID:""",
    """exa_json_path=$.message,exa_regex=Device ID:\s*({device_id}[^:]+?)\s+Device Name:""",
    """exa_json_path=$.message,exa_regex=Account Domain:\s*(-\s*|({domain}[^:]+?)\s+)Logon ID:""",
    """exa_json_path=$.message,exa_regex=Location Information:\s*(|-|({additional_info}[^"]*))(\s+|\s*")""",
    """exa_json_path=$.message,exa_regex=Class Name:\s*({device_type}[^:]+?)\s+(Vendor IDs:|Hardware IDs:)""",
    """exa_json_path=$.message,exa_regex=EventCode=({event_code}\d+)\s""",
    """exa_regex="hostname":"({dest_host}[\w\-.]+)""",
    """exa_regex=({event_name}A new external device was recognized by the system.)"""
  ]
  DupFields = [ "event_name->operation" ]
  ParserVersion = "v1.0.0"


}
```