#### Parser Content
```Java
{
Name = "microsoft-windows-csv-dhcp-traffic-success-leaseexpired"
  Vendor = "Microsoft"  
  Product = "Microsoft DHCP Log" 
  TimeFormat = "MM/dd/yy,HH:mm:ss"  
  Conditions = [  
    """leases expired and """, """leases deleted,"""
  ] 
  Fields = [  
    """({time}\d\d\/\d\d\/\d\d,\d\d:\d\d:\d\d),({additional_info}[^,]+),"""
	  """({event_name}leases expired)"""
  ] 
  ParserVersion = "v1.0.0"  


}
```