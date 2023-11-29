#### Parser Content
```Java
{
Name = "logrhythm-l-kv-process-create-success-pid"
Vendor = "LogRhythm"
Product = "LogRhythm"
TimeFormat = "MM/dd/yyyy HH:mm:ss"
Conditions = [
""" TIMESTAMP="""
""" PNAME="""
""" PID="""
]
Fields = [
"""TIMESTAMP=({time}\d+\/\d+\/\d\d\d\d\s\d+:\d+:\d+)"""
"""EVENT=({event_name}[^\s]+)"""
"""PID=({process_id}\d+)"""
"""PNAME=({process_name}[^\s]+)"""
"""PROTOCOL=({protocol}[^\s]+)"""
"""ORIGIN=({host}[^\s]+)"""
"""OWNER=(({domain}[^\\]+?)\\+)?({user}[\w\.\-]{1,40}\$?)"""
"""logonusers=(({domain}[^\\]+?)\\+)?({user}[\w\.\-]{1,40}\$?)"""
"""LOCALIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\sLOCALPORT=({src_port}\d+)\sREMOTEIP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\sREMOTEPORT=({dest_port}\d+)"""
]
ParserVersion = "v1.0.0"


}
```