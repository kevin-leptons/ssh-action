# SSH Actions

* This is a Github Actions that executes command at remote host.
* It is Docker container action.
* See [Github Actions](https://docs.github.com/en/actions) for more details.

# Usage

```yml
steps:
    - uses: kevin-leptons/ssh_action@v1
      with:
        host: ${{ secrets.REMOTE_HOST }}
        key: ${{ secrets.REMOTE_KEY }}
        command: ls -l
```

* host `{String}` URI refers to remote hosts like `user@domain`.
* key `{String}` SSH private key to authenticate with remote host. At remote
  host, public key must be add to `~/.ssh/authorized_keys`.
* command `{String}` Command to execute, Bash syntax.
* `secrets.REMOTE_HOST` and `secrets.REMOTE_KEY` can be setup by settings of
  Github repository.
