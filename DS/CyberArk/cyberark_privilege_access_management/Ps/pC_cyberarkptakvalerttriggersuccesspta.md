#### Parser Content
```Java
{
Name = "cyberark-pta-kv-alert-trigger-success-pta"
Vendor = "CyberArk"
Product = "Cyberark Privilege Access Management"
TimeFormat = "epoch"
Conditions = [
"""app="cyberark:pta""""
"""deviceCustomDate1="""
]
Fields = [
"""deviceCustomDate1(":\s+"|=)({time}\d{13}).*?"?deviceCustomDate1Label(":"|=)DetectionDate"""
""""deviceCustomDate1Label(": "|=)DetectionDate".*?"deviceCustomDate1(":\s+"|=)({time}\d+)"""
"""\shost_masked="({host}[^",]+)"""
"""\sduser="?(?:None|({user}[^",]+))"""
"""\sdvc_masked="({host}[^",]+)"""
"""\shost_ip_masked="({host}[^",]+)"""
"""\shost_masked="({host}[^",]+)"""
"""\ssrc_masked="({host}[^",]+)"""
"""\sdst_masked="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sdhost="({dest_host}[^",]+)"""
"""\sshost="({src_host}[^",]+)"""
"""\ssrc_masked="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\scs3="({additional_info}[^",]+)"""
"""\scategory="({alert_name}[^",]+)"""
"""\scef_severity=({alert_severity}\w+)"""
"""\sseverity=({alert_severity}\w+)"""
"""\scef_signature=({alert_id}\d+)"""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```