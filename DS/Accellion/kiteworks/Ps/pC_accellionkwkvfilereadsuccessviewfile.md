#### Parser Content
```Java
{
Name = accellion-kw-kv-file-read-success-viewfile
  ParserVersion = v1.0.0
  Product = Kiteworks
  Conditions = [ """View file""", """Activity:""" ]
  Fields = ${KiteWorksParsersTemplates.q-kiteworks-file-activity.Fields}[
    """\s({access}View) file\s+({file_name}.+?(\.({file_ext}\w+)))(\s+from email.|\.\s+File:)"""
  ]

q-kiteworks-file-activity = {
    Vendor = Accellion
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """\w+\s+\d+ \d+:\d+:\d+\s+({host}(({dest_ip}[A-Fa-f\d:.]+)|({dest_host}[\w.\-]+)))\s+"""
      """({host}(({dest_ip}[A-Fa-f\d:.]+)|({dest_host}[\w.\-]+)))\s+rest_server.py:"""
      """\ssize=({bytes}\d+)"""
      """({email_address}[^@\s]+@({email_domain}[^\s]+))\s+id=[^,]+,\s*({src_ip}[a-fA-F\d.:]+),\s*Activity:?"""
      """Activity:\s*({operation}.+?)\.\"*\s*$"""
      """Activity Type:\s+({operation}[^\s,]+)"""
     
}
```