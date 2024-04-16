#### Parser Content
```Java
{
Name = "microsoft-evprintservice-cef-printer-activity-success-307"
Vendor = "Microsoft"
Product = "Event Viewer - PrintService"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Microsoft-Windows-PrintService:307|"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sshost=({src_host}[^\s]+)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sduser=(({domain}[^\s]+?)\\+)?({user}[\w\.\-]{1,40}\$?)\s+(\w+=|$)"""
"""\ssuser=({user}[\w\.\-]{1,40}\$?)"""
"""\sfname=({object}.+?)\s*(\w+=|$)"""
"""ad.Key\[1\]=({object}.+?)\s*ad\.Key"""
"""\sfsize=({bytes}\d+)"""
"""ad.Key\[4\]=({printer_name}[^|]*?)\s*(:?$|ad\.Key)"""
"""\scs2=({printer_name}.+?)\s*(\w+=|$).*cs2Label=Printer Name"""
"""ad.Key\[5\]=({printer_id}[^|]*?)\s*(:?$|ad\.Key)"""
"""\scs3=({printer_name}.+?)\s*(\w+=|$).*cs3Label=Port"""
"""ad.Key\[7\]=({num_pages}\d+)"""
"""\scn1=({num_pages}\d+).*cn1Label=Pages Printed"""
"""\sdvchost=({host}[^\s]+)"""
"""\sdvc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sexternalId=({event_code}\d+)"""
"""({operation}PrintService:307)"""
"""\smsg=({operation}.+?)\s*\w+="""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```