#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-peripheral-storage-insert-success-6416
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss Z"
  ExtractionType = json
  Conditions = [ """"EventID":6416""", """A new external device was recognized by the system""", """"ProviderName":"Microsoft-Windows-Security-Auditing"""", """"Channel":"Security""" ]
  Fields = [
    """exa_json_path=$.TimeCreated,exa_field_name=time"""
    """exa_json_path=$.Computer,exa_field_name=host"""
    """exa_json_path=$.ProcessID,exa_field_name=process_id"""
    """exa_json_path=$.EventID,exa_field_name=event_code"""
    """exa_json_path=$.Keywords,exa_field_name=result"""
    """exa_json_path=$.Level,exa_field_name=run_level"""
    """exa_regex=Subject:.+?Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:\s+({domain}.+?)\s+Logon ID:\s+({login_id}[^\s]+)"""
    """exa_regex=Device Name:\s*({device_description}[^:]+?)\s+Class ID:""",
    """exa_regex=Device ID:\s*({device_id}[^:]+?)\s+Device Name:""",
    """exa_regex=Class Name:\s*({device_class}[^:]+?)\s+(Vendor IDs:|Hardware IDs:)"""
    """exa_regex=({event_name}A new external device was recognized by the system.)"""
    """exa_json_path=$.Message,exa_field_name=additional_info"""
  ]

  ParserVersion = "v1.0.0"


}
```