#### Parser Content
```Java
{
Name = citrix-cgateway-kv-app-notification-hdr_removed
 ParserVersion = v1.0.0
 Vendor = Citrix
 Product = Citrix Gateway
 TimeFormat = "MM/dd/yyyy:HH:mm:ss"
 Conditions = [ """sslvpn_process_sso_conn""" , """hdr_removed""" ]
 Fields =[
   """({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d \w+)\s+({host}[\w.\-]+)(\s+\S+){3}\s+({event_category}SSLVPN Message)?\s.*?user\s*({user}[^\s]+)\s*clientip\s*({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s*(request:\s*({action}[^\s]+))?""",
   """({event_name}sslvpn_process_sso_conn)"""
 ]


}
```