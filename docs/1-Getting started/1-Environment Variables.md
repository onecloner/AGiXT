### Environment Setup
You can choose to skip the environment setup and accept default values by entering `Y` on the first question `Quick Setup without advanced configuration? (Y for yes, N for No)`.

![image](https://github.com/Josh-XT/AGiXT/assets/102809327/7539d4cf-8081-4bca-97b9-a2affb427d59)

**If you chose `Y`, you can skip the remainder of this section.**

If you choose `N` on skipping environment setup, you will be prompted to enter some settings unless you already have your `.env` file set up.  If you do not have your `.env` file set up, you can use the following as a guide:

![image](https://github.com/Josh-XT/AGiXT/assets/102809327/c8ae9698-f1e0-44b8-9fb2-85cb66b684b7)

- `AGIXT_API_KEY` is the API key to use for the AGiXT API.  This is empty by default, if you would like to set it, change it in the env file.  The header format for requests will be `Authorization: Bearer {your_api_key}` for any requests to your AGiXT server or you can pass the `api_key` to the AGiXT SDK.

- `AGIXT_HUB` is the name of the AGiXT hub, this should be `AGiXT/hub` if you want to use the [Open Source AGiXT hub.](https://github.com/AGiXT/hub) If you want to use your own fork of AGiXT hub, change this to your username and the name of your fork.

- `AGIXT_URI` is the URI of the AGiXT hub, this should be `http://agixt:7437` by default. If hosting the AGiXT server separately, change this to the URI of your AGiXT server, otherwise leave it as-is.
- `GITHUB_USER` is your GitHub username, this is only required if using your own AGiXT hub to pull your repository data.
- `GITHUB_TOKEN` is your GitHub personal access token, this is only required if using your own AGiXT hub to pull your repository data.
- `UVICORN_WORKERS` is the number of workers to run the web server with, this is `6` by default, adjust this to your system's capabilities.

**Database configuration only applicable if using database**
- `DB_CONNECTED` is whether or not you want to use a database, this should be `false` by default, change this to `true` if you want to use a database. If you choose to, you will need to edit the database configuration options below, otherwise they can be left alone.
- `POSTGRES_SERVER` is the name of the database server, this should be `db` by default.
- `POSTGRES_DB` is the name of the database, this should be `postgres` by default.
- `POSTGRES_PORT` is the port that the database is listening on, this should be `5432` by default.
- `POSTGRES_USER` is the username to connect to the database with, this should be `postgres` by default.
- `POSTGRES_PASSWORD` **is the password to connect to the database with, this should be changed from the example file if using database.**

**Oobabooga Text Generation Web UI Configuration**
- `TORCH_CUDA_ARCH_LIST` is the CUDA architecture list to use for the Oobabooga text generation web UI. Example: RTX3000-5000 series are version `7.5`. Find yours at https://developer.nvidia.com/cuda-gpus .
- `CLI_ARGS` is the CLI arguments to pass to the Oobabooga text generation web UI. By default, this is set to `--listen --api --chat` and is not configurable in the AGiXT installer, it will need changed manually in the `.env` file if you want to change it to add additional arguments.

[Next Page: Install Options](https://josh-xt.github.io/AGiXT/1-Getting%20started/2-Install%20Options.html)