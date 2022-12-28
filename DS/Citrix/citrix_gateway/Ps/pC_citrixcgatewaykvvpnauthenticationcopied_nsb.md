#### Parser Content
```Java
{
Name = citrix-cgateway-kv-vpn-authentication-copied_nsb
 ParserVersion = v1.0.0
 Vendor = Citrix
 Product = Citrix Gateway
 TimeFormat = "MM/dd/yyyy:HH:mm:ss"
 Conditions = [ """nssso_res_hdr_handler""" , """copied_nsb""" ]
 Fields =[
   """({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d \w+)\s+({host}[\w.\-]+)(\s+\S+){3}\s+({event_category}SSLVPN Message)?\s.*?user\s*({user}[^\s]+)\s*clientip\s*({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s*(request:\s*({action}[^\s]+))?""",
   """({event_name}nssso_res_hdr_handler)""",
   """response-({result}\d+)"""
 ]


}
```