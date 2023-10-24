#### Parser Content
```Java
{
Name = "ibm-db2-cef-alert-trigger-success-securitysystemattack"
Vendor = "IBM"
Product = "DB2"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""CEF:"""
"""|Enterprise-IT-Security"""
"""Security_System_Attack"""
]
Fields = [
"""\s({time}\d+-\d+-\d+T\d+:\d+:\d+)\S*\s+({host}[\w\-.]+)\s+\w+\s"""
"""deviceProcessName =({host}[\w\-.]+)"""
"""act=({alert_name}.+?)\s+(\w+=|$)"""
"""cat=({category}.+?)\s+(\w+=|$)"""
"""cs2=({result}.+?)\s+(\w+=|$)"""
"""shost=({dest_host}[\w\-.]+)\s+(\w+=|$)"""
"""deviceProcessName =({process_name}.+?)\s+(\w+=|$)"""
"""cs1=({additional_info}.+?)\s+(\w+=|$)"""
"""duser=({user}[\w\.\-]{1,40}\$?)\s*\w+="""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```