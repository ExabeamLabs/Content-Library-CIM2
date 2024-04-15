#### Parser Content
```Java
{
Name = "delinea-centrifyas-kv-endpoint-login-fail-trustedpath"
   ParserVersion = "v1.0.0"
   Vendor = "Delinea"
   Product = "Centrify Authentication Service"
   TimeFormat = "epoch"
   Conditions = [ 
"""|Centrify Suite|Trusted Path|"""
"""|Trusted path denied|""" 
]
   Fields = [
"""utc=({time}\d{13})"""
"""user=({user}[^\(\)\s@]+)\("""
"""user=({user}[^\(\)\s@]+)@({domain}[^\(\)\s@]+)\s+(\w+=|$)"""
"""\|({event_name}Trusted path\s+[^\|]*)\|"""
"""status=({result}.+?)\s+(\w+=|$)"""
"""pid=({process_id}\d+)"""
"""server=(({protocol}[^\\\/\s]+)[\\\/]+)?({dest_host}[^\\\/\s]+?)\s+(\w+=|$)"""
"""reason=:?\s*({failure_reason}.+?)\s+(\w+=|$)"""
   ]


}
```