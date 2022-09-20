#### Parser Content
```Java
{
Name = cisco-ise-kv-endpoint-authentication-cisepassed
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco ISE
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ CISE_Passed_Authentications """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?({host}[\w\-.]+) ({event_name}CISE_Passed_Authentications)"""
    """Issuer=({user_dn}.+?[^\\]),""",
    """AD-User-Resolved-DNs=({user_dn}.+?[^\\]),""",
    """AD-User-DNS-Domain=({domain}[^,]+),""",
    """Subject Alternative Name - EMail=({email_address}[^@]+@[^,]+),""",
    """Calling-Station-ID=(::ffff:)?(({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})({calling_station_id}[^,]+))""",
    """SSID=([^:]+:)?({ssid}[^,]+),""",
    """Called-Station-ID=({dest_mac}[\w\-.]+)(:({ssid}[^,]+))?,""",
    """User-?Name =(([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2}|({user}[^\s,;@]+))""",
    """User-?Name =({user}[^,;@\s]+)@({domain}[^,;@\s]+?)(,|;)""",
    """AcsSessionID=({acs_session_id}[^,]+),""",
    """AuthenticationIdentityStore=({auth_server}[^,]+),""",
    """AuthenticationMethod=({auth_method}[^,]+),""",
    """SelectedAuthorizationProfiles=({access_type}[^,]+),""",
    """IdentityGroup=({identity_group}[^,]+),""",
    """NetworkDeviceProfileName =({network}[^,]+),""",
    """RadiusFlowType=({radius_flow_type}[^,]+),""",
    """, Device IP Address=(::ffff:)?({src_ip}[^,]+),""",
    """NAS-IP-Address=({nas_ip_address}[A-Fa-f\d:.]+)"""
  ]


}
```