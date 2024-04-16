#### Parser Content
```Java
{
Name = "vmware-carbonblack-leef-alert-trigger-success-privilegeescalate"
Vendor = "VMware"
Product = "Carbon Black CES"
TimeFormat = "MMM-dd-yyyy HH:mm:ss z"
Conditions = [
"""LEEF:"""
"""|CarbonBlack|CbDefense|"""
"""threatIndicators="""
"""incidentId="""
]
Fields = [
"""devTime=({time}\w{1,3}-\d\d-\d\d\d\d\s\d\d:\d\d:\d\d\s\w{1,3})"""
"""deviceName =({host}[^\s]+)"""
"""userName =(None|({user}[\w\.\-]{1,40}\$?))\s+\w+="""
"""email=({email_address}[^@]+@[^\s]+)"""
"""\WcommandLine=(None|({process_command_line}[^\n]+?))\s+\w+="""
"""threatIndicators=({alert_name}[^=]+?)\s+\w+="""
"""sev=({alert_severity}\d+)"""
"""eventType=({alert_type}[^=]+?)\s+\w+="""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```