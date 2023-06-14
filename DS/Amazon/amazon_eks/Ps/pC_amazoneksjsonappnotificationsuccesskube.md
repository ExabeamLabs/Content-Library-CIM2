#### Parser Content
```Java
{
Name = amazon-eks-json-app-notification-success-kube
  Vendor = Amazon
  Product = Amazon EKS
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"application":"shared-kube"""", """"machine_id":"""", """"message":"""]
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """"hostname":"({host}[\w\-.]+)"""",
	  """"application":"({app}[^"]+)"""",
	  """"message":"({additional_info}.+?)","""",
	  """"cmdline":"({process_command_line}.+?)","""",
	  """"size":({bytes}\d+)"""	
  ]


}
```