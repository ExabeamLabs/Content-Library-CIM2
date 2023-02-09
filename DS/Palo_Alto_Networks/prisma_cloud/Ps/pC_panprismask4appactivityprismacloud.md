#### Parser Content
```Java
{
Name = pan-prisma-sk4-app-activity-prismacloud
  Vendor = Palo Alto Networks
  Product = Prisma Cloud
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"resourceCloudService":"Amazon EC2"""", """destinationServiceName =Custom Application""", """"source":"Prisma Cloud"""" ]
  Fields = [
    """"privateIpAddresses":\[.+?"privateIpAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"policyName":"({policy_name}[^"]+)"""",
    """"alertId":"({event_code}[^"]+)"""",
    """"callbackUrl":"({additional_info}[^"]+)"""",
    """"instanceOwnerId":"({user}[^"]+)"""",
    """"source":"({app}[^"]+)"""",
    """"url":"({object}[^"]+)"""",
    """"policyId":"({policy_id}[^"]+)"""",
   ]
  DupFields = ["object->resource" ]


}
```