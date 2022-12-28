#### Parser Content
```Java
{
Name = accellion-kw-str-app-login-success-sessionstarted
  ParserVersion = v1.0.0
  Product = Kiteworks
  Conditions = [ """Session started""", """Activity:""" ]

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