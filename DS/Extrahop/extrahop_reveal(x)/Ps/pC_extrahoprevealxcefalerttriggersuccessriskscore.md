#### Parser Content
```Java
{
Name = "extrahop-revealx-cef-alert-trigger-success-riskscore"
Vendor = "Extrahop"
Product = "Extrahop Reveal(x)"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""CEF:"""
"""ExtraHop|Reveal(x)"""
"""Label=riskScore"""
"""Label=category"""
]
Fields = [
"""\Wrt=({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)"""
"""({host}[\w.-]+)\s+CEF:"""
"""cs1=({additional_info}[^=]+)\s\w+="""
"""cs2=({event_name}[^=]+)\s\w+="""
"""CEF:\d+\|([^\|]+\|){4}({alert_name}[^\|]+)"""
"""cn1=({alert_id}\d+)\s+cn1Label=detectionID"""
"""cn2=({alert_id}\d+)\s+cn2Label=detectionID"""
"""cn2=({original_risk_score}\d+)\s+cn2Label=riskScore"""
"""cn1=({original_risk_score}\d+)\s+cn1Label=riskScore"""
"""dst=(({dest_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""CEF:\d+\|([^\|]+\|){3}({alert_type}\d+)"""
"""src=(({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
"""sent\s*({bytes_out}[\d.]+)"""
"""received\s*({bytes_in}[\d.]+)"""
"""msg=({additional_info}[^\n]+)"""
"""cs2=({alert_type}[^=]+?)\s+cs2Label=category"""
"""suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""shost=({src_host}[^=\s]+)\s+\w+="""
"""dhost=({dest_host}[^=\s]+)\s+\w+="""
]
DupFields = [
"original_risk_score->alert_severity"
]
ParserVersion = "v1.0.0"


}
```