#### Parser Content
```Java
{
Name = "zeek-z-json-file-read-success-txhosts"
Product = "Zeek"
Conditions = [
"""fuid":"""
""""tx_hosts":"""
""""rx_hosts":"""
]
ParserVersion = "v1.0.0"

json-bro-activity.Fields}[
    """"helo":\s*"({helo}[^"]+)""",
    """"mailfrom":\s*\"({user}[\w\.\-]{1,40}\$?)@({domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""""
    """rcptto":\[({email_recipients}"({dest_email_address}[^",@]+@({exter_domain_recipient}[^"@,]+))".*?)\]""",
    """"subject":\s*"({email_subject}[^"]+)""",
    """"user_agent":\s*"({user_agent}[^"]+)"""
  
}
```