#### Parser Content
```Java
{
Name = accellion-kw-kv-file-upload-success-uploadedfile
  ParserVersion = v1.0.0
  Product = Kiteworks
  Conditions = [ """Uploaded file""", """Activity:""", """File: id=""" ]
  Fields = ${KiteWorksParsersTemplates.q-kiteworks-file-activity.Fields}[
    """({access}Uploaded) file ({src_file_name}.+?(\.({src_file_ext}\w+))?)\.\s*File:"""
    """({access}Uploaded) file \"+({src_file_name}[^\"]+?(\.({src_file_ext}\w+))?)\""""
  ]
  DupFields = [ "src_file_name->file_name" ]

q-kiteworks-file-activity = {
    Vendor = Accellion
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """\w+\s+\d+ \d+:\d+:\d+\s+({host}[\w.\-]+)\s+"""
      """({host}[\w.\-]+)\s+rest_server.py:"""
      """\ssize=({bytes}\d+)"""
      """({email_address}[^@\s]+@({email_domain}[^\s]+))\s+id=[^,]+,\s*({src_ip}[a-fA-F\d.:]+),\s*Activity:?"""
      """Activity:\s*({operation}.+?)\.\"*\s*$"""
      """Activity Type:\s+({operation}[^\s,]+)"""
     ]
    DupFields = [ "host->dest_host" 
}
```