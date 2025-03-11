#### Parser Content
```Java
{
Name = "cisco-mma-kv-network-traffic-success-association"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = Cisco Network Security
  TimeFormat = "epoch_sec"
  Conditions = [
""" events type"""
""" type"""
""" aid"""
  ]
  Fields = [
"""({time}\d{10})\.\d+\s+({host}[\w.\-]+)\s+events\s"""
"""\scs6=\d+\-\d+\-\d+T\d\d:\d\d:\d\d\.\d+Z\s+({host}[a-fA-F\d.:]+)"""
"""\sclient_ip\\*='({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sclient_mac\\*='({src_mac}[a-fA-F\d.:]+)"""
"""\stype\\*=(|({operation}.+?))(\s+\w+\\*=|\s*$)"""
"""\said\\*='({aid}[^']+)"""
"""\schannel\\*='({channel}[^']+)"""
"""\sduration\\*='({duration}[^']+)"""
"""\sip_src\\*='({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sdhcp_ip\\*='({dhcp_ip}[^']+)"""
"""\sidentity\\*='(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'"""
  ]


}
```