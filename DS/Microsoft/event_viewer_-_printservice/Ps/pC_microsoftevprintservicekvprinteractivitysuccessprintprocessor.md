#### Parser Content
```Java
{
Name = "microsoft-evprintservice-kv-printer-activity-success-printprocessor"
Vendor = "Microsoft"
Product = "Event Viewer - PrintService"
TimeFormat = "MM/dd/yyyy HH:mm:ss"
Conditions = [
"""driver_name="""
"""print_processor="""
"""data_type="""
]
Fields = [
"""\ssubmitted_time="({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d)"""
"""\smachine="+\\*(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^"]+))\s*"+\s*\w+="""
"""\suser="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
"""\sstatus="([^,]+,)*({operation}[^"]+)""""
"""\sstatus="([^,],)*({operation}[^,]+),error"""
"""\sstatus="({additional_info}[^"]+)""""
"""({result}error)"""
"""\sprinter="({printer_name}[^"]+)""""
"""\sdocument="+\s*({object}.+?)\s*"+"""
"""\ssize_bytes=({bytes}\d+)"""
"""\spage_printed=({num_pages}\d+)"""
"""\stotal_pages=({num_pages}\d+)"""
"""[\[\(]+({access}Read-Only)[\]\)]+"""
]
ParserVersion = "v1.0.0"


}
```