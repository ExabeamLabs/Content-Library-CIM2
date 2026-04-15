#### Parser Content
```Java
{
Name = citrix-appfw-str-app-notification-message
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Gateway
  TimeFormat = [ "MM/dd/yyyy:HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ssZ" ]
  Conditions = [ """ default""", """ : """, """-PPE"""]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)(\s+GMT)?\s*({host}[^\s]+).*?:\sdefault\s({protocol}[^\s]+)""",
    """({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s*({host}[^\s]+)\s({protocol}[^\s]+)"""
    """Message.*?"\s*({additional_info}[^\|]+?)[\s"]*(\||$)"""
    """Username = ({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """Remote ip = ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """gateway_vip ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """clientside_txbytes ({bytes_out}\d+)"""
    """clientside_rxbytes ({bytes_in}\d+)"""
    """ICAUUID = ({session_id}[^\s\]]+)"""
    ]


}
```