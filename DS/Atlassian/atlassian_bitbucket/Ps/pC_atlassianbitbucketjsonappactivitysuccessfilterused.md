#### Parser Content
```Java
{
Name = atlassian-bitbucket-json-app-activity-success-filterused
  ParserVersion = "v1.0.0"
  Conditions = [ """"actionI18nKey"""", """atlassian-bitbucket-audit""" ,""""action":"Pull request filters used""""]

atlassian-bitbucket-json-activity = {
    Vendor = Atlassian
    Product = Atlassian BitBucket
    TimeFormat = "epoch_sec"
    Fields = [
	    """"epochSecond":({time}\d{10})""",
      """"action":"({event_name}[^"]+)"""",
	    """"author":.+?"id":"({user_id}\d+)","name":"({user}[\w\.\-]{1,40}\$?)","type":"(?!SERVICE)"""
	    """"actionI18nKey":".+?action\.({operation}[^"]+)""",
	    """({app}bitbucket)""",
      """"source":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
	    """"system":"({resource}[^"]+)"""",
	    """"area":"({additional_info}[^"]+)""""
    
}
```