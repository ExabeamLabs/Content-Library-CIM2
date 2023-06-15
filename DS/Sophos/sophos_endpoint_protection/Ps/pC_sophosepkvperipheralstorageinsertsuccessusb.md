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
     """ComputerIPAddress=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
     """ReportingName =({device_id}[^;]+)""",
     """ReportingName =({device_type}.+?)(/|;)""",
     """ComputerDomain=({domain}[^;]+)""",
  ]
  DupFields = ["result->operation_details"]
  ParserVersion = "v1.0.0"


}
```