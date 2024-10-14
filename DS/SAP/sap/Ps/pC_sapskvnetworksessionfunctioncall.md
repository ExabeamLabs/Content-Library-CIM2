#### Parser Content
```Java
{
Name = sap-s-kv-network-session-functioncall
  Conditions = [ """ - SAP: """, """ - SAP Audit """, """ - SAP User: """, """Audit Class: RFC Function Call""", """: Successful RFC call.""" ]
  ParserVersion = "v1.0.0"

sap-events = {
      Vendor = SAP
      Product = SAP
      TimeFormat = "yyyy/MM/dd HH:mm:ss"
      Fields = [
        """({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)""",
        """Location:\s+({host}[^\s]+)""",
        """User:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
        """Descr:\s+({event_name}[^.]+)""",
        """- SAP:\s+({activity_id}[^\s]+)""",
        """({result}Successful|successful|failed|Failed)"""
     
}
```