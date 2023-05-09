#### Parser Content
```Java
{
Name = cisco-ise-kv-radius-traffic-fail-deviceadministrationfailed
  ParserVersion = v1.0.0
  Conditions = [ """Device-Administration: """, """ failed""" ]

s-nac-logon = {
  Vendor = Cisco
  Product = Cisco ISE
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\s+\d+\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """\s(::ffff:)?({host}(?!\d\d:\d\d:\d\d)[\w.\-]+)\s+(\S+\s+){3}(\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
    """\s(::ffff:)?({host}(?!\d\d:\d\d:\d\d)[\w.\-]+)\s+(\S+\s+){4}(\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
    """User-?Name =(([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2}|host\/({src_host}[\w\-.]+)|({user}[^,;]+?))(,|;)"""
    """User-?Name =(({domain}[^,;]+?)[\\\/]+)?(([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2}|({user}[^,;\\\/@]+))"""
    """User-?Name =([^,;]+?[\\\/]+)?({user}[^,;\\\/@]+)@({domain}[^,;]+)"""
    """, UserName =host\/[^.]+\.({domain}[^,]+),\s*NAS-IP-Address"""
    """, UserName =(({user_type}host)\/)?(({domain}[^\s\\]+)\\+)?(USERNAME|([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2}|({user}[^,@]+))"""
    """Called-Station-ID=(({dest_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|(::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|(::ffff:)?({dest_host}[\w\-.]+))(:({ssid}[^,]+))?,"""
    """, Calling-Station-ID=(({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|(::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|(::ffff:)?({src_host}[\w\-.]+))"""
    """AD-User-Candidate-Identities=((::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|(::ffff:)?({dest_host}[\w\-.]+)),"""
    """, AD-Host-Resolved-Identities=((::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|(::ffff:)?({dest_host}[^\s,@]+)[^,]*\s*)"""    
    """, AD-Host-Resolved-Identities=({computer_name}[^@,]+)"""
    """, NetworkDeviceName =({network}[^,]+),"""
    """, Device IP Address=({auth_server}[^,]+),"""
    """, Device IP Address=(::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,"""
    """, Framed-IP-Address=(::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?,"""
    """DestinationIPAddress=(::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """, NetworkDeviceGroups=Location#All Locations#({location}[^,]+)"""
    """(?i)(MacAddress)=({src_mac}[^,\s]+),"""
    """NAS-IP-Address=({nas_ip_address}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
 
}
```