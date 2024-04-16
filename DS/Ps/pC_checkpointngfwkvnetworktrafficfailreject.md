#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-network-traffic-fail-reject
  Conditions = [ """ CheckPoint """, """action:"Reject"""", """product:"VPN-1"""" ]
  ParserVersion = "v1.0.0"

checkpoint-auth.Fields}[
    """action:"+({operation}[^"]+)""",
    """\Wtime(:|=)"({time}\d{10})""""
  ]
  DupFields = [ "operation->event_name" 
}
```