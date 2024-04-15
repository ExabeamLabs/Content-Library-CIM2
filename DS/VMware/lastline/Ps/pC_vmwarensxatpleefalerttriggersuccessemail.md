#### Parser Content
```Java
{
Name = "vmware-nsxatp-leef-alert-trigger-success-email"
Vendor = "VMware"
Product = "Lastline"
TimeFormat = "MMM dd yyyy HH:mm:ss z"
Conditions = [
"""LEEF:"""
"""|Lastline|Enterprise|"""
"""deviceExternalId="""
"""devTime="""
"""|email-"""
]
Fields = [
"""\s({host}[\w\-.]+)\s+LEEF:"""
"""LEEF:([^\|]*\|){4}({alert_type}[^\|]+)"""
"""devTime=({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+\s+\w+)"""
"""desc=({alert_name}.+?)\s+(\w+=|$)"""
"""sev=({alert_severity}.+?)\s+(\w+=|$)"""
"""emailSubject=\s*({alert_subject}.+?)\s+(\w+=|$)"""
"""(sender|Sender)=({src_email_address}.+?)\s+(\w+=|$)"""
"""fname=({file_name}.+?)\s+(\w+=|$)"""
"""EventDetailLink=({additional_info}.+?)\s+(\w+=|$)"""
"""(mailUrlHash|fileHash)=({hash_md5}.+?)\s+(\w+=|$)"""
"""usrName =({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
"""\Wcat=({operation}.+?)\s+(\w+=|$)"""
]
DupFields = [
"email_address->dest_email_address"
"host->dest_host"
"src_email_address->target"
]
ParserVersion = "v1.0.0"


}
```