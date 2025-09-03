#### Parser Content
```Java
{
Name = sophos-xgfirewall-kv-app-login-success-sfw-1
  Vendor = Sophos
  Product = Sophos XG Firewall
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","yyyy-MM-dd' time='HH:mm:ss"]
  Conditions = [ """device_name="SFW"""", """log_type="Event"""", """log_component="Firewall Authentication"""", """logged in successfully to Firewall""" ]
  Fields = [
    """timestamp="({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}(\+|\-)[\d:]+)""",
    """\slog_type="({event_category}\S+)?"\s""",
    """\slog_component="({app}Firewall)""",
    """\slog_subtype="(({subtype}\S+))?"\s""",
    """\sstatus="({result}\S+)?"\s""",
    """\severity="({severity}\S+)?"\s""",
    """\suser_name="(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))?"\s.*?\s""",
    """user_full_name="({full_name}[^"\s,]+\s*,?\s*[^"\s]+)""""
    """\sauth_mechanism="({auth_method}\S+)?"\s""",
    """\ssrc_ip="?({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})?"?\s""",
    """\Wmessage="({additional_info}[^"]+)(\w+=|$|")""",
    """\ssrc_country="({src_country}[^"]+)""""
    """({event_name}logged in successfully to Firewall)"""
  ]


}
```