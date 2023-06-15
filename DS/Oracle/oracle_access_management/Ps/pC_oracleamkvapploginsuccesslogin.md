#### Parser Content
```Java
{
Name = oracle-am-kv-app-login-success-login
  Conditions = [ """ IAU_RESOURCEHOST: """", """IAU_USERID: """", """ IAU_EVENTTYPE: "Login""""  ]
  ParserVersion = v1.0.0

oam-app-activity = {
  Vendor = Oracle
  Product = Oracle Access Management
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\+\-]\d\d:\d\d) ({host}[\w\-.]+)""",
    """IAU_USERID: "(null|Anonymous|GET_HIDE_COLUMN_LIST|({user}[^\s"@]+))"""",
    """IAU_USERID: "(null|Anonymous|({email_address}[^\s"@]+@[^\s"@]+))"""",
    """IAU_IDENTITYDOMAIN: "(null|({domain}[^\s"]+))"""",
    """IAU_INSTANCENAME: "(null|({target}[^"]+))"""",
    """IAU_REMOTEIP: "({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """IAU_CLIENTIPADDRESS: "({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """IAU_RESOURCEHOST: "(null|login|({app}[^"]+))"""",
    """IAU_EVENTTYPE: "(null|({operation}[^"]+))"""",
    """IAU_RESOURCEURI: "(null|({additional_info}[^"]+))"""",
    """IAU_AUTHENTICATIONPOLICYID: "(null|({object}[^"]+))"""",
    """IAU_AUTHORIZATIONPOLICYID: "(null|({object}[^"]+))"""",
    """IAU_RESOURCEID: "(null|({resource}[^"]+))"""",
  
}
```