#### Parser Content
```Java
{
Name = "dell-sw-kv-alert-trigger-success-networkalert"
    Conditions = [
        """ m="""
        """id="""
        """ fw="""
        """ c="""
        """ msg=""""
        """ pri=0 """
        """ src="""
        """ dst="""
    ]
    ParserVersion = "v1.0.0"

sonicwall-vpn-login = {
  Vendor = Dell
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\d\d:\d\d:\d\d ({host}[^\s]+)\sSSLVPN:""",
    """\stime="({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(:({src_interface}[^\s:]+))?(:({src_host}[^\s:]+))?""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?(:({dest_interface}[^\s:]+))?(:({dest_host}[^\s:]+))?""",
    """\suser="\s*(({email_address}[^@"]+@[^\\\s"]+)|({user}[\w\.\-]{1,40}\$?))""",
    """\susr="\s*(({email_address}[^@"]+@[^\\\s"]+)|({user}[\w\.\-]{1,40}\$?))\s*"""",
    """\sproto=({protocol}\S+)""",
    """\sdomain="({domain}[^"]+)"""",
    """\sportal="({realm}[^"]+)"""",
    """\sagent="({user_agent}[^"]+)"""",
    """\sduration=({session_duration}\d+)""",
    """\sbytesIn=({bytes_in}\d+)""",
    """\sbytesOut=({bytes_out}\d+)""",
    """\sbytesTotal=({bytes}\d+)"""
  ]
  DupFields = ["user->account"
}
```