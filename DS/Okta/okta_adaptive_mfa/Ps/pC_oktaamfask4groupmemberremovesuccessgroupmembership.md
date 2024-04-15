#### Parser Content
```Java
{
Name = "okta-amfa-sk4-group-member-remove-success-groupmembership"
  Vendor = Okta
  Product = Okta Adaptive MFA
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """Remove user from group membership""", """group.user_membership.remove""", """"actor":""", """"type":""", """destinationServiceName =Okta""" ]
  Fields = [
    """"published":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)"""",
    """"ipAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"actor":\{[^\}]+?"type":"User","alternateId":"({email_address}[^@"]+@[^"]+)"""", """"actor":\{[^\}]+?"type":"User"[^\}]+?"displayName":"({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))"""",
    """"target":\[[^\]]+?"type":"+User","alternateId":"({dest_user}[^"]+)"""",
    """"target":\[[^\]]+?"type":"({object_type}[^"]+)"""",
    """"type":"UserGroup"[^\}]+?"displayName":"({group_name}[^"]+)"""",
    """displayMessage":"({event_name}[^"]+)"""",
    """"eventType":"({event_code}[^"]+)"""",
    """"result":"({action}[^"]t+)""""
  ]
  DupFields = [ "dest_user->object" ]
  ParserVersion = "v1.0.0"


}
```