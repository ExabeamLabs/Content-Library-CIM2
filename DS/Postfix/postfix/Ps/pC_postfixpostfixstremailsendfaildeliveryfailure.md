#### Parser Content
```Java
{
Name = "postfix-postfix-str-email-send-fail-deliveryfailure"
  Vendor = "Postfix"
  Product = "Postfix"
  TimeFormat = ["MMM dd HH:mm:ss"]
  Conditions = [ 
    """postfix/smtp["""
    """] said:"""
    """]:"""
  ]
  Fields = [
    """({time}\w\w\w \d\d \d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\s({process_name}[^\[]+)\[({process_id}[^\]]+)]\s*({message_id}[\w]+)"""
    """\Wsaid:\s*[\d\.\-\s]+\s({additional_info}[^\(]+)\(in reply"""
    """\Whost\s*({dest_host}[\w\-\.]+)\[({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"


}
```