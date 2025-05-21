#### Parser Content
```Java
{
Name = "microsoft-evprintservice-str-printer-activity-success-pagesprinted"
  Vendor = "Microsoft"
  Product = "Event Viewer - PrintService"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """ was printed on """
    """ Pages printed: """
    """No user action is required."""
    """ through port """
    """ Size in bytes: """
    """ owned by """
  ]
  Fields = [
     """({operation}print)"""
     """Pages printed:\s*({num_pages}\d+)"""
     """Size in bytes:\s*({bytes}\d+)"""
     """,\s+({object}[^:]+?)\s+owned by"""
     """printed on ({printer_name}[^\s]+)"""
     """owned by ({user}[\w\.\-\!\#\^\~]{1,40}\$?) on ({src_host}[^\s]+)"""
     """through port (({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+))(_\d+)?\."""
  ]
  ParserVersion = "v1.0.0"


}
```