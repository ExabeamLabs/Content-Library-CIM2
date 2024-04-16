#### Parser Content
```Java
{
Name = forescout-couteract-kv-alert-trigger-success-virtualfirewall
  Vendor = Forescout
  Product = Forescout CounterACT
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Block Event:""", """Target:""", """rule: true""", """Reason:""", """Virtual Firewall - Limit Inbound""", """Is Virtual Firewall blocking""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}[\w\-.]+)""",
    """({alert_name}Block Event)""",
    """Host:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Target:\s*(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[^\s]+))""",
    """Service:\s*({dest_port}\d{1,5})""",
    """({operation}Virtual Firewall blocking)""",
    """Reason:\s*({failure_reason}Virtual Firewall - Limit Inbound)""",
  ]


}
```