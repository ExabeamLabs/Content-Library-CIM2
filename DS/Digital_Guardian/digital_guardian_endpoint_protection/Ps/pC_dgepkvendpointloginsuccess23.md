#### Parser Content
```Java
{
Name = "dg-ep-kv-endpoint-login-success-23"
  ParserVersion = "v1.0.0"
  Vendor = "Digital Guardian"
  Product = "Digital Guardian Endpoint Protection"
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ 
"""Operation="23""""
"""Agent_UTC_Time=""" 
]
  Fields = [
"""\s(Agent_UTC_Time|Server_UTC_Timestamp)=\"({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+ (am|AM|pm|PM))\""""
"""\sComputer_Name =\"([^\/\\\"]+[\\\/])?({host}[^\"]+)\""""
"""\sUser_Name =\"(?:|(({domain}[^\"\/\\]+)[\/\\]+)?({user}[\w\.\-]{1,40}\$?))\""""
"""\sDomain_Name =\"(?:|({domain}[^\"]+))\""""
"""\sApplication=\"(?:|({process_name}[^\"]+))\""""
"""\sOperation=\"(?:|({event_code}[^\"]+))\""""
  ]
  DupFields = [ "host->dest_host" ]


}
```