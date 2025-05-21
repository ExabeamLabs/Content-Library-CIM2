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
     """UserName =([^\\]+\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?);""",
     """Action=({result}[^;]+);""",
     """({additional_info}SubType=[^;]+)""",
     """ComputerName =({dest_host}[^;]+);""",
     """ComputerIPAddress=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
     """ReportingName =({device_id}[^;]+)""",
     """ReportingName =({device_class}.+?)(/|;)""",
     """ComputerDomain=({domain}[^;]+)""",
     """USB\\+VID_({device_vid}[^&]+)&PID_({device_pid}[^\\&]+)"""
  ]
  DupFields = ["result->operation_details"]
  ParserVersion = "v1.0.0"


}
```