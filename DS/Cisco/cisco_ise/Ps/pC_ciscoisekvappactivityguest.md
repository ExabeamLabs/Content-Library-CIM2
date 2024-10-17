#### Parser Content
```Java
{
Name = cisco-ise-kv-app-activity-guest
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco ISE
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [""" CISE_Guest """]
  Fields = [
    """({host}\S+) ({event_name}CISE_Guest) (\S+\s+){3}({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """\sUserName =({user}[\w\.\-\!\#\^\~]{1,40}\$?)(,|;)""",
    """\sUserName =({email_address}[^,;@\s]+@[^,;@\s]+?)(,|;)""",
# auditsessionid is removed
# guestusername is removed
    """IdentityGroup=({identity_group}[^,]+?),""",
    """(?i)(MacAddress)=({src_mac}[^,]+?),""",
# ipaddress is removed
# usertype is removed
    """Calling-Station-ID=({calling_station_id}[^,\s]+),""",
# called_station_id is removed
    """\s*IpAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```