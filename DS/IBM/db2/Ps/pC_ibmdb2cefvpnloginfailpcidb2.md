#### Parser Content
```Java
{
Name = "ibm-db2-cef-vpn-login-fail-pcidb2"
Vendor = "IBM"
Product = "DB2"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""CEF:"""
"""|Enterprise-IT-Security"""
"""|DB2_AU07|"""
"""|DB2Aud007_Authorization_Failure|"""
""" PCI_DB2 """
]
Fields = [
"""\s({time}\d+-\d+-\d+T\d+:\d+:\d+)\S*\s+({host}[\w\-.]+)\s+PCI_DB2"""
"""deviceProcessName =({host}[\w\-.]+)"""
"""act=({action}.+?)\s+(\w+=|$)"""
"""cat=({category}.+?)\s+(\w+=|$)"""
"""dproc=({object}.+?)\s+(\w+=|$)"""
"""cs2=({result}.+?)\s+(\w+=|$)"""
"""shost=({src_host}[\w\-.]+)\s+(\w+=|$)"""
"""deviceProcessName =({process_name}.+?)\s+(\w+=|$)"""
"""cs1=({additional_info}.+?)\s+(\w+=|$)"""
"""cn1=({failure_reason}[^:,]+?)(:[^=]*?)?\s+(\w+=|$)"""
"""cs3=({access}.+?)\s+(\w+=|$)"""
"""duser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*\w+="""
"""({event_code}DB2_AU07)"""
]
ParserVersion = "v1.0.0"


}
```