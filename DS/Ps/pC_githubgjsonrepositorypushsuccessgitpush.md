#### Parser Content
```Java
{
Name = github-g-json-repository-push-success-gitpush
  ParserVersion = "v1.0.0"
  ExtractionType = json
  Conditions = [ """"action":""", """"git.push"""", """"repository":""" ]
  DupFields = [ "object->repository" ]


}
```