#### Parser Content
```Java
{
Name = "lumension-l-cef-peripheral-storage-activity-success-devicecontrol"
Vendor = "Lumension"
Product = "Lumension"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Lumension|"""
"""|Lumension Device Control|"""
]
Fields = [
"""art=({time}\d{13})"""
"""shost=({src_host}[^\s]+)\s"""
"""msg=({operation}[^\s]+)"""
"""\|Device Control Event\|({priority}[^|]+)\|"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""cs1=({device_class}[^\s]+)"""
"""cs2=({device_description}[^\s]+)"""
"""cs3=({device_id}[^\s]+)"""
"""sourceServiceName =({user_sid}[^\s]+)"""
"""suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
]
ParserVersion = "v1.0.0"


}
```