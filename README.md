# Hello world docker action

This action prints "Hello World" to the log or "Hello" + the name of a person to greet. To learn how this action was built, see "[Creating a Docker container action](https://help.github.com/en/articles/creating-a-docker-container-action)" in the GitHub Help documentation.

## Inputs

### `who-to-greet`

**Required** The name of the person to greet. Default `"World"`.

## Outputs

### `time`

The time we greeted you.
**To set a github action output using shell, you should use this syntax**
```
echo "::set-output name=[variable_name]::[variable_value]"
```
Exemple:
```
echo "::set-output name=user_name::Ali"
```
## Example usage

```yaml
uses: actions/hello-world-docker-action@master
with:
  who-to-greet: 'Ali ELLOUZE'
```