#### Parser Content
```Java
{
Name = "ibm-guardium-cef-alert-trigger-success-failedlogin"
Vendor = "IBM"
Product = "Guardium"
TimeFormat = "epoch"
Conditions = [
"""|IBM|Guardium|10.18|"""
"""cs5Label=DB Name"""
]
Fields = [
"""({host}[\w\-\.]+)\s*CEF:"""
"""\Wdvc=({host}\S+)\s*(\w+=|$)"""
"""\Wdvchost=({host}\S+)\s*(\w+=|$)"""
"""\Wrt=({time}\d{13})"""
"""CEF.+?([^|]*\|){5}({alert_name}[^|]+)"""
"""\WeventId=({alert_id}\d+)"""
"""\Wshost=({src_host}\S+)\s*(\w+=|$)"""
"""\Wdhost=({dest_host}\S+)\s*(\w+=|$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wsuser=\"?(({domain}[^\s\\\"]+)\\+)?(\?|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\"?\s*(\w+=|$)"""
"""\Wduser=\"?(({domain}[^\s\\\"]+)\\+)?(\?|({db_user}[^\\\s\"]+))\"?\s*(\w+=|$)"""
"""\WdestinationServiceName =({service_name}.+?)\s*(\w+=|$)"""
"""\Wcs1=({alert_type}.+?)\s*(\w+=|$)"""
"""\Wcs2=({server_group}.+?)\s*(\w+=|$)"""
"""\Wcs5=(|({db_name}.+?))\s*(\w+=|$)"""
"""proto=({protocol}[^=]+?)\s*\w+="""
]
DupFields = [
"db_user->account"
]
ParserVersion = "v1.0.0"


}
```