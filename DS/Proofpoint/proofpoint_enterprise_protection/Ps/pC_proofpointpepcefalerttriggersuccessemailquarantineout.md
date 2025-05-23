#### Parser Content
```Java
{
Name = "proofpoint-pep-cef-alert-trigger-success-emailquarantineout"
Vendor = "Proofpoint"
Product = "Proofpoint Enterprise Protection"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|ProofPoint|"""
"""|Email Quarantine Out|"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdvchost=({host}.+?)\s*(\w+=|$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wshost=({src_host}.+?)\s*(\w+=|$)"""
"""\Wsuser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s*(\w+=|$)"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wdhost=({dest_host}.+?)\s*(\w+=|$)"""
"""\Wduser=({email_recipients}.+?)\s*(\w+=|$)"""
"""\Wduser=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
"""\Wcs1=({message_id}.+?)\s*(\w+=|$)"""
"""\WflexString2=({alert_name}.+?)\s*(\w+=|$)"""
"""({alert_type}Email Quarantine)"""
"""\WeventId=({alert_id}\d+)"""
]
DupFields = [
"dest_email_address->target"
]
ParserVersion = "v1.0.0"


}
```