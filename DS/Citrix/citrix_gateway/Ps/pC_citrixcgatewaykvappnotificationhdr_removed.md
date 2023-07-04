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
   """({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d \w+)\s+({host}[\w.\-]+)(\s+\S+){3}\s+({event_category}SSLVPN Message)?\s.*?user\s*(-|({email_address}[^@"\s]+@[^@"\s]+)|({user}[\w.-]+))\s*clientip\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*(request:\s*({action}[^\s]+))?""",
   """({event_name}sslvpn_process_sso_conn)"""
 ]


}
```