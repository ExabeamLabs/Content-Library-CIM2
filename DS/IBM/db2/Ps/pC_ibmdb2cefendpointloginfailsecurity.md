#### Parser Content
```Java
{
Name = "ibm-db2-cef-endpoint-login-fail-security"
Vendor = "IBM"
Product = "DB2"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""CEF:"""
"""|Enterprise-IT-Security"""
"""|DB2_AU05|"""
"""|DB2Aud005_Login_Logout_Activity|"""
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
"""duser=({user}[\w\.\-]{1,40}\$?)\s*\w+="""
"""({event_code}DB2_AU05)"""
"""({event_name}DB2Aud005_Login_Logout_Activity)"""
]
ParserVersion = "v1.0.0"


}
```