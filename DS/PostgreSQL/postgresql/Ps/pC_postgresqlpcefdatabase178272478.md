#### Parser Content
```Java
{
Name = "postgresql-p-cef-database-178272478"
Vendor = "PostgreSQL"
Product = "PostgreSQL"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""eventId="""
"""|PostgreSQL|PostgreSQL Audit|"""
]
Fields = [
"""\srt=({time}\d{13})\s*\w+="""
"""\scs2=(None|idle|idle\sin\stransaction|authentication|({db_query}.+?))\s*\w+="""
"""\scs3=(\[unknown\]|({db_user}.+?))\s*\w+="""
"""\scs4=((\[unknown\])|({db_name}.+?))\s*\w+="""
"""\scs6=\s*({additional_info}.+?)\s*\w+="""
"""\sshost=({src_host}.+?)\s*\w+="""
"""\sdvc=({host}[A-Fa-f:\d.]+)"""
"""\sdvchost=({host}[\w\-.]+)"""
"""CEF[^\|]+\|([^\|]*\|){4}({event_name}.+?)\s*\|"""
"""\sdtz=({dtz}.+?)\s*\w+="""
"""\sact=({action}.+?)\s*\w+="""
"""\seventId=({alert_id}.+?)\s*\w+="""
"""\ssuser=(N\/A|-|\[unknown\]|({user}[\w\.\-]{1,40}\$?))\s*\w+="""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*\w+="""
]
ParserVersion = "v1.0.0"


}
```