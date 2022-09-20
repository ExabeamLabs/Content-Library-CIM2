#### Parser Content
```Java
{
Name = cisco-ise-kv-radius-traffic-success-deviceadminstrationsucceeded
  ParserVersion = v1.0.0 
  Conditions = [ """Device-Administration: """, """ succeeded""" , """Protocol=""" ]

s-nac-logon = {
  Vendor = Cisco
  Product = Cisco ISE
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\s+\d+\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """\s(::ffff:)?({host}(?!\d\d:\d\d:\d\d)[\w.\-]+)\s+(\S+\s+){3}(\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
    """\s(::ffff:)?({host}(?!\d\d:\d\d:\d\d)[\w.\-]+)\s+(\S+\s+){4}(\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
    """User-?Name =(([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2}|({user}[^,;]+?))(,|;)"""
    """User-?Name =(({domain}[^,;]+?)[\\\/]+)?(([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2}|({user}[^,;\\\/@]+))"""
    """User-?Name =([^,;]+?[\\\/]+)?({user}[^,;\\\/@]+)@({domain}[^,;]+)"""
    """, UserName =host\/[^.]+\.({domain}[^,]+),\s*NAS-IP-Address"""
    """, UserName =(({user_type}host)\/)?(({domain}[^\s\\]+)\\+)?(USERNAME|([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2}|({user}[^,@]+))"""
    """Called-Station-ID=(({dest_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|(::ffff:)?({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})|(::ffff:)?({dest_host}[\w\-.]+))(:({ssid}[^,]+))?,"""
    """, Calling-Station-ID=(({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|(::ffff:)?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(::ffff:)?({src_host}[\w\-.]+))"""
    """AD-User-Candidate-Identities=((::ffff:)?({dest_ip}[A-Fa-f:\d.]+)|(::ffff:)?({dest_host}[\w\-.]+))"""
    """, AD-Host-Resolved-Identities=((::ffff:)?({dest_ip}[A-Fa-f:\d.]+)|(::ffff:)?({dest_host}[^\s,]+)\s*)"""
    """, AD-Host-Resolved-Identities=({computer_name}[^@,]+)"""
    """, NetworkDeviceName =({network}[^,]+),"""
    """, Device IP Address=({auth_server}[^,]+),"""
    """, Device IP Address=(::ffff:)?({src_ip}[^,]+),"""
    """, Framed-IP-Address=(::ffff:)?({dest_ip}[^,]+),"""
    """DestinationIPAddress=(::ffff:)?({dest_ip}[a-fA-F\d.:]+)"""
    """, NetworkDeviceGroups=Location#All Locations#({location}[^,]+)"""
    """(?i)(MacAddress)=({src_mac}[^,\s]+),"""
    """NAS-IP-Address=({nas_ip_address}[A-Fa-f\d:.]+)"""
 
}
```