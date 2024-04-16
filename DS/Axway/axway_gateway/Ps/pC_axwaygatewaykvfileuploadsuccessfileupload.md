#### Parser Content
```Java
{
Name = "axway-gateway-kv-file-upload-success-fileupload"
Vendor = "Axway"
Product = "Axway Gateway"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""TransferStatus.Id:"""
"""message=Transfer start logged"""
"""user="""
"""Client Hostname="""
"""Transferred File="""
]
Fields = [
"""\d\d:\d\d:\d\d\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""Transferred File=({file_name}[^\=]+\.({file_ext}\w+)),"""
"""user=({user}[\w\.\-]{1,40}\$?)"""
"""Client Hostname=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""message=({event_name}[^\.]+)"""
]
DupFields = [ "file_name->src_file_name" , "file_ext->src_file_ext" ]
ParserVersion = "v1.0.0"


}
```