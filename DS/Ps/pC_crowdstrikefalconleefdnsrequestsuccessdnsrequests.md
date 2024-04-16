#### Parser Content
```Java
{
Name = crowdstrike-falcon-leef-dns-request-success-dnsrequests
Conditions = [
  """LEEF:"""
  """|CrowdStrike|FalconHost|"""
  """cat=DnsRequests"""
]
ParserVersion = "v1.0.0"

crowdstrike-auth-activity.Fields} [
  """"event_simpleName\\*"+:\\*"+({event_code}[^"\\]+)""",
  
  
}
```