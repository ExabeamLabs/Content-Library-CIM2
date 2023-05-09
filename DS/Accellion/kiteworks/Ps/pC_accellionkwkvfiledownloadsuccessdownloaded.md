#### Parser Content
```Java
{
Name = accellion-kw-kv-file-download-success-downloaded
  ParserVersion = v1.0.0
  Product = Kiteworks
  Conditions = [ """Downloaded """, """Activity:""" ]
  Fields = ${KiteWorksParsersTemplates.q-kiteworks-file-activity.Fields}[
    """\sDownloaded (file|attachment)\s+({file_name}.+?(\.({file_ext}\w+)))\.\s+(Subject|File):"""
    """({access}Downloaded)"""
    """with Files:\s*({file_name}[^,]+?(\.({file_ext}\w+))?.*?)\.\s*$"""
  ]

q-kiteworks-file-activity = {
    Vendor = Accellion
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """\w+\s+\d+ \d+:\d+:\d+\s+({host}(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w.\-]+)))\s+"""
      """({host}(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w.\-]+)))\s+rest_server.py:"""
      """\ssize=({bytes}\d+)"""
      """({email_address}[^@\s]+@({email_domain}[^\s]+))\s+id=[^,]+,\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,\s*Activity:?"""
      """Activity:\s*({operation}.+?)\.\"*\s*$"""
      """Activity Type:\s+({operation}[^\s,]+)"""
     
}
```