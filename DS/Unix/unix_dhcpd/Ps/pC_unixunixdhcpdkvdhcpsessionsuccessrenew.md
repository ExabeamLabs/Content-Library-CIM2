#### Parser Content
```Java
{
Name = "unix-unixdhcpd-kv-dhcp-session-success-renew"
Vendor = "Unix"
Product = "Unix dhcpd"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ dhcpd: """
  """ RENEW """
]
Fields = [
  """\w+ \d+ \d\d:\d\d:\d\d ({host}[\w.\-]+) dhcpd:"""
  """({event_name}RENEW)"""
  """sIP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sMAC=({dest_mac}[a-fA-F\d.:]+)"""
  """\sHOSTNAME=(?:nil|({dest_host}.+?))\s+\w+="""
  """\sDOMAIN=({domain}.+?)\s+\w+="""
  """\sLEASETIME=({lease_time}.+?)\s+\w+="""
]
DupFields = [
  "dest_host->user"
]
ParserVersion = "v1.0.0"


}
```