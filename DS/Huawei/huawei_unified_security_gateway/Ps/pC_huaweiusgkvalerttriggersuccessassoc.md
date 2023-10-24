#### Parser Content
```Java
{
Name = "huawei-usg-kv-alert-trigger-success-assoc"
Vendor = "Huawei"
Product = "Huawei Unified Security Gateway"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
"""SignName ="""
"""SignId="""
"""Os="""
"""ASSOC/"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\d\s*\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s({host}[^\s]+)\s*%"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d),\S+\s+({host}[\w\.\-]+)"""
"""SrcPort=({src_port}\d+)"""
"""SrcIp=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""DstPort=({dest_port}\d+)"""
"""DstIp=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""Protocol=({protocol}[^,]+)"""
"""Application="({app}[^"]+)"""
"""SignName ="({alert_name}[^"]+)"""
"""Severity=({alert_severity}[^,]+)"""
"""Category=({alert_type}[^,]+)"""
"""Policy="({policy_name}[^"]+)"""
"""User="(?!\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(?:unknown|({email_address}[^@"]+@[^@"]+)|({user}[\w\.\-]{1,40}\$?))""""
]
ParserVersion = "v1.0.0"


}
```