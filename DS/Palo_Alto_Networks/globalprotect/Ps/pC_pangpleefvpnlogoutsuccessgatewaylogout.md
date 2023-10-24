#### Parser Content
```Java
{
Name = pan-gp-leef-vpn-logout-success-gatewaylogout
  Conditions = [ """LEEF:""", """|Palo Alto Networks|""", """|PAN-OS Syslog Integration|""", """|gateway-logout-success|""", """|Type=GLOBALPROTECT|""" ]
  ParserVersion = "v1.0.0"

leef-pan-vpn-event = {
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d\s({host}[\w\-.]+)""",
    """ReceiveTime=({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)""",
    """usrName =(({domain}[^\\|]+)\\)?({user}[\w\.\-]{1,40}\$?)""",
    """PrivateIP=({src_translated_ip}[A-Fa-f\d:.]+)""",
    """PublicIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Machinename=({src_host}[\w\-.]+)""",
    """EventID=({event_name}[^|]+)""",
    """Status=({result}[^|]+)""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  
}
```