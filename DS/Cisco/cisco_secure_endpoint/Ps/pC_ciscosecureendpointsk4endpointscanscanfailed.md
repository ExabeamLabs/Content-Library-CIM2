#### Parser Content
```Java
{
Name = "cisco-secureendpoint-sk4-endpoint-scan-scanfailed"
  Conditions = [ 
    """"event_type""""
    """"Scan Failed""""
    """"trajectory":"""
  ]
  ParserVersion = "v1.0.0"

cisco-secureendpoint-sk4-alert = {
  Vendor = "Cisco"
  Product = "Cisco Secure Endpoint"
  TimeFormat = "epoch_sec"
  Fields = [
    """\Wact=(|({action}[^=]+?))(\s+\w+=|\s*$)"""
    """\Woutcome=(|({result}[^=]+?))(\s+\w+=|\s*$)"""
    """timestamp":\s*({time}\d{10})"""
    """"detection":"(|({alert_name}[^"]+?))""""
    """detection":\s*"({alert_name}[^"]+)"""
    """\Wsuser=((?i)(anonymous|system)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
    """\Wsuser=((?i)(anonymous|system)|({email_address}[^@\s]+?@[^@\s\.=]+?\.[^@\s\.=]+?)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@(NT AUTHORITY|({domain}[^@\s\.=]+?))))(\s+\w+=|\s*$)"""
    """user":\s*"((?i)(anonymous|system)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """user"+:\s*"+((?i)(anonymous|system)|({email_address}[^@]+@[^@"]+\.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@(NT AUTHORITY|({domain}[^"]+)))"""
    """hostname":\s*"({src_host}[^"]+)"""
    """file_path":\s*"(\\+\?\\+)?({file_path}[^"]+)"""
    """external_ip":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """"network_addresses":.+?"ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """"trajectory":\s*"({additional_info}[^"]+)"""
    """,\s*"disposition":\s*"(Unknown|({alert_severity}[^"\s]+))""""
    """,\s*"disposition":.+?file_name":\s*"({file_name}[^"]+)"""
    """"sha256":\s*"({hash_sha256}[^"]+)"""
    """"sha1":\s*"({hash_sha1}[^"]+)"""
    """"md5":\s*"({hash_md5}[^"]+)"""
    """,\s*"disposition":.+?md5":\s*"({hash_md5}[^"]+)"""
    """\sdestinationServiceName =({product_name}[^=]+?)(\s+\w+=|\s*$)"""
    """"ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """"mac":\s*"({src_mac}[^"]+)"""
    """"file_name":\s*"({file_name}[^"]+)"""
    """"event_type":\s*"({event_name}[^"]+)"""
    """"connector_guid":"({connector_guid}[^"]+)"""
    """"severity":\s*"({alert_severity}[^"]+)"""
    """event_type":\s*"({alert_type}[^"]+)"""
  ]
  DupFields = [ 
    "file_path->malware_url"
    "event_name->alert_type"
    "alert_type->category"
  
}
```