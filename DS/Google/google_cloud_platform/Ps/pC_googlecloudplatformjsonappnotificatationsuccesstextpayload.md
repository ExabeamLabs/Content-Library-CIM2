#### Parser Content
```Java
{
Name = google-cloudplatform-json-app-notificatation-success-textpayload
  Vendor = Google
  Product = Google Cloud Platform
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [""""textPayload":"""",  """"type":"cloud_run_revision"""",""""revision_name":"""","""dproc=Cloud PubSub"""]
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
    """"service_name":"({service_name}[^"]+)"""",
    """destinationServiceName =({app}[^=]+?)\s\w+=""",
	  """"region":"({region}[^"]+)"""",
  ]
  ParserVersion = v1.0.0


}
```