#### Parser Content
```Java
{
Name = freebsd-fbsd-xml-network-close-success-sessionend
 Conditions = [ """event="session end"""", """<subject""", """<record""" ]
 ParserVersion = "v1.0.0"

freebsd-events = {
    Vendor = FreeBSD
    Product = FreeBSD
    TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
    Fields = [
      """\s*time="({time}\w{3}\s\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)"""",
      """\s*uid="({user_id}[^"]+)"""",
      """\s*gid="({group_id}[^"]+)"""",
      """\s*pid="({process_id}[^"]+)"""",
      """<return errval="({result}[^"]+)"\s*""",
      """\s*event="({event_name}[^"]+)"""",
      """Users\s*'({user}[\w\.\-\!\#\^\~]{1,40}\$?)'\s*""",
      """<text>({additional_info}[^<]+)<\/text>""",
      """<path>(|({process_path}({process_dir}.*?)(\/+({process_name}[^\/]+?))?))<\/path>"""
    
}
```