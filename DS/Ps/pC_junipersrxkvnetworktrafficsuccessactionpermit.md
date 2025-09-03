#### Parser Content
```Java
{
Name = juniper-srx-kv-network-traffic-success-actionpermit
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
"""NetScreen"""
""" start_time=""""
""" src zone="""
""" action=Permit"""
]
  Fields =  ${JuniperParsersTemplates.juniper-firewall-network-traffic.Fields} [
    """\Wreason=({failure_reason}.+?)\s*(\w+=|$)"""
  ]


}
```