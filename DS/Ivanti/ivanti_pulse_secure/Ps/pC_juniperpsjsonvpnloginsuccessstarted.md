#### Parser Content
```Java
{
Name = juniper-ps-json-vpn-login-success-started
    ParserVersion = v1.0.0
    Vendor = Ivanti
    Product = Ivanti Pulse Secure
    TimeFormat = ["yyyy-MM-dd HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
    Conditions = [
""": Session started for user""", """"message":"""", """Juniper:"""
]
    Fields = [
      """\stime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
      """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """\sfw=({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+))""",
      """({host}[\w\-\.]+)\s*:\s*\S+\s*\-\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d).*?: Session started for user""",
      """,\s+hostname\s+({src_host}[\w.\-]+)""",
      """\- \[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]"""
      """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
      """with IP(?:v4 address)?\s+({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\srealm=[\\"]*({realm}.+?)[\\"]*(\s+\w+=|\s*")""",
      """\sroles=[\\"]*({role}.+?)[\\"]*(\s+\w+=|\s*")""",
      """\svpn=[\\"]*({vpn_client}.+?)[\\"]*(\s+\w+=|\s*")""",
      """user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\s*")"""
      """\sfw=({firewall}[a-fA-F\d.:]+)"""
      """\stype=({vpn_client_type}[^=]+?)(\s+\w+=|\s*$)"""
    ]
    DupFields = [ "user->account" ]
  

}
```