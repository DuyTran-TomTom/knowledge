# Terragrunt

```bash
tcc () {
	find . -type d -name "*.terragrunt-cache" -prune -exec rm -rf {} +
	find . -type f -name "*lock.hcl" -delete
}
```
