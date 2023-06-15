#### Parser Content
```Java
{
Name = citrix-cgateway-str-vpn-logout-success-removesessiondebug
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Gateway
  TimeFormat = "MM/dd/yyyy:HH:mm:ss z"
  Conditions = [ """ SSLVPN REMOVE_SESSION_DEBUG """ ]
  Fields = [
    """({time}\d\d/\d\d/\d\d\d\d:\d\d:\d\d:\d\d \w+)\s+({host}[\w.\-]+)(\s+\S+){3}\s+SSLVPN ({event_name}REMOVE_SESSION_DEBUG)\s""",
    """\s((?i)SessionId):?\s*({session_id}\d+)""",
      """\sUser\s+({user}[^\-\s]+)\s""",
      """\sClient_ip\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\sVserver_ip\s+({dest_translated_ip}[a-fA-F\d.:]+)""",
      """\sErrmsg\s+"({result_reason}[^"]+)""",
  ]


}
```