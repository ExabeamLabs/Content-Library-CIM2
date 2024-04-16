#### Parser Content
```Java
{
Name = citrix-netscalerwaf-str-network-traffic-default
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Web App Firewall
  TimeFormat = "MM/dd/yyyy:HH:mm:ss z"
  Conditions = [ """ : default""", """ Vserver""", """-PPE""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d\s*GMT)\s({host}[^\s]+).*?:\sdefault\s({protocol}[^\s]+)\s({event_name}[^\s]+)"""
    """Source\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)"""
    """Client(IP|_ip)\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """ClientPort\s*({src_port}\d+)"""
    """Vserver\s({dest_translated_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}):({dest_translated_port}\d+)"""
    """VserverServiceIP\s({dest_translated_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})"""
    """VserverServicePort\s*({dest_translated_port}\d+)"""
    """Nat(IP|_ip)\s({src_translated_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})(:({src_translated_port}\d+))?"""
    """Destination\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+)"""
    """Total_bytes_send\s({bytes_out}\d+)"""
    """Total_bytes_recv\s({bytes_in}\d+)"""
    """\sUser\s(-|({email_address}[^@"\s]+@[^@"\s]+)|({user}[\w\.\-]{1,40}\$?))\s"""
    """Errmsg\s*"({failure_reason}[^"]+?)("|$)"""
  ]
  DupFields = [ "event_name->operation" ]


}
```