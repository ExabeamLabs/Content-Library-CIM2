#### Parser Content
```Java
{
Name = "symantec-bcpa-kv-http-session-get"
  ParserVersion = "v1.0.0"
  Conditions = [
    """method="GET""""
    """OBSERVED"""
    """event_type="web-activity-allowed""""
    """http"""
  ]

bluecoat-proxy-1 = {
  Vendor = Symantec
  Product = Symantec Web Security Service
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """timestamp="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """user="({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """src_host="({src_host}[^"]+)"""",
    """src_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """method="({method}[^"]+)"""",
    """bytes_in="({bytes_in}\d+)"""",
    """bytes_out="({bytes_out}\d+)"""",
    """browser="({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident|Mozilla)"""",
    """os="({os}[^"]+)"""",
    """full_url="({url}(({protocol}[^:]+):\/+)?[^"]+)"""",
    """web_domain="({web_domain}[^"]+)"""",
    """proxy_action="({proxy_action}[^"]+)"""",
    """category="({category}[^"]+)"""",
    """\saction="({action}[^"]+)"""",
    """rule_name="({rule}[^"]+)"""",
    """uri_path="({uri_path}[^"]+)"""",
    """uri_query="({uri_query}[^"]+)"""",
    """referrer="({referrer}[^"]+)""""
  
}
```