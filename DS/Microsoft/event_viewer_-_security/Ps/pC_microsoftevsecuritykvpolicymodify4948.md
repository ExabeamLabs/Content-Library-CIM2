#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-policy-modify-4948
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """EventCode=4948""", """Microsoft Windows security auditing""", """A change was made to the Windows Firewall exception list""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s((?i)AM|PM))""",
    """ComputerName =({host}[\w\-.]+)""",
    """EventCode=({event_code}\d+)\s""",
    """Rule Name:\s*({rule}[^:]+)""",
    """Rule ID:\s*({rule_id}[^\s]+)\s""",
    """Message=({event_name}({additional_info}[^\.]+))""",
    """Keywords=({result}[^=]+)\s\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```