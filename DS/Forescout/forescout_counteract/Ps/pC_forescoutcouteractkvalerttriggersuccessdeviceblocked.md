#### Parser Content
```Java
{
Name = forescout-couteract-kv-alert-trigger-success-deviceblocked
  ParserVersion = v1.0.0
  Conditions = [ """ - DEVICE BLOCKED - """ ]

counteract-network-alert = {
  Vendor = Forescout
  Product = Forescout CounterACT
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """(\w+\s+\d+ \d+:\d+:\d+)\s+({host}\S+)\s+({alert_type}.+?)\s+-\s+({alert_name}DEVICE BLOCKED - [^\s:]+)""",
    """(\w+\s+\d+ \d+:\d+:\d+)\s+({host}\S+)\s+CounterACT:\s+({alert_name}Unauthorized Host event at .+?)/({alert_type}.+?)\[\d+\]:""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """from\[({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))\]\s+to\[({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))\]""",
  
}
```