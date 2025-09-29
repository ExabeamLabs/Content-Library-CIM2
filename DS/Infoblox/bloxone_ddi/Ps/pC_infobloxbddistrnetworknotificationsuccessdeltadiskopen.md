#### Parser Content
```Java
{
Name = infoblox-bddi-str-network-notification-success-deltadiskopen
	ParserVersion = v1.0.0
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """vobd:""", """Non-empty delta disk being open""" ]
  Fields = [      
	  """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{1,6}Z)\s+({host}[\w.-]+)\s+({additional_info}[^~]+?)\s*$""",
    """({operation}Non-empty delta disk being open)"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  DupFields = ["operation->event_name"]


}
```