#### Parser Content
```Java
{
Name = rsa-ram-kv-service-app-radiusservicestatus
  Conditions = [ """ SINGLEPOINT """, """ RADIUS_SERVICE_STATUS """ ]
  ParserVersion = "v1.0.0"

rsa-system-events = {
  Vendor = RSA
  Product = RSA Authentication Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """({host}[\w\-\.]+)\s+\d+\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s+\S+\s+SINGLEPOINT\s+\d+\s+({event_name}[^\s]+)\s""",
    """USER_?NAME="({user}[^"\s]+)"""",
    """SOURCE-IP-ADDRESS="({src_ip}[A-Fa-f:\d.]+)""",
# remote_ip is removed
    """STATUS="({result}[^"]+)"""",
    """SESSION_ID="({session_id}[^"]+)"""",
    """USER_AGENT="({user_agent}[^"]+)"""",
    """(APPLICATION|APP_NAME)="({app}[^"]+)"""",
    """REASON="({failure_reason}[^"]+)"""",
    """DESCRIPTION="({additional_info}[^"]+?)\.*""""
  
}
```