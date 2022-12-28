#### Parser Content
```Java
{
Name = fireeye-etp-kv-email-receive-fenotify
  ParserVersion = v1.0.0  
  Vendor = FireEye
  Product = FireEye ETP
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
"""alert (id:"""
"""X-ETP-TRAFFIC-TYPE:"""
"""fenotify-"""
"""alert-url:"""
"""X-RECEIVED-IP:""" 
]
  Fields = [
    """appliance:\s*({host}[^\s]+)""",
    """occurred:\s*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """\salert\s*\(id:({alert_id}[^,]+),\s*name:({alert_type}[^\)]+)""",
    """severity:\s*({alert_severity}[^\s]+)""",
    """smtp-mail-from:\s*([^<]+<)?({email_address}[^@\s]+@[^\s>]+)""",
    """smtp-to:\s*({dest_email_address}[^@\s]+@[^\s,]+)""",
    """\saction:\s*({action}[^\s]+)""",
    """\ssubject:\s*({email_subject}.+?)\s+src:""",
    """\stype:\s*({category}[^\s]+)\s+stype:""",
    """X-ETP-TRAFFIC-TYPE:\s*({direction}[^\s]+)""",
    """X-RECEIVED-IP:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """X-Message-ID:\s*({message_id}[^\s]+)""",
    """last-malware:\s*({alert_name}[^:]+?)\s+protocol""",
    """\ssmtp-mail-from:.+?url:\s*({malware_url}.+?)\s+dst:""",
    """domain:\s*({domain}[^:]+?)\s+smtp-mail-from:""",
    """md5sum:\s({hash_md5}[^\s]+)""",
    """sha256:\s+({hash_sha256}[^\s]+)"""
  ]
  SOAR {
    IncidentType = "dlp"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_type->description", "dest_email_address->dlpUser", "alert_name->dlpPolicy", "alert_severity->sourceSeverity", "action->dlpActionTaken","host->dlpDeviceName"]
    NameTemplate = """FireEye DLP Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address"]

}
```