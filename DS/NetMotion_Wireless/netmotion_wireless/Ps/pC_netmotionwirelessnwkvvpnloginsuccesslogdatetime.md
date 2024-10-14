#### Parser Content
```Java
{
Name = "netmotionwireless-nw-kv-vpn-login-success-logdatetime"
Vendor = "NetMotion Wireless"
Product = "NetMotion Wireless"
TimeFormat = "epoch"
Conditions = [
"""POP_Address="""
"""Log_Date_Time"""
]
Fields = [
"""Log_Date_Time=({time}\d{13})"""
"""Device_Name =\"+({src_host}[^\"]+)"""
"""User_Name =\"+([^\\]+\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""POP_Address=\"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""Virtual_Address=\"+({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
]
DupFields = [
"user->account"
]
ParserVersion = "v1.0.0"


}
```