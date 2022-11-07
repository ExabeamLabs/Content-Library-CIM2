#### Parser Content
```Java
{
Name = cisco-ise-app-activity-fail-failedattempts
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco ISE
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [""" CISE_Failed_Attempts """]
  Fields = [
    """(::ffff:)?({host}\S+) ({event_name}CISE_Failed_Attempts)""",
    """User(-)?Name =(({domain}[^\\\/\s,;@]+)\\+)?(([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2}|({user}[^,;@\s\\\/]+))(;|,|\s)""",
    """User(-)?Name =({email_address}[^,;@\s]+@[^,;@\s]+)""",
    """AcsSessionID=({acs_session_id}[^,]+?),""",
    """AuthenticationMethod=({auth_method}[^,]+?),""",
    """Calling-Station-ID=(::ffff:)?(({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))""",
    """DestinationIPAddress=({dest_ip}[a-fA-F\d.:]+)""",
    """DestinationPort=({dest_port}\d+)""",
    """Device IP Address=(::ffff:)?({src_ip}[a-fA-F\d.:]+)""",
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
    """AD-User-Candidate-Identities=({email_address}[^,@\s]+@[^,@\s]+),""",
    """ISEPolicySetName =({policy_name}[^,]+),""",
  ]
  DupFields = [ "endpoint_mac_address->mac" ]


}
```