#### Parser Content
```Java
{
Name = pingidentity-pi-kv-app-authentication-failure
  ParserVersion = "v1.0.0"
  Conditions = [
     """event=AUTHN_ATTEMPT"""
     """status=failure"""
     """pfhost="""
   ]

ping-events-3 = {
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),""",
    """event=({event_name}[^=]+?)\s+(\w+=|$)""",
    """ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """connectionid=(|({connection_id}[^=]+?))\s+(\w+=|$)""",
    """protocol=(|({protocol}[^=]+?))\s+(\w+=|$)""",
    """pfhost=(|({host}[\w.-]+?))\s+(\w+=|$)""",
    """useragent="({user_agent}[^"]+)"""",
    """description="({additional_info}[^"]]+)""""
    """subject="(|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(?:[^"]+?:)?({user}[\w\.\-]{1,40}\$?)))"""",
  
}
```