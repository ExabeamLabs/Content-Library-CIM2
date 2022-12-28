#### Parser Content
```Java
{
Name = juniper-ps-json-vpn-login-success-started
    ParserVersion = v1.0.0
    Vendor = Juniper Networks
    Product = Juniper Pulse Secure
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [
""": Session started for user""", """"message":"""", """Juniper:"""
]
    Fields = [
      """\stime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
      """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """\sfw=({host}[\w\-\.]+)""",
      """({host}[\w\-\.]+)\s*:\s*\S+\s*\-\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d).*?: Session started for user""",
      """,\s+hostname\s+({src_host}[\w.\-]+)""",
      """\- \[({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\]"""
      """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s""",
      """with IP(?:v4 address)?\s+({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\srealm=[\\"]*({realm}.+?)[\\"]*(\s+\w+=|\s*")""",
      """\sroles=[\\"]*({roles}.+?)[\\"]*(\s+\w+=|\s*")""",
      """\svpn=[\\"]*({vpn}.+?)[\\"]*(\s+\w+=|\s*")""",
      """user=({user}.+?)(\s+\w+=|\s*")"""
      """\sfw=({firewall}[a-fA-F\d.:]+)"""
      """\stype=({vpn_type}[^=]+?)(\s+\w+=|\s*$)"""
    ]
    DupFields = [ "host->dest_host" , "user->account" ]
  

}
```