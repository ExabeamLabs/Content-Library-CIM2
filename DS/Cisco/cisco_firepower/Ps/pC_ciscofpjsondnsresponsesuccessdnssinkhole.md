#### Parser Content
```Java
{
Name = "cisco-fp-json-dns-response-success-dnssinkhole"
Vendor = "Cisco"
Product = "Cisco Firepower"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""DNSSICategory: """
"""DNS_Sinkhole: """
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
"""\sAccessControlRuleReason:\s({result}[^,]+)"""
"""\sSrcIP:\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sDstIP:\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sSrcPort:\s({src_port}\d+)"""
"""\sDstPort:\s({dest_port}\d+)"""
"""\sProtocol:\s({protocol}[^,]+)"""
"""\sIngressInterface:\s*({ingress_interface}[^,]+)"""
"""\sEgressInterface:\s*({egress_interface}[^,]+)"""
"""\sUser:\s*(Unknown|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""InitiatorBytes:\s*({bytes_out}\d+)"""
"""ResponderBytes:\s*({bytes_in}\d+)"""
"""\sDNSQuery:\s*({dns_query}[^,]+)"""
"""\sDNSRecordType:\s*({dns_query_type}[^,]+)"""
"""\sDNSSICategory:\s({alert_type}[^\s]+)"""
]
DupFields = [
"alert_type -> alert_name"
]
ParserVersion = "v1.0.0"


}
```