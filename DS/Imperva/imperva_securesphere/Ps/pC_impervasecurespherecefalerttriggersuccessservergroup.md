#### Parser Content
```Java
{
Name = "imperva-securesphere-cef-alert-trigger-success-servergroup"
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = ["MMM dd yyyy HH:mm:ss","dd MMM yyyy HH:mm:ss"]
Conditions = [
"""|Imperva Inc.|SecureSphere"""
"""cat=Alert"""
"""=ServerGroup"""
"""Query"""
]
Fields = [
"""cs7=\s*\(({time}\d\d \w+ \d{4} \d\d:\d\d:\d\d)\)\s*cs7Label=EventTime"""
"""rt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
"""\d\d:\d\d:\d\d ({host}.+?) CEF:"""
"""\sduser="*(?:n\/a|(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-]{1,40}\$?))\"*\s*\w+="""
"""\scs4=(?: |({app}.+?))\s*\w+="""
"""\scs3=(?: |({service_name}.+?))\s*\w+="""
"""\scs2=(?: |({server_group}.+?))\s*\w+="""
"""\stable=(?: |({table_name}[^.,]+))"""
"""\ssrc=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
"""\sdst=\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\scs5=({alert_name}.+?) (from|by|\w+=)"""
"""\scs1=({alert_type}.+?)\s*\w+="""
"""alert_num=({alert_id}\d+)"""
"""([^\|]+\|){6}({alert_severity}[^|=]+)\|"""
"""spt=({src_port}\d+)"""
"""dpt=({dest_port}\d+)"""
]
ParserVersion = "v1.0.0"


}
```