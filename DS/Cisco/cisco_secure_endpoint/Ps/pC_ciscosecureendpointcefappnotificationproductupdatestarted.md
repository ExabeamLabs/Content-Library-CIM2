#### Parser Content
```Java
{
Name = cisco-secureendpoint-cef-app-notification-productupdatestarted
  ParserVersion = v1.0.0
  Conditions = [ """"event_type"""", """"Product Update Started""", """"trajectory":""", """"timestamp_nanoseconds":""" ]

s-cisco-amp-alert = {
  Vendor = Cisco
  Product = Cisco Secure Endpoint
  ExtractionType = json
  TimeFormat = "epoch_sec"
  Fields = [
    """\Wact=(|({action}[^=]+?))(\s+\w+=|\s*$)""",
    """\Woutcome=(|({result}[^=]+?))(\s+\w+=|\s*$)""",
    """"timestamp":\s*({time}\d{10})""",
    """event_type":\s*"({alert_name}[^"]+)"""
    """dpriv=({alert_name}[^=]+?)\s\w+=""",
    """"detection":\s*"(|({alert_name}[^"]+?))"""",
    """\Wsuser=((anonymous|system)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)""",
    """\Wsuser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|((anonymous|system)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))@(NT AUTHORITY|({domain}[^@\s\.=]+?)))(\s+\w+=|\s*$)""",
    """user":\s*"((anonymous|system)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """user"+:\s*"+(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|((anonymous|system)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))@(NT AUTHORITY|({domain}[^"]+)))"""",
    """hostname":\s*"({src_host}[^"]+)""",
    """file_path":\s*"(\\+\?\\+)?({file_path}[^"]+)""",
    """file_path":\s*"(\\+\?\\+)?({malware_file_name}[^"]+)""",
    """external_ip":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"network_addresses":.+?"ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"trajectory":\s*"({additional_info}[^"]+)""",
    """,\s*"disposition":\s*"(Unknown|({alert_severity}[^"\s]+))"""",
    """CEF:([^\|]*\|){6}({alert_severity}[^\|]+)\|""",
    """,\s*"disposition":.+?file_name":\s*"({file_name}[^"]+)""",
    """"sha256":\s*"({hash_sha256}[^"]+)""",
    """"sha1":\s*"({hash_sha1}[^"]+)""",
    """"md5":\s*"({hash_md5}[^"]+)""",
    """,\s*"disposition":.+?md5":\s*"({hash_md5}[^"]+)""",
    """\sdestinationServiceName =({product_name}[^=]+?)(\s+\w+=|\s*$)""",
    """"ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"mac":\s*"({src_mac}[^"]+)""",
    """"file_name":\s*"({file_name}[^"]+)""",
    """\s*"disposition":[^\{]+?file_name":\s*"({file_name}[^"]+)""",
    """"event_type":\s*"({event_name}[^"]+)""",
    """"connector_guid":"({connector_guid}[^"]+)""",
    """"severity":\s*"({alert_severity}[^"]+)""",
    """event_type":\s*"({alert_type}[^"]+)"""
    """event_type":\s*"({category}[^"]+)"""

    """exa_json_path=$..timestamp,exa_field_name=time"""
    """exa_json_path=$.computer.hostname,exa_field_name=src_host"""
    """exa_json_path=$.computer.external_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.computer.network_addresses..ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.event_type,exa_field_name=event_name"""
    """exa_json_path=$.event_type,exa_field_name=alert_type"""
    """exa_json_path=$.event_type,exa_field_name=category"""
    """exa_regex=event_type":\s*"({category}[^"]+)"""
    """exa_json_path=$..computer.network_addresses[:1].Mac,exa_field_name=src_mac"""
    """exa_json_path=$.event.computer.network_addresses[:1].mac,exa_field_name=src_mac"""
    """exa_json_path=$.event.file.identity.sha256,exa_field_name=hash_sha256"""
    """exa_json_path=$.event.file.parent.identity.md5,exa_field_name=hash_md5"""
    """exa_json_path=$.connector_guid,exa_field_name=connector_guid"""
    """exa_json_path=$.event.connector_guid,exa_field_name=connector_guid"""
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.file.file_path,exa_field_name=file_path"""
    """exa_json_path=$.file.file_path,exa_field_name=malware_file_name"""
    """exa_json_path=$.file.file_name,exa_field_name=file_name"""
    """exa_json_path=$.file.identity..sha256,exa_field_name=hash_sha256"""
    """exa_json_path=$.event.file.identity.sha256,exa_field_name=hash_sha256"""
    """exa_json_path=$.event.file.file_path,exa_field_name=file_path"""
    """exa_json_path=$.event.file.file_path,exa_field_name=malware_file_name"""
  s-cisco-amp-alert = {
  Vendor = Cisco
  Product = Cisco Secure Endpoint
  ExtractionType = json
  TimeFormat = "epoch_sec"
  Fields = [
    """\Wact=(|({action}[^=]+?))(\s+\w+=|\s*$)""",
    """\Woutcome=(|({result}[^=]+?))(\s+\w+=|\s*$)""",
    """"timestamp":\s*({time}\d{10})""",
    """event_type":\s*"({alert_name}[^"]+)"""
    """dpriv=({alert_name}[^=]+?)\s\w+=""",
    """"detection":\s*"(|({alert_name}[^"]+?))"""",
    """\Wsuser=((anonymous|system)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)""",
    """\Wsuser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|((anonymous|system)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))@(NT AUTHORITY|({domain}[^@\s\.=]+?)))(\s+\w+=|\s*$)""",
    """user":\s*"((anonymous|system)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """user"+:\s*"+(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|((anonymous|system)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))@(NT AUTHORITY|({domain}[^"]+)))"""",
    """hostname":\s*"({src_host}[^"]+)""",
    """file_path":\s*"(\\+\?\\+)?({file_path}[^"]+)""",
    """file_path":\s*"(\\+\?\\+)?({malware_file_name}[^"]+)""",
    """external_ip":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"network_addresses":.+?"ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"trajectory":\s*"({additional_info}[^"]+)""",
    """,\s*"disposition":\s*"(Unknown|({alert_severity}[^"\s]+))"""",
    """CEF:([^\|]*\|){6}({alert_severity}[^\|]+)\|""",
    """,\s*"disposition":.+?file_name":\s*"({file_name}[^"]+)""",
    """"sha256":\s*"({hash_sha256}[^"]+)""",
    """"sha1":\s*"({hash_sha1}[^"]+)""",
    """"md5":\s*"({hash_md5}[^"]+)""",
    """,\s*"disposition":.+?md5":\s*"({hash_md5}[^"]+)""",
    """\sdestinationServiceName=({product_name}[^=]+?)(\s+\w+=|\s*$)""",
    """"ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"mac":\s*"({src_mac}[^"]+)""",
    """"file_name":\s*"({file_name}[^"]+)""",
    """\s*"disposition":[^\{]+?file_name":\s*"({file_name}[^"]+)""",
    """"event_type":\s*"({event_name}[^"]+)""",
    """"connector_guid":"({connector_guid}[^"]+)""",
    """"severity":\s*"({alert_severity}[^"]+)""",
    """event_type":\s*"({alert_type}[^"]+)"""
    """event_type":\s*"({category}[^"]+)"""

    """exa_json_path=$..timestamp,exa_field_name=time"""
    """exa_json_path=$.computer.hostname,exa_field_name=src_host"""
    """exa_json_path=$.computer.external_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.computer.network_addresses..ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.event_type,exa_field_name=event_name"""
    """exa_json_path=$.event_type,exa_field_name=alert_type"""
    """exa_json_path=$.event_type,exa_field_name=category"""
    """exa_regex=event_type":\s*"({category}[^"]+)"""
    """exa_json_path=$..computer.network_addresses[:1].Mac,exa_field_name=src_mac"""
    """exa_json_path=$.event.computer.network_addresses[:1].mac,exa_field_name=src_mac"""
    """exa_json_path=$.event.file.identity.sha256,exa_field_name=hash_sha256"""
    """exa_json_path=$.event.file.parent.identity.md5,exa_field_name=hash_md5"""
    """exa_json_path=$.connector_guid,exa_field_name=connector_guid"""
    """exa_json_path=$.event.connector_guid,exa_field_name=connector_guid"""
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.file.file_path,exa_field_name=file_path"""
    """exa_json_path=$.file.file_path,exa_field_name=malware_file_name"""
    """exa_json_path=$.file.file_name,exa_field_name=file_name"""
    """exa_json_path=$.file.identity..sha256,exa_field_name=hash_sha256"""
    """exa_json_path=$.event.file.identity.sha256,exa_field_name=hash_sha256"""
    """exa_json_path=$.event.file.file_path,exa_field_name=file_path"""
    """exa_json_path=$.event.file.file_path,exa_field_name=malware_file_name"""
  ]
},
cisco-events-2 = {
  Vendor = Cisco
  Product = Cisco
  TimeFormat = "MMM dd yyyy hh:mm:ss a"
  Fields = [
    """\s({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+\s+(AM|PM|am|pm))""",
    """UserID\s*=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """ClientAddress\s*=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """EventType\s*=({operation}[^\]]+)""",
    """ResourceAccessed\s*=({object}[^\]]+)""",
    """EventStatus\s*=({result}[^\]]+)""",
    """ComponentID\s*=({target}[^\]]+)""",
    """AuditDetails\s*=({additional_info}[^\]]+)""",
    """App ID\s*=({app}[^\]]+)""",
    """userPrincipalName"+:\s*"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
  ]
},
cisco-system-info-aa = {
  Vendor = "Cisco"
  Product = Cisco Network Infrastructure and Management
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","MMM dd yyyy HH:mm:ss.SS","yyyy MMM dd HH:mm:ss","MMM dd yyyy HH:mm:ss.SSS","epoch_sec","epoch", "MMM dd HH:mm:ss", "MMM dd HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy MMM dd HH:mm:ss.SSSSSS"]
  Fields = [
    """(\d+:\s*({host}[\w\-\.]+)\s*(:\s*\d+)?:\s*)?\w+\s\d+\s(\d\d\d\d\s)?\d\d:\d\d:\d\d(\.\d+)?(\s\w+)?:\s*%"""
    """\w+\s\d+\s\d\d:\d\d:\d\d\s({host}[\w\-\.]+)\s"""
    """\s({time}\w+ \d+(\s*\d+)? \d+:\d+:\d+(\.\d+)?)"""
    """({time}\d+ \w+ \d+ \d+:\d+:\d+(\.\d+)?)\s+\w+:\s+\%""",
    """\Wrt=({time}\d{13})""",
    """({event_code}%\w+\-[^:\s]+):""",
    """\%[\w+-.]+:\s*({additional_info}[^\$]+?)\s*$"""
  ]
},

cef-cisco-dns-response-sk4-template {
  Vendor = Cisco
  Product = Cisco Cloud Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """"ResponseCode_s":"({dns_response_code}[^"]+)"""
    """"Domain_s":"({dns_query}[^"]+)"""
    """"domain":"({dns_query}[^"]+)"""
    """"Action_s":"({result}[^"]+)"""
    """"QueryType_s":"({dns_query_type}[^"]+)"""
    """"Categories_s":"({categories}[^"]+)"""
    """"InternalIP_s":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """"Identites_s":"([\w\s\.]+,)?(({full_name}\w+\s+\w+[^",]+?) \(({email_address}[^\)@]+?@[^\)]+?)\))?(,({dest_host}[^\(\)"\s]+))?"""
  ]
}

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
  ]
}

}
}
```