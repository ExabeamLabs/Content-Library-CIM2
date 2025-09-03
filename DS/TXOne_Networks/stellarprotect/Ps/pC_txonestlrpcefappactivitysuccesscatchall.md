#### Parser Content
```Java
{
Name = txone-stlrp-cef-app-activity-success-catchall
  ParserVersion = v1.0.0
  Product = StellarProtect
  Conditions = [ """CEF:""", """|TXOne Networks|""", """|StellarProtect|""" ]

stellar-cef-event = {
  Vendor = "TXOne Networks"
  TimeFormat =[ "yyyy-MM-dd'T'HH:mm:ssZ"]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) Stellar"""
    """\|({event_id}[^\|]+)\|Agent Event\|"""
    """msg=({additional_info}[^=]+?)\s\w+="""
    """serverIP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """eventId=({event_id}\d+)"""
    """agentIp=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """agentOS=({os}[^=]+?)\s\w+="""
    """accessUser=(({domain}[^\\=]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """parentProcess\d+=({process_path}({process_dir}[^=]+)\\({process_name}[^=]+?))\s\w+="""
    """accessImagePath=[^=]+\\({image_name}[^=]+?)\s\w+="""
    """mode=({operation}[^=]+?)\s\w+="""
    """list=({failure_reason}[^=]+?)\s\w+="""
    """fileHashBlocked=({file_hash}[^=]+?)\s\w+="""
    """category=({event_category}\d+)"""
    """({alert_name}Anomaly Detection)"""
    """\|Agent Event\|({alert_severity}\d+)"""
    """TXOne Networks\|({log_source}[^\|]+)"""
  
}
```