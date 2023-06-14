#### Parser Content
```Java
{
Name = cisco-ie-cef-email-deliverystart
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "epoch"
    Conditions = [ """CEF:""", """MID """, """ RID """, """Delivery start DCID""" ]
    Fields = [
      """\srt=({time}\d{13})""",
      """MID ({alert_id}\d+)"""
	  """msg=({additional_info}.+?)\s\w+="""
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```