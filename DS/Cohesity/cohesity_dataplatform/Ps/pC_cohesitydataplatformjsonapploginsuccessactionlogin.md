#### Parser Content
```Java
{
Name = "cohesity-dataplatform-json-app-login-success-actionlogin"
  Vendor = "Cohesity"
  Product = "Cohesity DataPlatform"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
    """cluster_audit:"""
    """"Action" : "Login""""
    """"EntityType" : "User""""
    """"EntityName" :"""
  ]
  Fields = [
    """\"+Timestamp\"+\s+:\s+\"+({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+-\d+:\d+)"""
    """\"+ClusterName:\s*({host}[^,]+)"""
    """\"EntityId\" : \"({user_sid}[^\"]+)"""
    """\"User\"+\s+:\s+\"+({user}[^\"]+)"""
    """\"Domain\"+\s+:\s+\"+({domain}[^\"]+)"""
    """\"Action\"+\s+:\s+\"+({event_name}[^\"]+)"""
    """\"Description\"+\s+:\s+\"+({additional_info}[^,]+?)\"+,"""
    """({app}Iris)"""
    """({event_name}Login)"""
    """logged in from \\*\"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"


}
```