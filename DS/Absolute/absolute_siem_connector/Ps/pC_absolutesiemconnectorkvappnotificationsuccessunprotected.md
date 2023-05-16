#### Parser Content
```Java
{
Name = absolute-siemconnector-kv-app-notification-success-unprotected
  ParserVersion = "v1.0.0"
  Vendor = Absolute
  Product = Absolute SIEM Connector
  TimeFormat = "yyyy-MM-dd HH:mm:ss z"
  Conditions = [ """AbsoluteSIEMConnector""", """eventType="DeviceBecameAVUnprotected"""", """verb="Unprotected"""" ]
  Fields = [
    """date="({time}\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2}\s\w{3})""",
    """\s({host}[\w\-.]+)\sAbsoluteSIEMConnector""",
    """actorType=("Device".+?actorName ="({src_host}[\w\-.]+)|"User".+?actorName ="(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[^"\s]+)))"""",
    """objectID="({object}[^"]+)"""",
    """({operation}DeviceBecameAVUnprotected)""",
    """objectProperties="({additional_info}.+?)"\s+\w+="""
   ]
   DupFields = ["operation -> event_name"]


}
```