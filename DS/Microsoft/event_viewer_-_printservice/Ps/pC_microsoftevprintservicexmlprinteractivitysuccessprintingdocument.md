#### Parser Content
```Java
{
Name = "microsoft-evprintservice-xml-printer-activity-success-printingdocument"
  Vendor = "Microsoft"
  Product = "Event Viewer - PrintService"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [
    """Microsoft-Windows-PrintService"""
    """<UserData><"""
    """<EventID>"""
  ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)"""
    """<Computer>({host}[\w\-.]+)"""
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """UserID\\*=('|")({user_sid}[^\s'"]+)"""
    """<Opcode>({result}[^\d<]+)"""
    """<EventID>({event_code}\d+)"""
    """<Message>({activity_1}.*?\s*(?i)Document) \d+,"""
    """owned by [^\s]+\s*.*?( on [^\s]+)?({activity_2}.+?) on ({printer_name}.+?)(\.\s+|\s+through)"""
    """<Message>[^,]+,\s+({file_name}({object}.+?))\s+owned by"""
    """owned by ({user}[\w\.\-\!\#\^\~]{1,40}\$?) (to|on) """
    """owned by.+? on \\*(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}.+?)) was """
    """through port (\w+_)?(?:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|\\*({dest_host}[\w\-.]+?))\.\s+"""
    """Size in bytes:\s+({bytes}\d+)"""
    """Pages printed:\s+({num_pages}\d+)"""
    """({access}Read-Only)"""
    """<Channel>({channel}[^<]+)<"""
    """<Printer>({printer_name}[^<]+)<"""
    """<UserData>({additional_info}.+?)<\/UserData>"""
    """<Param2>({file_name}({object}[^<]+))<""",
    """<Param3>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<"""
    """<Param4>({src_host}[\w\-.]+)<"""
    """<Param5>({printer_name}[^<]+)<"""
    """<Param6>(?:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+))<"""
    """<Param7>({bytes}\d+)<"""
    """<Param8>({num_pages}\d+)<"""
    """<Copies>({num_pages}\d+)<"""
    """<ErrorCode>({error_code}[^<]+)<"""
    """<Level>({run_level}[^<]+)<"""
  ]
  ParserVersion = "v1.0.0"


}
```