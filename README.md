- Задание_1
1. Они перечислены в файле aws/provider.go:
- [data_source](https://github.com/hashicorp/terraform-provider-aws/blob/0d2a4101856d3438cd9b91446e0b7a0e4bf8d3f8/aws/provider.go#L186)
- [Resources](https://github.com/hashicorp/terraform-provider-aws/blob/2b12ec179f2616975ce0afe67b454dce7368a4ed/aws/provider.go#L456)
2. 
- Конфликтует с [ConflictsWith: []string{"name_prefix"},](https://github.com/hashicorp/terraform-provider-aws/blob/2b12ec179f2616975ce0afe67b454dce7368a4ed/aws/resource_aws_sqs_queue.go#L99)
- Как сказано в `website/docs/r/sqs_queue.html.markdown`, Queue names must be made up of only uppercase and lowercase ASCII letters, numbers, underscores, and hyphens, and must be between 1 and 80 characters long
