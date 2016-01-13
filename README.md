# ScratchAPI
[Scratch](https://scratch.mit.edu) API Interface

ScratchAPI is a scratch API interface written in [Python](https://www.python.org/).

To get started, install it with `setup.py`

## Logging in
To use the api, you must log in to your scratch account:
```python
import scratchapi
scratch = scratchapi.ScratchUserSession('Username', 'password')
```
Now, you can verify your session to see if you logged in correctly:
```python
scratch.tools.verifySession()
```
There are a lot of things you can you when you're logged in!

Take ownership of a new project:
```python
scratch.lib.utils.request(path='/internalapi/project/new/set/?v=v442&title=Project', server=scratch.PROJECTS_SERVER, method='POST', payload={})
```

Follow Someone:
```python
scratch.users.follow('Bob')
```

Set a cloud variable:
```python
s.cloud.set_var('Variable', 12345, 4453648)
```
