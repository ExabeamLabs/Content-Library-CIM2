#### Parser Content
```Java
{
Name = "cisco-ise-kv-app-notification-profiler"
  Vendor = "Cisco"
  Product = "Cisco ISE"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [
    """ CISE_Profiler """
	]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+(::ffff:)?({host}[\w\-.]+)\s+CISE_"""
    """\s*({time}\w+ \d+ \d+:\d+:\d+)"""
    """\w+\s+\d+\s+\d+:\d+:\d+\s+\S+\s+CISE_.*?({time}\d+-\d+-\d+\s+\d+:\d+:\d+)"""
    """\s({event_name}CISE_\S+)\s"""
    """\WMatchedPolicyID=({policy_id}[^\\,]+)"""
    """\sDevice IP Address=(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """Framed-IP-Address=(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """,Device IP Address=(::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """EndpointIPAddress=(::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """Profiler:\s*({operation}[^\\,]+)"""
    """EndpointSourceEvent=({operation}[^,\\]+)"""
    """PeerName =CN=(::ffff:)?({src_host}[^\\,]+)"""
    """Subject=CN=(::ffff:)?({src_host}[^\\,]+)"""
    """\WNAS-Identifier=(::ffff:)?({src_host}[\w\-.]+)"""
    """\WAD-Host-DNS-Domain=({domain}[\w\-.]+)"""
    """\WFailureReason=(-|({failure_reason}[^\\,]+))"""
    """\WUser-Fetch-User-Name =({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})"""
    """,OriginalUserName =(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """CreationType=({operation}[^,\\]+)"""
    """op=({operation}[^,\\]+)"""
    """dhcp-client-identifier=({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})"""
    """host-name=(::ffff:)?({src_host}[^,\\]+)"""
    """(Original)?UserName =(({domain}[^\\,]+)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """EndpointMacAddress=({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})"""
    """\d+\s({event_code}\d+)\sINFO"""
    """EndpointIdentityGroup=({device_type}[^,\\]+),\s*"""
    """NACRadiusUserName =(({domain}[^\\,]+)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  ]
  ParserVersion = "v1.0.0"


}
```