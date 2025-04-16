#### Parser Content
```Java
{
Name = cisco-ise-kv-endpoint-authentication-cisepassed
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Identity and Access Management
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
    """,\s*AD-User-SamAccount-Name =({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """User-?Name =(([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2}|((({domain}[^=]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
    """User-?Name =({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^,;@\s]+?)(,|;)""",
    """AcsSessionID=({acs_session_id}[^,]+),""",
    """AuthenticationIdentityStore=({auth_server}[^,]+),""",
    """AuthenticationMethod=({auth_method}[^,]+),""",
    """SelectedAuthorizationProfiles=({access_type}[^,]+),""",
    """IdentityGroup=({identity_group}[^,]+),""",
    """NetworkDeviceProfileName =({network}[^,]+),""",
    """RadiusFlowType=({radius_flow_type}[^,]+),""",
    """, Device IP Address=(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,""",
    """NAS-IP-Address=({nas_ip_address}[A-Fa-f\d:.]+)"""
  ]


}
```