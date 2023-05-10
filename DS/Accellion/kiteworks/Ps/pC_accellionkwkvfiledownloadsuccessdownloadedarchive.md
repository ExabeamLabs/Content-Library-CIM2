#### Parser Content
```Java
{
Name = accellion-kw-kv-file-download-success-downloadedarchive
  ParserVersion = v1.0.0
  Product = Kiteworks
  Conditions = [ """Downloaded archive""", """Activity:""" ]
  Fields = ${KiteWorksParsersTemplates.q-kiteworks-file-activity.Fields}[
    """({access}Downloaded)"""
    """with Files:\s*({src_file_name}[^\",]+?(\.({src_file_ext}\w+))?)(,({additional_info}.+?))?\.\s*$"""
    """({access}Downloaded) archive \"*({file_name}[^\"]+?(\.({file_ext}\w+))?)\"* from \"*({additional_info}[^\"]+)"""
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