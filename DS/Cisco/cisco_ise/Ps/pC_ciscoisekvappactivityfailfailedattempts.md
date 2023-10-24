#### Parser Content
```Java
{
Name = cisco-ise-kv-app-activity-fail-failedattempts
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco ISE
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [""" CISE_Failed_Attempts """]
  Fields = [
    """(::ffff:)?({host}\S+) ({event_name}CISE_Failed_Attempts)""",
    """User(-)?Name =(({domain}[^\\,]+)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))>?,"""
    """AcsSessionID=({acs_session_id}[^,]+?),""",
    """AuthenticationMethod=({auth_method}[^,]+?),""",
    """Calling-Station-ID=(::ffff:)?(({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """DestinationIPAddress=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """DestinationPort=({dest_port}\d+)""",
    """Device IP Address=(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
# device_port is removed
    """Device Type=({device_type}[^,]+?),""",
# endpoint_mac_address is removed
    """FailureReason=({failure_reason}[^,]+?),""",
    """Location=({location}[^,]+?),""",
# nas_identifier is removed
    """NAS-IP-Address=(::ffff:)?({nas_ip_address}[a-fA-F\d.:]+)""",
# nas_port is removed
# nas_port_type is removed
# network_device_groups is removed
# network_device_name is removed
    """Protocol=({protocol}[^,]+?),""",
    """Response=({response}[^,]+?),""",
    """Service-Type=({service_type}[^,]+?),""",
# usertype is removed
    """Called-Station-ID=({dest_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})(:({ssid}[^,]+))?,""",
    """AllowedProtocolMatchedRule=({rule}[^,]+),""",
    """[\=,](({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))(?<!local)(?<!loc)(?<!prd)(?<!localdomain)|({user}[\w\.\-]{1,40}\$?)(?:@({domain}[^,"]+)))("|,)\s""",
    """ISEPolicySetName =({policy_name}[^,]+),""",
  ]
  DupFields = [ "endpoint_mac_address->mac" ]


}
```