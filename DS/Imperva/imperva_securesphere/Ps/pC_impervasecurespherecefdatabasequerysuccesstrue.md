#### Parser Content
```Java
{
Name = "imperva-securesphere-cef-database-query-success-true"
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "epoch"
Conditions = [
"""|Imperva|SecureSphere DAM|"""
"""cs5=Query"""
"""outcome=True"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\sdvchost=({host}[^\s]+)"""
"""\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""\scs4=(?: |({app}.+?))\s+\w+="""
"""\scs3=(?: |({service_name}.+?))\s+\w+="""
"""\scs2=(?: |({server_group}.+?))\s+\w+="""
"""\sflexString1=(?: |({db_name}.+?))\s+\w+="""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sflexString2=(?: |({db_operation}.+?))\s+\w+="""
"""\scn2=({response_size}\d+)"""
"""\sshost=({src_host}[^\s]+)"""
"""\sdhost=({dest_host}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```