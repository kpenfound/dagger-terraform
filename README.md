# dagger-terraform
A dagger extension for terraform operations

## Supported Commands
- fmt
- plan
- apply
- destroy

## Supported Remote States
- Terraform Cloud

## TODO
- Support more remote states

## Example
```gql
query (
  $dir: FSID!
  $token: SecretID!
){
  terraform {
    plan(
      config: $dir
      token: $token
    ) {
      id
    }
  }
}
```

