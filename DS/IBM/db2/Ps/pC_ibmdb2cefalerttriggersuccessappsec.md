#### Parser Content
```Java
{
Name = "ibm-db2-cef-alert-trigger-success-appsec"
Vendor = "IBM"
Product = "DB2"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""CEF:"""
"""|Enterprise-IT-Security"""
"""|AppSec"""
""" PCI_DB2 """
]
Fields = [
"""\s({time}\d+-\d+-\d+T\d+:\d+:\d+)\S*\s+({host}[\w\-.]+)\s+PCI_DB2"""
"""deviceProcessName =({host}[\w\-.]+)"""
"""act=({alert_name}.+?)\s+(\w+=|$)"""
"""cat=({category}.+?)\s+(\w+=|$)"""
"""cs2=({action}.+?)\s+(\w+=|$)"""
"""shost=({dest_host}[\w\-.]+)\s+(\w+=|$)"""
"""deviceProcessName =({process_name}.+?)\s+(\w+=|$)"""
"""cs1=({additional_info}.+?)\s+(\w+=|$)"""
"""duser=({user}.+?)\s*\w+="""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```