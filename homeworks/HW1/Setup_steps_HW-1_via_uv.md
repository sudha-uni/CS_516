# Setup steps for HW 1

After you have forked and cloned the project (moments), you can use uv for fast and correct installation of dependencies

UV is a next-generation Python package and project manager, designed to be significantly faster and more efficient than traditional tools like pip and virtualenv. It is developed by Astral and written in Rust, which contributes to its high performance. 
1. Install uv package manager \
Preferred approaches - \
for Windows : 

```shell
winget install --id=astral-sh.uv  -e
```

for macOS : 

```shell
brew install uv
```

Alternate approach : 

```shell
pip install uv
```

2. Navigate to your project directory <br><br>
3. Sync all dependencies from the pyproject.toml to your project. uv sync creates a virtual environment if one doesn't already exist and it creates a uv.lock file which records the exact version of all dependencies.
```shell
uv sync
```
4. Follow the steps mentioned in the readme : To initialize the app, run the flask init-app command:
```shell
uv run flask init-app
```
If you just want to try it out, generate fake data with flask lorem command then run the app:
```shell
uv run flask lorem
```
(If you see an error for any missing dependencies, you can add them in the following way and try running the command again)
```shell
uv add Faker
```

Lorem will create a test account:

email: admin@helloflask.com \
password: moments

Now you can run the app:
```shell
uv run flask run
```
* Running on http://127.0.0.1:5000/
