# Hello world docker action

This action prints "Hello World" to the log or "Hello" + the name of a person to greet. To learn how this action was built, see "[Creating a Docker container action](https://help.github.com/en/articles/creating-a-docker-container-action)" in the GitHub Help documentation.

## Inputs

### `who-to-greet`

**Required** The name of the person to greet. Default `"World"`.

## Outputs

### `time`

The time we greeted you.


## To set a github action output using shell, you should use this syntax:

The `set-output` command is deprecated and will be disabled soon. Please upgrade to using Environment Files. For more information see: https://github.blog/changelog/2022-10-11-github-actions-deprecating-save-state-and-set-output-commands/

<del>

```sh
echo "::set-output name={variable_name}::{variable_value}"
```
</del>

**New Syntax:**

```sh
echo "{name}={value}" >> "$GITHUB_OUTPUT"
```
Exemple:
```sh

echo "user_name=Ali" >> "$GITHUB_OUTPUT"
```
## Example usage

```yaml
uses: actions/hello-world-docker-action@master
with:
  who-to-greet: 'Ali ELLOUZE'
```