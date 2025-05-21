#### Parser Content
```Java
{
Name = "proofpoint-pep-kv-smtp-start-session"
  ParserVersion = "v1.0.0"
  Conditions = [ """mod=session""","""cmd=connect""" ]
 
proofpoint-dlp-log = {
  Vendor = Proofpoint
  Product = Proofpoint Enterprise Protection
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss"]
  Fields = [
    """"+host"+:"+({host}[^"]+)""",
    """({time}\w+ \d+ \d+:\d+:\d+)(\s+({host}[\w\-.]+)\s+)?"""
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """Original Address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sx=({xid}[^\s]+)\s""",
# mode is removed
    """cmd=(?:\s|({command}[^\s]+))\s""",
# module is removed
    """rule=(?:\s|({rule}[^\s"]+))""",
    """action=(?:\s|({action}[^\s"]+))""",
    """policy=(?:\s|({policy_name}[^\s]+))""",
    """file=(?:\s|({file_name}[^\s]+))""",
    """size=(?:\s|({bytes}\d+))\s""",
    """sha256=(?:\s|({hash_md5}[^\s]+))\s""",
    """value=(?:\s|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s""",
    """prot=(?:\s|({protocol}[^:\s]+))""",
    """\sscore=({original_risk_score}[\d.]+)\s""",
    """spamscore=({spam_score}[\d]+)\s""",
    """phishscore=({phishing_score}[\d]+)\s""",
    """malwarescore=({malware_score}[\d]+)\s""",
    """value=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s+(\w+=|$)""",
    """from=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))("+|\s+\w+=)""",
  ]
  DupFields = [ "xid->alert_id"
}
```