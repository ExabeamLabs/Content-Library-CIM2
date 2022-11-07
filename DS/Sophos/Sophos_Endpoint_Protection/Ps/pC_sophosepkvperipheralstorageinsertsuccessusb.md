#### Parser Content
```Java
{
Name = sophos-ep-kv-peripheral-storage-insert-success-usb
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Action=""", """EventType=Device control;""", """ReportingName =""", """ComputerIPAddress=""", """InsertedAt=""", """USB""" ]
  Fields = [
     """EventID=({event_code}[\d]+);""",
     """EventTime=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
     """EventType=({operation}[^;]+);""",
     """UserName =([^\\]+\\+)?({user}[^;]+);""",
     """Action=({result}[^;]+);""",
     """({additional_info}SubType=[^;]+)""",
     """ComputerName =({dest_host}[^;]+);""",
     """ComputerIPAddress=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
     """ReportingName =({device_id}[^;]+)""",
     """ReportingName =({device_type}.+?)(/|;)""",
     """ComputerDomain=({domain}[^;]+)""",
  ]
  DupFields = ["result->activity_details"]
  ParserVersion = "v1.0.0"


}
```