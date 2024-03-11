#### Parser Content
```Java
{
Name = sophos-ep-kv-alert-trigger-web
  ParserVersion = "v1.0.0"
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ReportingName =""","""ComputerIPAddress=""", """Action=Blocked;""", """EventType=Web;""" ]
  Fields = [
     """;\s+EventID=({event_code}[\d]+);""",
     """EventTime=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
     """;\s*EventType=({event_category}[^;]+);""",
     """;\s*Name =({event_name}[^;]+);""",
     """;\s*UserName =([^\\]+\\+)?({user}[^;]+);""",
     """;\s*Action=({action}[^;]+);""",
     """;\s*({additional_info}SubType=[^;]+)""",
     """;\s*ComputerName =({src_host}[^;]+);""",
     """;\s*ComputerIPAddress=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """ComputerDomain=({domain}[^;]+)""",
  ]
DupFields = ["event_name->alert_name"]


}
```