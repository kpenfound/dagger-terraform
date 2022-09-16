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

## Include this in your cloak.yaml
```yaml
  - git:
      remote: git@github.com:kpenfound/dagger-terraform.git
      ref: main
      path: cloak.yaml
```

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

