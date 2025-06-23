#### Parser Content
```Java
{
Name = "cyberark-pta-cef-alert-trigger-success-riskyactivities"
Vendor = "CyberArk"
Product = "CyberArk Privilege Access Manager"
TimeFormat = "epoch"
Conditions = [
"""CyberArk|PTA"""
"""suser="""
]
Fields = [
"""deviceCustomDate1=({time}\d{13})"""
"""\s({host}[^\s]+)\sCEF"""
"""shost=((None)|({src_host}[^\s]+))"""
"""src=((None)|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
"""dst=((None)|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""suser=((None)|({email_address}[^@\s]+@[^\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""dhost=((None)|({dest_host}[^\s]+))"""
"""duser=((None)|({additional_info}[^\s\(]+))"""
"""cs2=({alert_id}[^\s]+)"""
"""CEF[^|]+?\|[^|]+?\|({alert_type}[^\|]+)"""
"""CEF[^|]+?\|[^|]+?\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)"""
"""Cyber-Ark\|Vault\|[^\|]+\|({event_code}\d+)"""
]
ParserVersion = "v1.0.0"


}
```