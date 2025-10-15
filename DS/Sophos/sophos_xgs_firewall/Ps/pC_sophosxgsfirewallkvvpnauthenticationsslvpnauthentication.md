#### Parser Content
```Java
{
Name = sophos-xgsfirewall-kv-vpn-authentication-sslvpnauthentication
  Product = Sophos XGS Firewall
  Conditions = [ """log_component="SSL VPN Authentication"""", """log_type="Event"""", """ login to SSLVPN through """, """log_subtype="Authentication"""" ]
  ParserVersion = "v1.0.0"
  Fields=${SophosParsersTemplates.kv-sophos-xgs-event.Fields}[
    """({event_name}login to SSLVPN)"""
  ]

kv-sophos-xgs-event = {
  Vendor = Sophos
  Product = Sophos XGS Firewall
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """timestamp="({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d(\+|\-)\d{4})""",
    """log_id="({event_code}\d+)""",
    """log_type="({event_category}[^"]+)""",
    """log_subtype="({subtype}[^"]+)""",
    """log_component="({app}(Firewall|SSL VPN|CLI|GUI|VPN Portal|AD SSO))""",
    """status="({result}[^"]+)""",
    """severity="({severity}[^"]+)""",
    """user_name="(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))?"\s.*?\s""",
    """auth_mechanism="({auth_method}[^"]+)""",
    """src_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """message="({additional_info}[^"]+)""",
    """src_country="({src_country}[^"]+)""",
    """bytes_sent="({bytes_out}\d+)""",
    """protocol="({protocol}[^"]+)""",
    """reason="({result_reason}[^"]+)"""
  
}
```