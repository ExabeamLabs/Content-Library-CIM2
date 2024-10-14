#### Parser Content
```Java
{
Name = "delinea-centrifyas-cef-endpoint-login-fail-sshd"
   ParserVersion = "v1.0.0"
   Vendor = "Delinea"
   Product = "Centrify Authentication Service"
   TimeFormat = "epoch"
   Conditions = [ 
"""Centrify Suite|Centrify"""
"""SSHD denied""" 
]
   Fields = [
"""utc=({time}\d{13})""",
"""\sahost=({host}[^=]+?)\s+\w+="""
"""\sclient=(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^=]+?))\s+\w+="""
"""user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\d+\|\d+\|({event_name}.+?)\|\d"""
"""status=({result}.+?)\s\w+="""
"""pid=({process_id}\d+)"""
"""service=({process_path}.+?)\s\w+="""
"""EntityName =(.+\\+)?({dest_host}[^\"\s]+)(\s|$)"""
"""reason=({failure_reason}[^=\|]+?)(\s+\w+=|\|)"""
   ]


}
```