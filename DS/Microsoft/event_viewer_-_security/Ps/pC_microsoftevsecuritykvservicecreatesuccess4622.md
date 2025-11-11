#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-service-create-success-4622
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """EventCode=4622""", """SourceName =Microsoft Windows security auditing""", """A security package has been loaded by the Local Security Authority""", """ComputerName =""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d \w\w)""",  
    """({event_code}4622)""",
    """ComputerName =({dest_host}({host}[\w\-\.]+))""",
    """({event_name}A security package has been loaded by the Local Security Authority)""",
    """Keywords=({result}[^=]+?)\s*\w+=""",
    """Security Package Name:\s*({service_name}[^$]+?)\s*("|$)""",
    """RecordNumber=({event_id}\w+)""",
  ]
  ParserVersion = "v1.0.0"


}
```