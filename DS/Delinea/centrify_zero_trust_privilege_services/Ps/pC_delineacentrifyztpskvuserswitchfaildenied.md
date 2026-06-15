#### Parser Content
```Java
{
Name = "delinea-centrifyztps-kv-user-switch-fail-denied"
Vendor = "Delinea"
Product = "Centrify Zero Trust Privilege Services"
TimeFormat = "epoch_sec"
Conditions = [
"""Centrify Suite|dzdo"""
"""dzdo denied"""
]
Fields = [
"""utc=({time}\d{10})"""
"""\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w.\-]+)\s"""
"""user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\d+\|\d+\|({event_name}.+?)\|\d"""
"""status=({result}.+?)\s\w+="""
"""pid=({process_id}\d+)"""
"""service=({service_name}.+?)\s\w+="""
"""runas=({account}({dest_user}.+?))\s\w+="""
"""EntityName =({domain}[^\\]+)\\+({dest_host}[\w\-\.]+)"""
"""command=({process_path}({process_dir}.*?)(\/+({process_name}[^\/]+?))?)\s*(\w+=|$)"""
"""centrifyEventID=({event_code}\d+)"""
]
ParserVersion = "v1.0.0"


}
```