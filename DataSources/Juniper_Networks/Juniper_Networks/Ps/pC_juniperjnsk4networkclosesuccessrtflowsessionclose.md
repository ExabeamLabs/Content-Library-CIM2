#### Parser Content
```Java
{
Name = juniper-jn-sk4-network-close-success-rtflowsessionclose
  ParserVersion = "v1.0.0"
  Conditions = [ """source-address="""", """destination-address="""", """session-id-32="""", """junos""", """RT_FLOW_SESSION_CLOSE""" ]

juniper-network-connection {
    Vendor = Juniper Networks
    Product = Juniper Networks
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d\:\d\d:\d\d\.\d\d\dZ)"""",
      """"host":"({host}[^"]+)"""",
      """service-name="+((?i)(none)|({service_name}[^"]+))""",
      """service-name="+(junos-)?(ms-)?((?i)(none)|({protocol}\w+))""",
      """bytes-from-server="({bytes_out}\d+)""",
      """bytes-from-client="({bytes_in}\d+)""",
      """\ssource-address="(({src_ip}[A-Fa-f:\d.]+))""",
      """\sdestination-address="(({dest_ip}[A-Fa-f:\d.]+))""",
      """\ssource-port="(({src_port}\d+))""",
      """\sdestination-port="(({dest_port}\d+))""",
      """\ssource-zone-name="(({src_zone}[^"]+))""",
      """\sdestination-zone-name="(({dest_zone}[^"]+))""",
      """\snat-source-address="({src_translated_ip}[A-Fa-f:\d.]+)""",
      """\snat-destination-address="({dest_translated_ip}[A-Fa-f:\d.]+)""",
      """nat-source-port="({src_translated_port}\d+)""",
      """nat-destination-port="({dest_translated_port}\d+)""",
      """packet-incoming-interface="({src_interface}[^"]+)""",
      """session-id-32="({session_id}[^"]+)""",
      """requestClientApplication=({app}.+?)\s*\w+=""",
      """\sapplication="((?i)(UNKNOWN)|({app}[^"]+))""",
      """policy-name="({policy_name}[^"]+)""",
      """({event_name}RT_FLOW_SESSION_({action}[^"]+))""",
      """reason="({result}[^"]+)""",
   ]
 },
}
#============================================== Start of JuniperParsers section ==================================================================
JuniperParsers = [

{
  Name = juniper-ps-cef-vpn-login-success-connected
  ParserVersion = v1.0.0
  Vendor = Juniper Networks
  Product = Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
"""CEF:"""
"""PulseSecure: """
""" Connected to """
]
  Fields = [
    """PulseSecure:.+?({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({host}[\w\-.]+)""",
    """\s+-\s+\[({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\]""",
    """\Wuser=([^\\]+\\)?({user}[^\s\|]+)""",
    """\s+-\s+\[[^\]]+\]\s+(({domain}[^\(]+)\\)?({user}.+?)\(({realm}[^\)]+)?\)""",
    """\sConnected to\s+(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\.-]+))\s+port"""
  ]
  DupFields = [ "user->account" 
}
```