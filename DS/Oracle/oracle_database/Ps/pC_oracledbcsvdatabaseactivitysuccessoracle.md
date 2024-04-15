#### Parser Content
```Java
{
Name = "oracle-db-csv-database-activity-success-oracle"
Vendor = "Oracle"
Product = "Oracle Database"
TimeFormat = "dd-MMM-yyyy HH:mm:ss"
Conditions = [
"""[LNX]"""
""" Oracle """
"""CONNECT_DATA="""
]
Fields = [
"""({host}[\w.\-]+)\s+Oracle(\s+\S+){3}\s+({time}\d\d-\w+-\d\d\d\d \d\d:\d\d:\d\d)"""
"""\(USER=({user}[^\)]+?)\)"""
"""\(COMMAND=({command}[^\)]+?)\)"""
"""\(SERVICE=({service_name}[^\)]+?)\)"""
"""\(HOST=({dest_host}[^\)]+?)\)"""
"""\(PROTOCOL=({protocol}[^\)]+?)\)"""
"""\(PORT=({dest_port}\d+)\)"""
"""\(PROGRAM=({process_path}[^\)]+?)\)"""
]
ParserVersion = "v1.0.0"


}
```