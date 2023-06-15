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
   """({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d \w+)\s+({host}[\w.\-]+)(\s+\S+){3}\s+({event_name}SSLVPN Message)?\s.*?user\s*({user}[^\s]+)\s*clientip\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*(request:\s*({action}[^\s]+))?""",
   """({event_name}svr_output_handler)""",
   """response-({result}\d+)"""
 ]


}
```