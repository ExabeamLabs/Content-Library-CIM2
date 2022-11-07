#### Parser Content
```Java
{
Name = pan-gp-leef-vpn-logout-success-gatewaylogout
  Conditions = [ """LEEF:""", """|Palo Alto Networks|""", """|PAN-OS Syslog Integration|""", """|gateway-logout-success|""", """|Type=GLOBALPROTECT|""" ]
  ParserVersion = "v1.0.0"

leef-pan-vpn-event = {
  Vendor = Palo Alto Networks
  Product = Palo Alto GlobalProtect
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Fields = [
    """\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d\s({host}[\w\-.]+)""",
    """ReceiveTime=({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)""",
    """usrName =(({domain}[^\\|]+)\\)?({user}[^|]+)""",
    """PrivateIP=({src_translated_ip}[A-Fa-f\d:.]+)""",
    """PublicIP=({src_ip}[A-Fa-f\d:.]+)""",
    """Machinename=({src_host}[\w\-.]+)""",
    """EventID=({event_name}[^|]+)""",
    """Status=({result}[^|]+)"""
  
}
```