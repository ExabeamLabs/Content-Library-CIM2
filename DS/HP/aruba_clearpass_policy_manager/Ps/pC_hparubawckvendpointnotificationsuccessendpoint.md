#### Parser Content
```Java
{
Name = hp-arubawc-kv-endpoint-notification-success-endpoint
  ParserVersion = "v1.0.0"
  Conditions = [ """ CPPM_Endpoint """, """Endpoint.MAC-Address=""", """,Endpoint.Username=""" ]

aruba-clearpass-events = {
  Vendor = HP
  Product = Aruba ClearPass Policy Manager
  TimeFormat = ["yyyy-MM-dd HH:mm:ss.SSZ", "MMM dd HH:mm:ss"]
  Fields = [
    """({time}\w+\s+\d+ \d+:\d+:\d+)"""
    """RADIUS\.Acct-Timestamp=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d(\.\d+?[\+\-]\d+))""",
    """\s\d\d\s\d\d:\d\d:\d\d\s({host}[\w\.\-]+)\sLEEF:""",
    """RADIUS\.Acct-Username=(?:({user_type}host)/)(({src_domain}[^\\\s,]+)\\+)?(anonymous|({src_host}[\w\-\.]+))""",
    """RADIUS\.Acct-Username=(?!(host)/)(({domain}[^\\\s,]+)\\+)?(anonymous|({user}[[\w\.\-]{1,40}\$?))""",
    """Auth.Username=({user}[\w\.\-]{1,40}\$?)\sAuth""",
    """Auth.Protocol=({protocol}[^\s]{1,2000})\sAuth""",
    """\s(Auth\.|RADIUS\.Acct\-)NAS-IP-Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s\w+""",
    """RADIUS\.Acct-Framed-IP-Address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sAuth.Host-MAC-Address=({src_mac}\w+)\s""",
    """RADIUS.Acct-NAS-Port=({dest_port}\d+)""",
    """Auth.Login-Status=(0|({result_code}\d+))"""
    """Auth.Enforcement-Profiles=\[({additional_info}[^\}]+)\]"""
    """Auth.Service=({service_name}[^=]+?)\sAuth"""
  
}
```