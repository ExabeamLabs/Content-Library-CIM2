#### Parser Content
```Java
{
Name = dragos-dragosp-cef-app-notification-success
  Vendor = Dragos
  Product = Dragos Platform
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """|Dragos|""" , """notification""", """|Platform|""", """content="""]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+\S+)"""
    """occurredAt=({time}\d+-\d+-\d+T\d+:\d+:\d+\S+)"""
    """content=({additional_info}[^=]+)\."""
    """notification\|[^\|]+\|({severity}\d+)\|"""
    """\sasset_hostname=({host}[^\s]+)\s"""
    """\ssrc_asset_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\sdst_asset_ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """dst_asset_hostname=({dest_host}[^\s]+)\s"""
    """dst_asset_mac=({dest_mac}[^\s]+)\s"""
    """dst_asset_domain=({dest_domain}[^\s]+)\s"""
    """src_asset_hostname=({src_host}[^\s]+)\s"""
    """src_asset_mac=({src_mac}[^\s]+)\s"""
    """src_asset_domain=({src_domain}[^\s]+)\s"""
    """type=({object}[^\s]+)"""
    """\sid=({event_id}[^\s]+)"""
    ]
    ParserVersion = "v1.0.0"


}
```