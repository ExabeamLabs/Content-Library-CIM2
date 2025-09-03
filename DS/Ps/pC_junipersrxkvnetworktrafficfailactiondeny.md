#### Parser Content
```Java
{
Name = juniper-srx-kv-network-traffic-fail-actiondeny
  ParserVersion = v1.0.0
  Conditions = [ 
"""NetScreen"""
""" start_time=""""
""" src zone="""
""" action=Deny"""
]
  Fields = ${JuniperParsersTemplates.juniper-firewall-network-traffic.Fields} [
    """\Wreason=({failure_reason}.+?)\s*(\w+=|$)""",
  ]


}
```