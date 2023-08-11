# HCP vault

```bash
vault-login () {
	export VAULT_ADDR=https://vault.tomtomgroup.com 
	export VAULT_NAMESPACE="ad-delivery/maps-autostream-${1}" 
	vault login -method=oidc
}
```

Example
```bash
vault-login dev
```