#### Parser Content
```Java
{
Name = "hp-printserver-cef-printer-activity-success-printserver"
Vendor = "HP"
Product = "HP Print Server"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|HP|Print Server|"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sshost=({src_host}.+?)\s+(\w+=|$)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+(\w+=|$)"""
"""\ssntdom=({domain}.+?)\s+(\w+=|$)"""
"""\ssuser=({user}[\w\.\-]{1,40}\$?)\s+(\w+=|$)"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+(\w+=|$)"""
"""\ssuid=({full_name}.+?)\s+(\w+=|$)"""
"""\sfname=({object}.+?)\s+(\w+=|$)"""
"""\scs1=({printer_name}.+?)\s+(\w+=|$)"""
"""\scs2=({printer_id}.+?)\s+(\w+=|$)"""
"""\scs3=({dest_host}.+?)\s+(\w+=|$)"""
"""\scn1=({num_pages}\d+)"""
"""\sdvc=({host}.+?)\s+(\w+=|$)"""
"""\sdvchost=({host}.+?)\s+(\w+=|$)"""
"""CEF:([^\|]*\|){5}({operation}[^\|]+)\|"""
]
ParserVersion = "v1.0.0"


}
```