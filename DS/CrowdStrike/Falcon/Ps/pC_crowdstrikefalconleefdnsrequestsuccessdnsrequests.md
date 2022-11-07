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
    """"LogonType\\*"+:\\*"+({login_type}\d+)""",
    """"LogonDomain\\*"+:\\*"+({domain}[^"\\]+)""",
    """"ClientComputerName\\*"+:\\*"+(-|({dest_host}[^"\\,]+))"""
  ]
  ParserVersion = "v1.0.0"
},

{
Vendor = CrowdStrike
Product = Falcon
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
  """\WdevTime=({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)"""
  """\Wduser=(?!N\/A)({user}[^=@]+?)(@({domain}[^@]+?))?(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)"""
  """\WusrName =(?!N\/A)({user}[^=@]+?)(@({domain}[^@]+?))?(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)"""
  """\Wdomain=(?!N\/A)({domain}[^=]+?)(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)"""
  """\Wsrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\Wdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\WsrcPort=({src_port}\d+)"""
  """\WdstPort=({dest_port}\d+)"""
  """\Wcat=({category}[^\|]+?)\s*(\||\w+=|$|"+\s*$)"""
  """\Wproto=({protocol}[^\s]+?)\s*(\||\w+=|$|"+\s*$)"""
  """\WfileName =({file_name}.+?)\s*(\||\w+=|$|"+\s*$)"""
  """\Wresource=({src_host}.+?)\s*(\||\w+=|$|"+\s*$)"""
  """\Wsev=({alert_severity}.+?)\s*(\||\w+=|$|"+\s*$)"""
  """CrowdStrike\|([^|]+\|){2}({alert_name}[^|]+)"""
  """\Wurl=({additional_info}[^\|]+?)\s*(\||\w+=|$|"+\s*$)"""
  """\Wmd5=({hash_md5}[^\s]+?)\s*(\||\w+=|$|"+\s*$)"""
  """({app}FalconHost)"""
  """CrowdStrike\|([^|]+\|){2}({alert_name}[^|]+)"""
  """\WdnsRequestDomain=({dns_query}[^\s|"]+?)(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)"""
  """\WrequestType=({dns_query_type}[^="|]+?)(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)"""
]
DupFields = [
  "category->alert_type"
]
Name = crowdstrike-falcon-leef-dns-request-success-dnsrequests
Conditions = [
  """LEEF:"""
  """|CrowdStrike|FalconHost|"""
  """cat=DnsRequests"""
]
ParserVersion = "v1.0.0"
},

{
  Name = crowdstrike-falcon-leef-app-login-falconhost
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """LEEF:""", """|CrowdStrike|FalconHost|""", """cat=AuthActivityAuditEvent""" ]
  Fields = [
    """\WdevTime=({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
    """\WusrName =({user}[^=@]+?)(@({domain}[^@]+?))?(\s*\||\s+\w+=|\s*$|\s*")""",
    """\Wsrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\Wsuccess=({result}.+?)\s*(\||\w+=|$)""",
    """({app}FalconHost)""",
  ]
  DupFields = ["domain->email_domain"]
  ParserVersion = "v1.0.0"
},

{
  Name = crowdstrike-falcon-sk4-app-login-success-validateentitlement
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch_sec"
  Conditions = [ """"eventType":""", """"AuthActivityAuditEvent"""", """"OperationName":""", """"validateEntitlementsHmac"""" ]
  Fields = [
    """"eventCreationTime":\s*({time}\d{10})""",
    """"timestamp":"({time}\d{10})"""",
    """"UTCTimestamp":({time}\d{10})""",
    """"UserId":\s*"({email_address}[^"@]+@({email_domain}[^"@]+))"""",
    """"UserId":\s*"({user}[^"@]+)"""",
    """"UserIp":\s*"({src_ip}[^"]+)""",
    """"ServiceName":\s*"({app}[^"]+)""",
    """"Success":\s*({result}[^",]+)"""
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = crowdstrike-falcon-json-app-login-twofactorauthenticate
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch_sec"
  Conditions = [ """"event-name":""", """"audit-event"""", """"OperationName":"twoFactorAuthenticate"""" ]
  Fields = [
    """"eventCreationTime":\s*({time}\d{10})""",
    """"timestamp":"({time}\d{10})"""",
    """"UTCTimestamp":({time}\d{10})""",
    """"UserId":\s*"({email_address}[^"@]+@({email_domain}[^"@]+))"""",
    """"UserId":\s*"({user}[^"@]+)"""",
    """"UserIp":\s*"({src_ip}[^"]+)""",
    """"ServiceName":\s*"({app}[^"]+)""",
    """"Success":\s*({result}[^",]+)"""
	""""time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"OperationName":"({event_name}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"
},

${CrowdStrikeParsersTemplates.crowdstrike-auth-activity}{
  Name = crowdstrike-falcon-json-process-create-success-processroll
  Conditions = [ """"event_simpleName\":\"ProcessRollup2\"""", """"@timestamp"""" ]
  Fields = ${CrowdStrikeParsersTemplates.crowdstrike-auth-activity.Fields} [
         """"ImageFileName\\*":\\*"({process_path}[^"]+(\/|\\)({process_name}[^"\\]+))\\*"\S"""
  ]
  ParserVersion = "v1.0.0"
},

${CrowdStrikeParsersTemplates.crowdstrike-auth-activity}{
  Name = crowdstrike-falcon-json-process-create-success-syntheticprocessroll
  Conditions = [ """"event_simpleName\":\"SyntheticProcessRollup2\"""", """"@timestamp"""" ]
  Fields = ${CrowdStrikeParsersTemplates.crowdstrike-auth-activity.Fields} [
         """"ImageFileName\\*":\\*"({process_path}[^"]+(\/|\\)({process_name}[^"\\]+))\\*"\S"""
  ]
  ParserVersion = "v1.0.0"
}

${CrowdStrikeParsersTemplates.leef-crowdstrike-alert-t}{
  Name = crowdstrike-falcon-leef-network-traffic-success-networkaccesses
  ParserVersion = v1.0.0
  Product = Falcon
  Conditions = [ """LEEF:""", """|CrowdStrike|FalconHost|""", """cat=NetworkAccesses""" ]
  Fields = ${CrowdStrikeParsersTemplates.leef-crowdstrike-alert-t.Fields} [
    """CrowdStrike\|([^|]+\|){2}({alert_name}[^|]+)""",
    """\Wdst=({dest_ip}[a-fA-F:\d.]+)(\t|\s+\w+=|\s*\||\s*$|\s*"*\s*$)"""
  
}
```