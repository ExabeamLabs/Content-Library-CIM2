#### Parser Content
```Java
{
Name = tanium-ep-kv-app-authentication-exabeamlogoneventest
    ParserVersion = v1.0.0
    Vendor = Tanium
    Product = Endpoint Platform
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
    Conditions = [ """ Tanium """, """Question="Exabeam-Logon-Even-Test"""" ]
    Fields = [
      """({host}[\w.\-]+)\s+Tanium """,
      """\sEndpoint-Name ="(-|({dest_host}[^"]+))"""",
      """\sTimestamp="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)""",
      """\sTarget-User="(-|({user}[^"]+))"""",
      """\sTarget-Domain="(-|({domain}[^"]+))"""",
      """\sLogon-Result="(-|({result}[^"]+))"""",
      """\sLogon-Type="(-|({login_type_text}[^"]+))"""",
      """\sLogon-Provider="(-|({auth_method}[^"]+))"""",
      """\sProcess="(-|({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+)))"""",
      """\sSource-IP-Address="(::1|({src_ip}[a-fA-F\d.:]+))"""",
    ]


}
```