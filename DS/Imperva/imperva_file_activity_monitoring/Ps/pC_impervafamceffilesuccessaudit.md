#### Parser Content
```Java
{
Name = "imperva-fam-cef-file-success-audit"
Vendor = "Imperva"
Product = "Imperva File Activity Monitoring"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""CEF"""
"""|SecureSphere|"""
"""|Audit.FAM|"""
]
Fields = [
"""\Wrt=({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wspt=({src_port}\d+)"""
"""\Wproto=({protocol}.+?)\s+(\w+=|$)"""
"""\Wduser=({account}.+?)\s+(\w+=|$)"""
"""\Wcs9=({result}.+?)\s+(\w+=|$)"""
"""\Wcs8=({access}.+?)\s+(\w+=|$)"""
"""\Wcs7=({file_path}.+?)\s+(\w+=|$)"""
"""\Wcs7=\\+({dest_host}[^\\]+)\\+({file_dir}([^\\]+\\)+?)({file_name}[^\\]+?(\.({file_ext}\w+))?)\s+(\w+=|$)"""
"""\Wcs6=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)"""
"""\Wcs5=({domain}.+?)\s+(\w+=|$)"""
"""\Wcs4=({event_code}.+?)\s+(\w+=|$)"""
"""\Wcs3=({service_name}.+?)\s+(\w+=|$)"""
"""\Wcs2=({server_group}.+?)\s+(\w+=|$)"""
"""\Wcs1=({policy_name}.+?)\s+(\w+=|$)"""
"""\Wcs12=(|({event_category}.+?))\s+(\w+=|$)"""
"""\Wcs11=(|({data_owner}.+?))\s+(\w+=|$)"""
"""\Wcs10=({access_type}.+?)\s+(\w+=|$)"""
"""\Wcat=({category}.+?)\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```