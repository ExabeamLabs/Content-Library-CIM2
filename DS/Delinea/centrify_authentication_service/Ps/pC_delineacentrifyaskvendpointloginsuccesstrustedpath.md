#### Parser Content
```Java
{
Name = "delinea-centrifyas-kv-endpoint-login-success-trustedpath"
   ParserVersion = "v1.0.0"
   Vendor = "Delinea"
   Product = "Centrify Authentication Service"
   TimeFormat = "epoch"
   Conditions = [ 
"""|Centrify Suite|Trusted Path|"""
"""|Trusted path granted|""" 
]
   Fields = [
"""utc=({time}\d{13})"""
"""user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\("""
"""user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\(\)\s@]+)\s+(\w+=|$)"""
"""\|({event_name}Trusted path\s+[^\|]*)\|"""
"""status=({result}.+?)\s+(\w+=|$)"""
"""pid=({process_id}\d+)"""
"""server=(({protocol}[^\\\/\s]+)[\\\/]+)?({dest_host}[\w\-.]+?)(@({dest_domain}[^\\\/\s]+))?\s*(\w+=|$|")"""
   ]


}
```