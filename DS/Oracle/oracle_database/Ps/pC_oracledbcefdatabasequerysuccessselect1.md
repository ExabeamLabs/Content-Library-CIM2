#### Parser Content
```Java
{
Name = "oracle-db-cef-database-query-success-select-1"
Vendor = "Oracle"
Product = "Oracle Database"
TimeFormat = "epoch"
Conditions = [
"""|ORACLE|"""
"""|SELECT|"""
"""DBID:"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\sdvchost=({host}[^\s]+)"""
"""\seventId=({event_code}\d+)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sdhost=({src_host}[^\s]+)"""
"""\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""\sduser=(\/|({account}.+?))\s+\w+="""
"""Oracle Audit.+?(OS$USERID|CLIENT USER):\[\d+\]\s*("|')({user}[\w\.\-\!\#\^\~]{1,40}\$?)("|')"""
"""Oracle Audit.+?\s(USERID|DATABASE USER):\[\d+\]\s*("|')({account}[^\\\/\s"']+)("|')"""
"""Oracle Audit.+?DBID:\[\d+\]\s*("|')(|({db_name}[^"']+))("|')"""
"""\|ORACLE\|ORACLESYSDBA\|([^\|]*\|){2}({db_operation}[^\|]+)"""
"""\|ORACLE\|Oracle\|([^\|]*\|){3}({db_operation}[^\|]+)"""
"""\smsg=\s*({db_query}([^\\=]|(\\\\)*\\=|\\)+?)\s+(\w+=|$)"""
]
DupFields = [
"host->dest_host"
"account->db_user"
]
ParserVersion = "v1.0.0"


}
```