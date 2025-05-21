#### Parser Content
```Java
{
Name = cisco-fp-kv-dns-response-success-dnsquery
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """AccessControlRuleAction: """, """ApplicationProtocol: DNS""", """DNSQuery: """ ]

cisco-firepower-template = {
  Vendor = Cisco
  Product = Cisco Network Security
  Fields = [
    """\Wrt=({time}\d{13})"""
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s*({host}[\w\-.]+)?\s*"""
    """\w+\s+\d+ \d\d:\d\d:\d\d ({host}[\w.\-]+)""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """({time}\w+ \d\d (\d\d\d\d )?\d\d:\d\d:\d\d)""",
    """AccessControlRuleName:\s*({rule}[^,]+),""",
    """ACPolicy:\s*({policy_name}[^,]+)""",
    """ApplicationProtocol:\s*({app_protocol}[^,]+),""",
    """Client:\s*({user_agent}[^,]+)"""
    """ConnectionID:\s*({connection_id}[^,]+)"""
    """ConnectionDuration:\s*({connection_duration}[^,]+)"""
    """DeviceUUID:\s*({device_id}[^\s,]+)"""
    """DstIP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F:]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """DstPort:\s*({dest_port}\d+)""",
    """EgressInterface:\s*({dest_interface}[^\s,]+?),""",
    """EgressZone:\s*({egress_zone}[^,]+)"""
    """FirstPacketSecond:\s*({time}\d+-\d+-\d+T\d+:\d+:\d+Z)"""
    """IngressInterface:\s*({src_interface}[^\s,]+?),""",
    """IngressZone:\s*({ingress_zone}[^,]+)""",
    """IntrusionPolicy:\s*({alert_name}[^,]+),""",
    """NAPPolicy:\s*({nap_policy}[^,"\n:]+)"""
    """Priority:\s*({priority}[^,]+),"""
    """\s+Protocol:\s*({protocol}[^,]+)"""
    """SrcIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """SrcPort:\s*({src_port}\d+)""",
    """User:\s*(Unknown|No Authentication Required|Not Found|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """AccessControlRuleAction:\s*({action}[^,]+)""",
    """WebApplication:\s*({web_application}[^,]+)""",
    """InitiatorPackets:\s*({initiator_packets}[^,]+)""",
    """ResponderPackets:\s*({responder_packets}\d+)""",
    """UserAgent:\s*({user_agent}.+?),\s+Client:""",
    """InitiatorBytes:\s*({bytes_out}\d+)""",
    """ResponderBytes:\s*({bytes_in}\d+)""",
    """URLCategory:\s*({categories}({category}[^,;]+)[^,]+)""",
    """URL:\s*({url}[^,\s"]+)""",
    """URL:\s*(?:-|\w+:\/+)({web_domain}[^\s\/:]+?)(,|$|:|"|\/|\\)""",
    """URL:\s*(?:-|\w+:\/+[^\/]+)({uri_path}\/[^?\s]+)""",
    """URL:\s*.*?({uri_query}\?[^\s"]+)""",
    """URI:\s*(?:-|\w+:\/+[^\/]+)({uri_path}\/[^?\s]+)""",
    """URI:\s*.*?({uri_query}\?[^\s",]+)""",
    """DNSQuery:\s*({dns_query}[^,]+)""",
    """DNSRecordType:\s*({dns_query_type}[^:,]+?),""",
    """DNSResponseType:\s*({dns_response}[^,]+)""",
    """AccessControlRuleReason:\s*({rule_reason}[^,]+)""",
    """FileDirection:\s*({operation}[^,:]+?),\s\w+:""",
    """FileAction:\s*({operation_details}[^,:]+?),\s\w+:""",
    """FileSHA256:\s*({hash_sha256}[^,:]+?),\s\w+:""",
    """SHA_Disposition:\s*(Unavailable|Unknown|({disposition}[^,:]+?)),\s\w+:""",
    """\sFileName:\s*({file_name}[^,]+?(\.({file_ext}[^\.,]+?))?),\s\w+:""",
    """FileType:\s*({file_type}[^,:]+?),\s\w+:""",
    """FileSize:\s*({bytes}\d+)""",
    """FilePolicy:\s*({policy_name}[^,:]+?),\s\w+:""",
    """FilePolicy:.*?URI:\s*({file_url}[^,]+),\s\w+:""",
    """%\w+\-\d+\-({event_code}\d+):\s\w+:"""
  
}
```