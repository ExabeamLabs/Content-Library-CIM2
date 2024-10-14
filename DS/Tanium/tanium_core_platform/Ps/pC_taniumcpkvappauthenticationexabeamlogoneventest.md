#### Parser Content
```Java
{
Name = tanium-cp-kv-app-authentication-exabeamlogoneventest
    ParserVersion = v1.0.0
    Vendor = Tanium
    Product = Tanium Core Platform
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
    Conditions = [ """ Tanium """, """Question="Exabeam-Logon-Even-Test"""" ]
    Fields = [
      """({host}[\w.\-]+)\s+Tanium """,
      """\sEndpoint-Name ="(-|({dest_host}[^"]+))"""",
      """\sTimestamp="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)""",
      """\sTarget-User="(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
      """\sTarget-Domain="(-|({domain}[^"]+))"""",
      """\sLogon-Result="(-|({result}[^"]+))"""",
      """\sLogon-Type="(-|({login_type_text}[^"]+))"""",
      """\sLogon-Provider="(-|({auth_method}[^"]+))"""",
      """\sProcess="(-|({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+)))"""",
      """\sSource-IP-Address="(::1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
    ]


}
```