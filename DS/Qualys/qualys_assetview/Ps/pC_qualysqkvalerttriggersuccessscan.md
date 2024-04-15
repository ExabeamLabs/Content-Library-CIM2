#### Parser Content
```Java
{
Name = "qualys-q-kv-alert-trigger-success-scan"
Vendor = "Qualys"
Product = "Qualys AssetView"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""", TAGS="""
""", SEVERITY="""
""" IP="""
"""SCAN"""
]
Fields = [
"""\sIP="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sOS="({os}[^"]+)"""
"""\sNETBIOS="({src_host}[^"]+)"""
"""\sSEVERITY=({alert_severity}\d+)"""
"""\sTAGS="({alert_name}[^",]+)"""
"""\sTAGS="({additional_info}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```