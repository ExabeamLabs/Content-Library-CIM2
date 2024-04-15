#### Parser Content
```Java
{
Name = "ibm-guardium-cef-alert-trigger-success-unauthaccess"
Vendor = "IBM"
Product = "Guardium"
TimeFormat = "epoch"
Conditions = [
"""|IBM|Guardium|"""
"""cs3Label=Database Name"""
"""deviceSeverity="""
]
Fields = [
"""CEF:([^|]*\|){5}({alert_name}[^|]+)"""
"""CEF:([^|]*\|){6}({alert_severity}[^|]+)"""
"""\Wrt=({time}\d{13})"""
"""\Wdvc=({host}[A-Fa-f:\d.]+)"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""\Wsuser=({user}[^\s]+)"""
"""\Wcs3=(|({db_name}.+?))\s*(\w+=|$)"""
"""\Wcs2=({server_group}.+?)\s*(\w+=|$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wshost=(({domain}[^\\]+)\\+)?({src_host}[^\\\s]+)"""
"""\Wdhost=({dest_host}[\w\-.]+)"""
"""\WeventId=({alert_id}\d+)"""
"""\Wcn1=({response_size}\d+)"""
"""\WdeviceSeverity=({device_severity}\d+)"""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```