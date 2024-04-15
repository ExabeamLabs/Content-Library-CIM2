#### Parser Content
```Java
{
Name = "microsoft-evprintservice-xml-printer-activity-success-printingdocument-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - PrintService"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "microsoft-windows-printservice"
      "printing a document"
      "<eventid>"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d+-\\d+-\\d+T\\d+:\\d+:\\d+\\.\\d+Z)"
      "(?i)<Computer>({host}[\\w\\-.]+)"
      "(?i)UserID='({user_sid}[^\\s']+)"
      "(?i)<Opcode>({result}[^\\d<]+)"
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)<Message>({activity_1}.*?\\s*(?i)Document) \\d+,"
      "(?i)owned by [^\\s]+\\s*.*?( on [^\\s]+)?({activity_2}.+?) on ({printer_name}.+?)(\\.\\s+|\\s+through)"
      "(?i)<Message>[^,]+,\\s+({object}.+?)\\s+owned by"
      "(?i)owned by ({user}.+?) (to|on) "
      "(?i)owned by.+? on \\\\*(?:({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?|({src_host}.+?)) was "
      "(?i)through port (\\w+_)?(?:({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?|\\\\*({dest_host}.+?))\\.\\s+"
      "(?i)Size in bytes:\\s+({bytes}\\d+)"
      "(?i)Pages printed:\\s+({num_pages}\\d+)"
      "(?i)({access}Read-Only)"
    ]
    DupFields = [
      "object->file_name"
      "object->operation"
    ]
    ParserVersion = "v1.0.0"
  

}
```