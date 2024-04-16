#### Parser Content
```Java
{
Name = "trendmicro-officescan-kv-alert-trigger-success-ccca"
Vendor = "Trend Micro"
Product = "OfficeScan"
TimeFormat = "M/dd/yyyy HH:mm:ss"
Conditions = [
"""TMCM:SLF_INCIDENT_EVT_CCCA"""
]
Fields = [
"""\sEvent time \(local\)="({time}\d+\/\d+\/\d\d\d\d \d\d:\d\d:\d\d)"""
"""\sTMCM server="({host}[^"]+)"""
"""\sSecurity agent ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sPolicy rule="({alert_name}[^"]+)"""
"""\sC&C risk level="({alert_severity}[^"]+)"""
"""\sC&C url="({malware_url}[^"]+)"""
"""\sC&C ip port="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sC&C channel="({protocol}[^"]+)"""
"""Process="({process_path}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```