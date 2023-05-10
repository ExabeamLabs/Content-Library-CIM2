#### Parser Content
```Java
{
Name = citrix-cgateway-str-app-notification-svr_output_handler
 ParserVersion = v1.0.0
 Vendor = Citrix
 Product = Citrix Gateway
 TimeFormat = "MM/dd/yyyy:HH:mm:ss"
 Conditions = [ """svr_output_handler""" ]
 Fields =[
   """({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d \w+)\s+({host}[\w.\-]+)(\s+\S+){3}\s+({event_name}SSLVPN Message)?\s.*?user\s*({user}[^\s]+)\s*clientip\s*({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s*(request:\s*({action}[^\s]+))?""",
   """({event_name}svr_output_handler)""",
   """response-({result}\d+)"""
 ]


}
```