#### Parser Content
```Java
{
Name = proofpoint-tap-json-email-receive-emailthreat-1
Conditions = [
  """Proofpoint"""
  """"threatsInfoMap\":"""
  """"threatTime\":"""
  """"threat\":"""
  """"default_inbound\""""
]
ParserVersion = "v1.0.0"

s-proofpoint-email-in-1.Fields}[
    """"sha256"+:"+({hash_sha256}[^"]+)"+,"md5"+:"+({hash_md5}[^"]+)"+,\s*"filename":\s*"(?!text(\.txt|\.html|-calendar))""",
    """ Category \[({category}[^\]]+?)\]""",
    """"url":"\s*"([A-Fa-f\d]{64}|[^@]+@[^\.]+\.[^"]+|({malware_url}[^"]+))""",
    """"threat":\s*"([A-Fa-f\d]{64}|[^@]+@[^\.]+\.[^"]+|({malware_url}[^"]+))""",
    """"threat(Url|URL)":\s*"<?({threat_url}[^"]+?)"""",
    """(fromAddress|sender)":\s*\[?"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|0-9]+))([\\]+)?([\\]+)?"\]?""",
    """toAddresses":\s*\[({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]]*?)\]""",
     """\scs1=Policy \[id: [^\]]*? ; name: ({alert_subject}({alert_name}[^\]]+?)) ; category: ({category}[^\]]+?)]""",
    """:\sCategory\s\[[^\]]+\]\s,\sName\s\[({alert_subject}({alert_name}[^\]]+))\]""",
    """"fromArray":"({result}clicksBlocked|clicksPermitted|messagesBlocked|messagesDelivered)"""",
    """"threatStatus":"({status_msg}[^"]+)""",
    """,\s*"filename":\s*"(?!text(\.txt|\.html|-calendar))\s*({email_attachments}({file_name}({email_attachment}[^",;]+\.({file_ext}[^"]+)))[^"]*?)",\s*"\w+":""",
    """"recipient":\["({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"],""",
    """proto=({alert_subject}({alert_name}[^=]+))\s""",
    """msg=.*?\[({alert_source}[^\]]+)\]:""",
    """msg=.*?name:\s*({alert_source}[^\]]+)\]"""
    """"userAgent":"({user_agent}[^"]+)""""
    """"clickTime":"({log_time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
    """"clickIP":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """"completelyRewritten":\s*({alert_status}(?i)true|false)"""
    """eventType=({result}[^\s]+)"""
    """"classification":\s*"({alert_subject}({alert_name}[^"]+))""",
  
}
```