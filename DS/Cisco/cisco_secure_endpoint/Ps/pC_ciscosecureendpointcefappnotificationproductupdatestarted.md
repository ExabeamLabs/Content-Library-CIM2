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
    """dpriv=({alert_name}[^=]+?)\s\w+=""",
    """"detection":\s*"(|({alert_name}[^"]+?))"""",
    """\Wsuser=((?i)(anonymous|system)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)""",
    """\Wsuser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|((?i)(anonymous|system)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))@(NT AUTHORITY|({domain}[^@\s\.=]+?)))(\s+\w+=|\s*$)""",
    """user":\s*"((?i)(anonymous|system)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """user"+:\s*"+(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|((?i)(anonymous|system)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))@(NT AUTHORITY|({domain}[^"]+)))"""",
    """hostname":\s*"({src_host}[^"]+)""",
    """file_path":\s*"(\\+\?\\+)?({file_path}[^"]+)""",
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

    """exa_json_path=$..timestamp,exa_field_name=time"""
    """exa_json_path=$.computer.hostname,exa_field_name=src_host"""
    """exa_json_path=$.computer.external_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.computer.network_addresses..ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.event_type,exa_field_name=event_name"""
    """exa_json_path=$.event_type,exa_field_name=alert_type"""
    """exa_json_path=$..computer.network_addresses[:1].Mac,exa_field_name=src_mac"""
    """exa_json_path=$.event.computer.network_addresses[:1].mac,exa_field_name=src_mac"""
    """exa_json_path=$.event.file.identity.sha256,exa_field_name=hash_sha256"""
    """exa_json_path=$.event.file.parent.identity.md5,exa_field_name=hash_md5"""
    """exa_json_path=$.connector_guid,exa_field_name=connector_guid"""
    """exa_json_path=$.event.connector_guid,exa_field_name=connector_guid"""
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.file.file_path,exa_field_name=file_path"""
    """exa_json_path=$.file.file_name,exa_field_name=file_name"""
    """exa_json_path=$.file.identity..sha256,exa_field_name=hash_sha256"""
    """exa_json_path=$.event.file.identity.sha256,exa_field_name=hash_sha256"""
    """exa_json_path=$.event.file.file_path,exa_field_name=file_path"""
  ]
  DupFields = [ "file_path->malware_file_name", "alert_type->category" 
}
```