#### Parser Content
```Java
{
Name = "sybase-s-cef-database-query-success-selecttable"
Vendor = "Sybase"
Product = "Sybase"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Sybase|ASE Audit|"""
"""msg=Select table"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdvc=({host}[A-Fa-f:\d.]+)"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""\Wsuser=({user}[^\s]+)"""
"""\Wdhost=({dest_host}[\w\-.]+)"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wcs6=({db_name}.+?)\s+\w+=.+?cs6Label=Database Name"""
"""\Wcs6Label=Database Name.+?cs6=({db_name}.+?)\s+\w+="""
"""\Wcs2=({db_object}.+?)\s+\w+=.+?cs2Label=Object Name"""
"""\Wcs2Label=Object Name.+?cs2=({db_object}.+?)\s+\w+="""
"""\Wcs3=({db_user}.+?)\s+\w+=.+?cs3Label=Object Owner"""
"""\Wcs3Label=Object Owner.+?cs3=({db_user}.+?)\s+\w+="""
"""\Wmsg=({db_operation}\S+)"""
"""\Wcs1=({db_query}.+?)\s+(\w+=|$)"""
"""({app}Sybase)"""
]
DupFields = [
"user->user"
"db_user->account"
]
ParserVersion = "v1.0.0"


}
```