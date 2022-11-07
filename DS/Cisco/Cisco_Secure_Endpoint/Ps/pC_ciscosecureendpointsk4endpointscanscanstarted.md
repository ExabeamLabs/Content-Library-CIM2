#### Parser Content
```Java
{
Name = cisco-secureendpoint-sk4-endpoint-scan-scanstarted
  ParserVersion = v1.0.0
  Product = Cisco Secure Endpoint
  Conditions = [ """"event_type"""", """"Scan Started""", """"trajectory":""", """"timestamp_nanoseconds":""" ]

s-cisco-amp-alert = {
  Vendor = Cisco
  Product = Cisco Secure Endpoint
  TimeFormat = "epoch_sec"
  Fields = [
    """\Wact=(|({action}[^=]+?))(\s+\w+=|\s*$)""",
    """\Wdproc=(|({process_name}[^=]+?))(\s+\w+=|\s*$)""",
    """\Woutcome=(|({action}[^=]+?))(\s+\w+=|\s*$)""",
    """timestamp":\s*({time}\d+)""",
    """"detection":"(|({alert_name}[^"]+?))"""",
    """detection":\s*"({alert_name}[^"]+)""",
    """\Wsuser=((?i)(anonymous|system)|({user}[^\\\s@]+?))(\s+\w+=|\s*$)""",
    """\Wsuser=((?i)(anonymous|system)|({email_address}[^@\s]+?@[^@\s\.=]+?\.[^@\s\.=]+?)|({user}[^@\s=]+?@(NT AUTHORITY|({domain}[^@\s\.=]+?))))(\s+\w+=|\s*$)""",
    """user":\s*"((?i)(anonymous|system)|({user}[^"@\s]+))"""",
    """user"+:\s*"+((?i)(anonymous|system)|({email_address}[^@]+@[^@"]+\.[^"]+)|({user}[^@]+)@(NT AUTHORITY|({domain}[^"]+)))""",
    """hostname":\s*"({src_host}[^"]+)""",
    """file_path":\s*"(\\+\?\\+)?({file_path}[^"]+)""",
    """external_ip":\s*"({dest_ip}[^"]+)""",
    """"network_addresses":.+?"ip":\s*"({src_ip}[^"]+)""",
    """"trajectory":\s*"({additional_info}[^"]+)""",
    """,\s*"disposition":\s*"(Unknown|({alert_severity}[^"\s]+))"""",
    """,\s*"disposition":.+?file_name":\s*"({file_name}[^"]+)""",
    """"sha256":\s*"({hash_sha256}[^"]+)""",
    """"sha1":\s*"({hash_sha1}[^"]+)""",
    """"md5":\s*"({hash_md5}[^"]+)""",
    """,\s*"disposition":.+?md5":\s*"({hash_md5}[^"]+)""",
    """\sdestinationServiceName =({product_name}[^=]+?)(\s+\w+=|\s*$)""",
    """"ip":\s*"({src_ip}[a-fA-F\d.:]+)""",
    """src=({src_ip}[\da-fA-F.:]+)""",
    """"mac":\s*"({src_mac}[^"]+)""",
    """"file_name":\s*"({file_name}[^"]+)""",
    """"event_type":\s*"({event_name}[^"]+)""",
    """"connector_guid":"({connector_guid}[^"]+)""",
    """"severity":\s*"({alert_severity}[^"]+)""",
    """event_type":\s*"({alert_type}[^"]+)"""
  ]
  DupFields = [ "file_path->malware_url", "event_name->alert_type", "alert_type->category" 
}
```