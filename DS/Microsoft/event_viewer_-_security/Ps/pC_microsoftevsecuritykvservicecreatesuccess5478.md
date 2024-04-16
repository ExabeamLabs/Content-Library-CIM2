#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-service-create-success-5478
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["dd/MM/yyyy HH:mm:ss a", "MM/dd/yyyy hh:mm:ss a"]
  Conditions = [ """EventCode=5478""", """SourceName =Microsoft Windows security auditing""", """Message=The IPsec Policy Agent service was started""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d ((?i)AM|PM))""",
    """ComputerName =({host}[\w.-]+)""",
    """EventCode=({event_code}5478)""",
    """Message=({event_name}The IPsec Policy Agent service was started)""",
    """Keywords=({result}[^=]+?)\s*(\w+=|$)""",
    """RecordNumber=({event_id}[^\s]+)""",
    """TaskCategory=({service_type}[^=]+?)\s*(\w+=|$)""",
    """({service_name}IPsec Policy Agent)"""
  ]
  DupFields = ["host->dest_host"]
  ParserVersion = "v1.0.0"


}
```