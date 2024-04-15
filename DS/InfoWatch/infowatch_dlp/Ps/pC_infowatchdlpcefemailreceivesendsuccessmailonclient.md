#### Parser Content
```Java
{
Name = "infowatch-dlp-cef-email-receive-send-success-mailonclient"
Vendor = "InfoWatch"
Product = "InfoWatch DLP"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Mail on Client|"""
  """|DLP|DLP TM"""
]
Fields = [
  """\Wact=({action}.+?)(\s+[\w\.]+=|\s*$)"""
  """\Wrt=({time}\d{13})"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wsntdom=({src_email_address}[^@=]+?@[^@]+?)(\s+[\w\.]+=|\s*$)"""
  """\Wsuser=({user}.+?)(\s+[\w\.]+=|\s*$)"""
  """\Wduser=({email_recipients}({dest_email_address}[^;@=]+@[^;\s]+).*?)(\s+[\w\.]+=|\s*$)"""
  """\Wdvchost=({host}.+?)(\s+[\w\.]+=|\s*$)"""
  """\Wdvc=({host}.+?)(\s+[\w\.]+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```