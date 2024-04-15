#### Parser Content
```Java
{
Name = "microsoft-evprintservice-xml-printer-activity-success-printingdocument"
  Vendor = "Microsoft"
  Product = "Event Viewer - PrintService"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [
    """Microsoft-Windows-PrintService"""
    """Printing a document"""
    """<EventID>"""
  ]
  Fields = [
    """<TimeCreated SystemTime='({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)"""
    """<Computer>({host}[\w\-.]+)"""
    """UserID='({user_sid}[^\s']+)"""
    """<Opcode>({result}[^\d<]+)"""
    """<EventID>({event_code}\d+)"""
    """<Message>({activity_1}.*?\s*(?i)Document) \d+,"""
    """owned by [^\s]+\s*.*?( on [^\s]+)?({activity_2}.+?) on ({printer_name}.+?)(\.\s+|\s+through)"""
    """<Message>[^,]+,\s+({object}.+?)\s+owned by"""
    """owned by ({user}.+?) (to|on) """
    """owned by.+? on \\*(?:({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}.+?)) was """
    """through port (\w+_)?(?:({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|\\*({dest_host}.+?))\.\s+"""
    """Size in bytes:\s+({bytes}\d+)"""
    """Pages printed:\s+({num_pages}\d+)"""
    """({access}Read-Only)"""
  ]
  DupFields = [
    "object->file_name"
    "object->operation"
  ]
  ParserVersion = "v1.0.0"


}
```