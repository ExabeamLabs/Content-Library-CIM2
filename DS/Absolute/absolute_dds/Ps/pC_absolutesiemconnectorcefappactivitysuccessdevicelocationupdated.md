#### Parser Content
```Java
{
Name = absolute-siemconnector-cef-app-activity-success-devicelocationupdated
  Vendor = Absolute
  Product = Absolute DDS
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss z"
  Conditions = [ """AbsoluteSIEMConnector""", """eventType="DeviceLocationUpdated"""", """verb="Updated"""" ]
  Fields = [
    """date="({time}\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2}\s\w{3})""",
    """\s({host}[\w\-.]+)\sAbsoluteSIEMConnector""",
    """({operation}DeviceLocationUpdated)""",
    """objectID="({object}[^"]+)"""",
    """actorType=("Device".+?actorName ="({src_host}[\w\-.]+)|"User".+?actorName ="(({email_user}[^"@]+@[^".]+\.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
    """objectProperties="({additional_info}.+?)"\s+\w+="""
   ]
   DupFields = ["operation -> event_name"]


}
```